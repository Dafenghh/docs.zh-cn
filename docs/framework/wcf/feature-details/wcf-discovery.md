---
title: WCF Discovery
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- WCF [WCF], discovery
- Windows Communication Foundation [WCF], discovery
- discovery [WCF]
ms.assetid: 462c4913-f388-45a9-9042-28ae96a4e735
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c11daa14a3897b05947dd6f8c3f3be99eb69c377
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="wcf-discovery"></a>WCF Discovery
[!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] 提供了相关支持，使您能够通过使用 WS-Discovery 协议以互操作方式在运行时发现服务。 [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] 服务可以使用多播消息将自己的可用性公告到网络，也可以公告到发现代理服务器。 客户端应用程序可以搜索网络或发现代理服务器来查找满足一组条件的服务。 本节中的主题分别概述和详细介绍了此功能的编程模型。  
  
## <a name="in-this-section"></a>本节内容  
 [WCF 发现概述](../../../../docs/framework/wcf/feature-details/wcf-discovery-overview.md)  
 概述由 [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] 提供的 WS-Discovery 支持。  
  
 [WCF 发现对象模型](../../../../docs/framework/wcf/feature-details/wcf-discovery-object-model.md)  
 描述对象模型中的类和 WS-Discovery 支持的扩展性。  
  
 [如何：以编程方式向 WCF 服务和客户端添加可发现性](../../../../docs/framework/wcf/feature-details/how-to-programmatically-add-discoverability-to-a-wcf-service-and-client.md)  
 演示如何检测到 [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] 服务。  
  
 [实现发现代理](../../../../docs/framework/wcf/feature-details/implementing-a-discovery-proxy.md)  
 描述一些必需步骤，这些步骤用于实现发现代理、注册到发现代理的可检测服务以及使用发现代理查找可检测服务的客户端。  
  
 [发现版本控制](../../../../docs/framework/wcf/feature-details/discovery-versioning.md)  
 简要概述了一些新发现功能的原型实现， 还概述了如何选择要使用的发现版本。  
  
 [在配置文件中配置发现](../../../../docs/framework/wcf/feature-details/configuring-discovery-in-a-configuration-file.md)  
 演示如何在配置中配置 Discovery。  
  
 [使用发现客户端通道](../../../../docs/framework/wcf/feature-details/using-the-discovery-client-channel.md)  
 演示在编写 [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] 客户端应用程序时如何使用 Discovery 客户端通道。
