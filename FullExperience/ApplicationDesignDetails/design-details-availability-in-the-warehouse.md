---
title: "Design Details: Availability in the Warehouse"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "warehouse, availabilty"
ms.assetid: b910fb95-dc9b-425c-8ab8-bd6a46206518
caps.latest.revision: 9
ms.author: "sgroespe"
manager: "terryaus"
translation.priority.ht: 
  - "da-dk"
  - "de-at"
  - "de-ch"
  - "de-de"
  - "en-au"
  - "en-ca"
  - "en-gb"
  - "en-in"
  - "en-nz"
  - "es-es"
  - "es-mx"
  - "fi-fi"
  - "fr-be"
  - "fr-ca"
  - "fr-ch"
  - "fr-fr"
  - "is-is"
  - "it-ch"
  - "it-it"
  - "nb-no"
  - "nl-be"
  - "nl-nl"
  - "ru-ru"
  - "sv-se"
---
# Design Details: Availability in the Warehouse
The system must keep a constant control of item availability in the warehouse, so that outbound orders can flow efficiently and provide optimal deliveries.  
  
 Availability varies depending on allocations at the bin level when warehouse activities such as picks and movements occur and when the inventory reservation system imposes restrictions to comply with. A rather complex algorithm verifies that all conditions are met before allocating quantities to picks for outbound flows.  
  
## Bin Content and Reservations  
 In any installation of NAV warehouse management, item quantities exist both as warehouse entries, in the Warehouse application area, and as item ledger entries, in the Inventory application area. These two entry types contain different information about where items exist and whether they are available. Warehouse entries define an item’s availability by bin and bin type, which is called bin content. Item ledger entries define an item’s availability by its reservation to outbound documents.  
  
 Special functionality in the picking algorithm exists to calculate the quantity that is available to pick when bin content is coupled with reservations.  
  
## Quantity Available to Pick  
 If, for example, the picking algorithm does not consider item quantities that are reserved for a pending sales order shipment, then those items might be picked for another sales order that is shipped earlier, which prevents the first sales from being fulfilled. To avoid this situation, the picking algorithm subtracts quantities that are reserved for other outbound documents, quantities on existing pick documents, and quantities that are picked but not yet shipped or consumed.  
  
 The result is displayed in the **\($ N\_7345\_52 Available Qty. to Pick $\)** field in the **\($ N\_7345 Pick Worksheet $\)** window, where the field is calculated dynamically. The value is also calculated when users create warehouse picks directly for outbound documents. Such outbound documents could be sales orders, production consumption, or outbound transfers, where the result is reflected in the related quantity fields, such as **\($ T\_5767\_26 Qty. to Handle $\)**.  
  
> [!NOTE]  
>  Concerning the priority of reservations, the quantity to reserve is subtracted from the quantity available to pick. For example, if the quantity available in pick bins is 5 units, but 100 units are in put\-away bins, then when you try to reserve more than 5 units for another order, an error message is displayed because the additional quantity must be available in pick bins.  
  
### Calculating the Quantity Available to Pick  
 The quantity available to pick is calculated as follows:  
  
 quantity available to pick \= quantity in pick bins \- quantity on picks and movements – \(reserved quantity in pick bins \+ reserved quantity on picks and movements\)  
  
 The following diagram shows the different elements of the calculation.  
  
 ![Available to pick, with reservation overlap](../ApplicationDesign/media/design_details_warehouse_management_availability_2.png "design\_details\_warehouse\_management\_availability\_2")  
  
## Quantity Available to Reserve  
 Because the concepts of bin content and reservation co\-exist, the quantity of items that are available to reserve must be aligned with allocations to outbound warehouse documents.  
  
 It should be possible to reserve all items in inventory, except those that have started outbound processing. Accordingly, the quantity that is available to reserve is defined as the quantity on all documents and all bin types, except the following outbound quantities:  
  
-   Quantity on unregistered pick documents  
  
-   Quantity in shipment bins  
  
-   Quantity in to\-production bins  
  
-   Quantity in open shop floor bins  
  
-   Quantity in to\-assembly bins  
  
-   Quantity in adjustment bins  
  
 The result is displayed in the **\($ N\_498\_18 Total Available Quantity $\)** field in the **\($ N\_498 Reservation $\)** window.  
  
 On a reservation line, the quantity that cannot be reserved, because it is allocated in the warehouse, is displayed in the **\($ N\_498\_8 Qty. Allocated in Warehouse $\)** field in the **\($ N\_498 Reservation $\)** window.  
  
### Calculating the Quantity Available to Reserve  
 The quantity available to reserve is calculated as follows:  
  
 quantity available to reserve \= total quantity in inventory \- quantity on picks and movements for source documents \- reserved quantity \- quantity in outbound bins  
  
 The following diagram shows the different elements of the calculation.  
  
 ![Avaliable to reserve, per warehouse allocations](../ApplicationDesign/media/design_details_warehouse_management_availability_3.png "design\_details\_warehouse\_management\_availability\_3")  
  
## See Also  
 [Design Details: Warehouse Management](../ApplicationDesign/design-details-warehouse-management.md)