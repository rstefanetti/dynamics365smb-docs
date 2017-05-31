---
title: "How to: Calculate Lines from Production Order Headers"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "production orders, calculating lines from"
  - "production orders, headers"
ms.assetid: 1ea70605-414e-49fb-994f-54dddc3135e6
caps.latest.revision: 13
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
# How to: Calculate Lines from Production Order Headers
The production order lines contain the items that are to be produced in the production order.  
  
 You can either insert the production order lines manually or use the function that calculates the production order lines from the header.  
  
 If you use the function to calculate the production order lines from the header, the old production order lines are deleted and new lines are calculated.  
  
### To calculate lines from a production order header  
  
1.  In the **Search** box, enter **Firm Planned Prod. Order**, and then choose the related link.  
  
2.  Create a new firm planned production order.  
  
3.  In the **No.** field, insert the next number in the series.  
  
4.  In the **Source Type** field, select the source of the production order.  
  
5.  In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.  
  
6.  Fill in the **Quantity** and **Due Date** fields according to your specifications.  
  
7.  On the **Actions** tab, in the **Functions** group, choose **Refresh**. The **Refresh Production Order** window opens.  
  
8.  On the **Production Order** FastTab, the current production order has been selected as a default.  
  
9. The following table describes the options available for this batch job.  
  
    |[!INCLUDE[bp_tableoption](../ApplicationDesign/includes/bp_tableoption_md.md)]|Selection|[!INCLUDE[bp_tabledescription](../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Scheduling Direction**|**Forward**|Scheduling starts from the starting date and proceeds forward to the finishing date. You must fill in the starting date to use this option.|  
    ||**Backward**|Scheduling starts from the ending date and proceeds backward to the starting date.|  
    |**Calculate**|**Lines**|Select this field to calculate the production order lines.|  
    ||**Routings**|This field has no influence on calculating the production lines.|  
    ||**Component Need**|This field has no influence on calculating the production lines.|  
    |**Warehouse**|**Create Inbound Request**|This field has no influence on calculating the production lines.|  
  
10. Choose the **OK** button to confirm your selection. Now the production order lines are calculated.  
  
## See Also  
 [How to: Refresh Production Orders](../OperationsPlanning/how-to-refresh-production-orders.md)   
 [How to: Calculate Production Order Components](../OperationsPlanning/how-to-calculate-production-order-components.md)   
 [How to: Calculate Production Order Routing Lines](../OperationsPlanning/how-to-calculate-production-order-routing-lines.md)   
 [About Production Orders](../Production/about-production-orders.md)   
 [How to: Use the Manufacturing Batch Unit of Measure](../DesignAndEngineering/how-to-use-the-manufacturing-batch-unit-of-measure.md)