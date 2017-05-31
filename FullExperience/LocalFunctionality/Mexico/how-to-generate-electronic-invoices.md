---
title: "How to: Generate Electronic Invoices"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "electronic invoices, generating"
ms.assetid: 1a65d68b-0851-42d6-af52-a2608d1f8ae1
caps.latest.revision: 7
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "es-mx"
---
# How to: Generate Electronic Invoices
In [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)], after you post a sales invoice you must generate an electronic invoice that will be sent to the customer. You can also export the electronic invoice as an XML file, which you can save to a specified location.  
  
 The following procedure describes how to generate electronic invoices for sales invoices, but the same steps also apply to service invoices and credit memos.  
  
### To generate electronic invoices for sales invoices  
  
1.  In the **Search** box, enter **\($ N\_132 Posted Sales Invoice $\)**, and then choose the related link.  
  
2.  Select the posted invoice.  
  
3.  On the **Actions** tab, in the **Functions** group, choose **Send Electronic Document**. An email will be sent to the customer with the electronic invoice attached as an XML file. If you selected the **\($ T\_98\_10005 Send PDF Report $\)** field in the **\($ N\_118 General Ledger Setup $\)** window, a PDF will be included with the XML file.  
  
4.  Optionally, on the **Actions** tab, in the **Functions** group, choose **Export E\-Document as XML**. Select the location where you want to save the electronic invoice as an XML file.  
  
     To verify the electronic invoice activity, in the **\($ N\_132 Posted Sales Invoice $\)** window, on the **Invoicing** FastTab, the **\($ T\_112\_10019 Electronic Document Sent $\)** and **\($ T\_112\_10021 No. of E\-Document Submissions $\)** fields will be updated.  
  
> [!NOTE]  
>  [!INCLUDE[bp_refimplementation](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Austria/includes/bp_refimplementation_md.md)]  
  
## See Also  
 [How to: Set Up Electronic Invoicing](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Mexico/how-to-set-up-electronic-invoicing.md)   
 [Electronic Invoicing](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Mexico/electronic-invoicing.md)   
 [\($ N\_132 Posted Sales Invoice $\)](../Topic/\($%20N_132%20Posted%20Sales%20Invoice%20$\).md)   
 [\($ N\_118 General Ledger Setup $\)](assetId:///40b9235c-b0d7-4a9f-9ecf-6dc97655309b)