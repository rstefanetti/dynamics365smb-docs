---
title: "How to: Set Up Withholding Tax"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "Business Activity Statement (BAS), setting up withholding tax"
  - "posting groups, WHT"
  - "withholding tax, setting up"
ms.assetid: 06b087a5-782c-4af3-9d96-34aa900b801c
caps.latest.revision: 20
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "en-au"
---
# How to: Set Up Withholding Tax
Withholding tax \(WHT\) is the tax withheld by a company when it makes a payment to a vendor, in which the full amount owed to the vendor is reduced by the tax withheld. The withheld tax is then remitted to the Australian Taxation Office \(ATO\) when the next Business Activity Statement \(BAS\) is submitted.  
  
 If a supplier without an Australian Business Number \(ABN\) provides an invoice, a withholding tax amount must be withheld if the total amount of the invoice is more than the threshold amount.  
  
 To use withholding tax, you must set up the business posting groups and product posting groups for withholding tax so that the correct WHT calculations are made for each vendor.  
  
> [!NOTE]  
>  As a prerequisite, you need to set up source codes for WHT settlement in the **\($ N\_279 Source Code Setup $\)** window.  
  
 The following procedure describes how to set up product posting groups for WHT, but the same steps also apply to setting up business posting groups for WHT.  
  
### To set up a product posting group for withholding tax  
  
1.  In the **Search** box, enter **\($ N\_28041 WHT Product Posting Group $\)**, and then choose the related link.  
  
2.  Fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_28041\_1 Code $\)**|Specify the code for the product posting group. You can enter a maximum of 10 alphanumeric characters.|  
    |**\($ T\_28041\_2 Description $\)**|Specify the description for the product posting group. You can enter a maximum of 50 alphanumeric characters.|  
  
3.  Choose the **OK** button.  
  
### To set up posting for withholding tax  
  
1.  In the **Search** box, enter **\($ N\_28043 WHT Posting Setup $\)**, and then choose the related link.  
  
2.  Fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_28043\_1 WHT Business Posting Group $\)**|Specifies the business posting group code for withholding tax.|  
    |**\($ T\_28043\_2 WHT Product Posting Group $\)**|Specifies the product posting group code for withholding tax.|  
    |**\($ T\_28043\_25 WHT Calculation Rule $\)**|Specifies the calculation rule for WHT, which is used with the amount specified in the **\($ T\_28043\_24 WHT Minimum Invoice Amount $\)** field. This will help identify the transactions for which WHT will not be deducted.<br /><br /> For example, if you select the **Less than** option here and enter 100 in the **\($ T\_28043\_24 WHT Minimum Invoice Amount $\)** field, then WHT will not be deducted for those transactions with an amount less than 100.|  
    |**\($ T\_28043\_24 WHT Minimum Invoice Amount $\)**|Specifies the threshold amount that is below which WHT will not be deducted.|  
    |**\($ T\_28043\_3 WHT % $\)**|Specifies the WHT rate. You must enter the rate without the percent sign.|  
    |**\($ T\_28043\_23 Realized WHT Type $\)**|Specifies the mode of WHT calculation for purchases or sales of items.|  
    |**\($ T\_28043\_4 Prepaid WHT Account Code $\)**|Specifies the general ledger account number to which sales WHT is to be posted.|  
    |**\($ T\_28043\_5 Payable WHT Account Code $\)**|Specifies the general ledger account number to which purchase WHT is to be posted.|  
    |**\($ T\_28043\_7 WHT Report $\)**|Specifies the withholding tax report type.|  
    |**\($ T\_28043\_10 Bal. Prepaid Account Type $\)**|Specifies the type of balancing account for sales WHT transactions.|  
    |**\($ T\_28043\_11 Bal. Prepaid Account No. $\)**|Specifies the account number or bank name for sales WHT transactions, based on the type selected in the **\($ T\_28043\_10 Bal. Prepaid Account Type $\)** field.|  
    |**\($ T\_28043\_12 Bal. Payable Account Type $\)**|Specifies the type of balancing account for purchase WHT transactions.|  
    |**\($ T\_28043\_13 Bal. Payable Account No. $\)**|Specifies the account number or bank name for purchase WHT transactions. This is based on the type selected in the **\($ T\_28043\_12 Bal. Payable Account Type $\)** field.|  
    |**\($ T\_28043\_8 WHT Report Line No. Series $\)**|Specifies the number series for the WHT report line.|  
    |**\($ T\_28043\_9 Revenue Type $\)**|Specifies the revenue type. For more information, see [How to: Set Up Revenue Types for Withholding Tax](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Australia/how-to-set-up-revenue-types-for-withholding-tax.md).|  
    |**\($ T\_28043\_20 Purch. WHT Adj. Account No. $\)**|Specifies the account number which to post purchase credit memo adjustments.|  
    |**\($ T\_28043\_21 Sales WHT Adj. Account No. $\)**|Specifies the account number to post sales credit memo adjustments.|  
    |**\($ T\_28043\_22 Sequence $\)**|Specifies the sequence in which the withholding tax posting setup information must be displayed in reports.|  
  
3.  Choose the **OK** button.  
  
## See Also  
 [How to: Set Up Revenue Types for Withholding Tax](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Australia/how-to-set-up-revenue-types-for-withholding-tax.md)   
 [How to: View Withholding Tax Entries](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Australia/how-to-view-withholding-tax-entries.md)   
 [How to: Calculate and Post Withholding Tax Settlements](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Australia/how-to-calculate-and-post-withholding-tax-settlements.md)   
 [Withholding Tax](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Australia/withholding-tax.md)   
 [\($ N\_279 Source Code Setup $\)](assetId:///dc7fc6db-e9d1-40a6-be60-2ba6e9cf5c69)   
 [Australian Taxation Office \(ATO\)](http://www.ato.gov.au/)