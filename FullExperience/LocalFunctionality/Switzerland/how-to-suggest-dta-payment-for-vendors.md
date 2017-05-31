---
title: "How to: Suggest DTA Payment for Vendors"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "DTA payments, suggesting vendors"
ms.assetid: 8daeddb8-bb59-451f-b491-fa22f44bcb80
caps.latest.revision: 2
ms.author: "edupont"
translation.priority.ht: 
  - "de-ch"
  - "fr-ch"
---
# How to: Suggest DTA Payment for Vendors
You can suggest vendor payments using the payment journal, and transfer the overdue invoices into the journal for individual vendors. You can also examine each vendor for open credit memos or open payments, and build a list of vendors for DatenTrägerAustausch \(DTA\) processing. For more information, see [How to: Verify a List of Vendors for DTA Payments](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Switzerland/how-to-verify-a-list-of-vendors-for-dta-payments.md).  
  
 During the batch processing of DTA payment suggestions, the foreign currency \(FCY\) amount is converted to local currency \(LCY\) at the current rate for FCY payments, and transferred into the payment journal. For more information, see the **\($ N\_256 Payment Journal $\)** window. In the case of a bank debit, the LCY amount is overwritten with the debited LCY amount, and the exchange rate—or exchange factor—is calculated. For more information, see the [\($ T\_98 General Ledger Setup $\)](assetId:///199e09dc-fe90-4792-be3e-ad395447dfd6) table and the [\($ T\_330 Currency Exchange Rate $\)](assetId:///b0b89d1c-bc67-4cc9-ba62-20ddd368452c) table.  
  
### To suggest DTA payment for vendors  
  
1.  In the **Search** box, enter **Payment Journals**, and then choose the related link.  
  
2.  In the **\($ N\_256\_33 Batch Name $\)** field, select the required journal batch.  
  
3.  Select the required payment line, and on the **Home** tab, in the **Process** group, select **DTA Suggest Vendor Payment**.  
  
4.  In the **DTA Suggest Vendor Payments** window, on the **Options** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ B\_3010546\_F\_1\_25 Posting Date $\)**|Specify the credit date for the payment. This date is useful in determining whether a payment discount has been provided.|  
    |**\($ B\_3010546\_F\_1\_22 Due Date from $\)**|Specify the starting date for the open invoices to be included in the payment suggestion.|  
    |**\($ B\_3010546\_F\_1\_24 Due Date to $\)**|Specify the ending date for the open invoices to be included in the payment suggestion.|  
    |**\($ B\_3010546\_F\_1\_20 Process Cash Discounts $\)**|Specify if the cash discount payments outside the due date range will be considered for the payment suggestion.|  
    |**\($ B\_3010546\_F\_1\_13 Cash Disc. Date from $\)**|Specify the starting date for the cash discount. The open entries with cash discount dates within this date range are included in the payment suggestion.|  
    |**\($ B\_3010546\_F\_1\_19 Cash Disc. Date to $\)**|Specify the ending date for the cash discount. The open entries with cash discount dates within this date range are included in the payment suggestion.|  
    |**\($ B\_3010546\_F\_1\_12 Available Amount \(LCY\) $\)**|Enter the maximum value of the sum of all payments.|  
    |**\($ B\_3010546\_F\_1\_11 First Doc. No. $\)**|Specify the payment suggestion document number. This number is assigned according to the number series for the current log.|  
    |**\($ B\_3010546\_F\_1\_1 Debit to Bank $\)**|Select the code of the bank that will receive the debit. The bank must be activated for DTA.|  
    |**\($ B\_3010546\_F\_1\_3 Auto. Debit Bank $\)**|Specify if the bank will be debited automatically, depending on the currency code.|  
  
5.  Choose the **OK** button.  
  
 During processing, each vendor is checked for open credit memos or open payments, and a message displays at the end of the process. All of the related lines are transferred to the payment journal. The related vendor ledger entries are marked with **DTA** to prevent transfer of duplicate entries to the payment journal. You can view, check, and modify the suggested payments, and you can decide whether to reduce the payments by the credit memo amounts, or to apply the open credit memos and open invoices.  
  
## See Also  
 [Swiss Electronic Payments Using DTA](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Switzerland/swiss-electronic-payments-using-dta.md)   
 [How to: Verify a List of Vendors for DTA Payments](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Switzerland/how-to-verify-a-list-of-vendors-for-dta-payments.md)   
 [How to: Submit DTA Payments](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Switzerland/how-to-submit-dta-payments.md)   
 [How to: Export Payments Using EZAG](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Switzerland/how-to-export-payments-using-ezag.md)   
 [\($ T\_3010541 DTA Setup $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Switzerland/-$-t_3010541-dta-setup-$-.md)   
 [\($ T\_98 General Ledger Setup $\)](assetId:///199e09dc-fe90-4792-be3e-ad395447dfd6)   
 [\($ T\_330 Currency Exchange Rate $\)](assetId:///b0b89d1c-bc67-4cc9-ba62-20ddd368452c)   
 [\($ N\_256 Payment Journal $\)](../../Finance/-$-n_256-payment-journal-$-.md)   
 [How to: Suggest Vendor Payments](../../Finance/how-to-suggest-vendor-payments.md)   
 [\($ B\_393 Suggest Vendor Payments $\)](../Topic/\($%20B_393%20Suggest%20Vendor%20Payments%20$\).md)   
 [\($ T\_288\_3010550 Debit Bank $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Switzerland/-$-t_288_3010550-debit-bank-$-.md)