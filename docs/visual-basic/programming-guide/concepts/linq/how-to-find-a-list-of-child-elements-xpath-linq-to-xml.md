---
title: "如何： 查找子元素 (XPATH-LINQ to XML) 的列表 (Visual Basic)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2868abfd-9f7b-412a-9cb5-f643f0fed146
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 110aa447a4804e5162eb45d3d59f12fb174e4473
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-find-a-list-of-child-elements-xpath-linq-to-xml-visual-basic"></a>如何： 查找子元素 (XPATH-LINQ to XML) 的列表 (Visual Basic)
本主题将 XPath 子元素轴与 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] <xref:System.Xml.Linq.XContainer.Elements%2A> 轴进行比较。  
  
 XPath 表达式为：`./*`  
  
## <a name="example"></a>示例  
 本示例查找 `Address` 元素的所有子元素。  
  
 本示例使用以下 XML 文档：[示例 XML 文件：多个采购订单 (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md)。  
  
```vb  
Dim cpo As XDocument = XDocument.Load("PurchaseOrders.xml")  
Dim po As XElement = cpo.Root.<PurchaseOrder>.<Address>.FirstOrDefault  
  
' LINQ to XML query  
Dim list1 As IEnumerable(Of XElement) = po.Elements()  
  
' XPath expression  
Dim list2 As IEnumerable(Of XElement) = po.XPathSelectElements("./*")  
  
If (list1.Count() = list2.Count()) AndAlso _  
    (list1.Intersect(list2).Count() = list1.Count()) Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
For Each el As XElement In list1  
    Console.WriteLine(el)  
Next  
```  
  
 该示例产生下面的输出：  
  
```  
Results are identical  
<Name>Ellen Adams</Name>  
<Street>123 Maple Street</Street>  
<City>Mill Valley</City>  
<State>CA</State>  
<Zip>10999</Zip>  
<Country>USA</Country>  
```  
  
## <a name="see-also"></a>另请参阅  
 [LINQ to XML 针对 XPath 用户 (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
