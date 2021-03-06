---
title: "如何：检测何时按下 Enter 键"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Enter key [WPF], detecting
- keys [WPF], Enter
ms.assetid: a66f39d2-ef4a-43a5-b454-a4ea0fe88655
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 21bb0dc8a38f8b49a4f5372c9dfc1e17e5114d6a
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-detect-when-the-enter-key-pressed"></a>如何：检测何时按下 Enter 键
此示例演示如何检测何时<xref:System.Windows.Input.Key.Enter>键盘上按下键。  
  
 此示例组成[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]文件和代码隐藏文件。  
  
## <a name="example"></a>示例  
 当用户按<xref:System.Windows.Input.Key.Enter>中的键<xref:System.Windows.Controls.TextBox>，在文本框中输入将出现在另一个区域的[!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)]。  
  
 以下[!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)]创建用户界面，其中包括<xref:System.Windows.Controls.StackPanel>、 <xref:System.Windows.Controls.TextBlock>，和一个<xref:System.Windows.Controls.TextBox>。  
  
 [!code-xaml[keydown#KeyDownUI](../../../../samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml#keydownui)]  
  
 下面的代码隐藏创建<xref:System.Windows.UIElement.KeyDown>事件处理程序。  如果按下的键是<xref:System.Windows.Input.Key.Enter>密钥，显示一条消息是在<xref:System.Windows.Controls.TextBlock>。  
  
 [!code-csharp[keydown#KeyDownSample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml.cs#keydownsample)]
 [!code-vb[keydown#KeyDownSample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/KeyDown/VisualBasic/Window1.xaml.vb#keydownsample)]  
  
## <a name="see-also"></a>请参阅  
 [输入概述](../../../../docs/framework/wpf/advanced/input-overview.md)  
 [路由事件概述](../../../../docs/framework/wpf/advanced/routed-events-overview.md)
