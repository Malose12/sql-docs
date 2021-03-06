---
title: "! (Logical Not) (SSIS Expression) | Microsoft Docs"
ms.custom: ""
ms.date: "06/13/2017"
ms.prod: "sql-server-2014"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "integration-services"
ms.tgt_pltfrm: ""
ms.topic: conceptual
helpviewer_keywords: 
  - "logical Not (!)"
  - "! (logical Not)"
ms.assetid: d5c4d1e1-7be4-4d25-bcd9-5b6ddb53b3b3
caps.latest.revision: 35
author: "douglaslMS"
ms.author: "douglasl"
manager: craigg
---
# ! (Logical Not) (SSIS Expression)
  Negates a Boolean operand.  
  
> [!NOTE]  
>  The ! operator cannot be used in conjunction with other operators. For example, you cannot combine the ! and the > operators into the !>. operator.  
  
## Syntax  
  
```  
  
!boolean_expression  
  
```  
  
## Arguments  
 *boolean_expression*  
 Is any valid expression that evaluates to a Boolean. For more information, see [Integration Services Data Types](../data-flow/integration-services-data-types.md).  
  
## Result Types  
 DT_BOOL  
  
## Remarks  
 The following table shows the result of the ! operation.  
  
|Original Boolean expression|After applying the ! operator|  
|---------------------------------|------------------------------------|  
|TRUE|FALSE|  
|NULL|NULL|  
|FALSE|TRUE|  
  
## Expression Examples  
 This example evaluates to FALSE if the **Color** column value is "red".  
  
```  
!(Color == "red")  
```  
  
 This example evaluates to TRUE if the value of the **MonthNumber** variable is the same as the integer that represents the current month. For more information, see [MONTH &#40;SSIS Expression&#41;](month-ssis-expression.md) and [GETDATE &#40;SSIS Expression&#41;](getdate-ssis-expression.md).  
  
```  
!(@MonthNumber != MONTH(GETDATE())  
```  
  
## See Also  
 [Operator Precedence and Associativity](operator-precedence-and-associativity.md)   
 [Operators &#40;SSIS Expression&#41;](operators-ssis-expression.md)  
  
  