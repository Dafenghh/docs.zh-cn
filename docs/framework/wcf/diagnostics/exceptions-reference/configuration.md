---
title: "配置"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 86a6e12f-73b5-450e-8725-f4ca5fe0702c
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: bfd61ea70fcae443d4a76403ed6c10c874407c4d
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="configuration"></a>配置
本主题列出由 [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] 配置生成的所有异常。  
  
## <a name="exception-list"></a>异常列表  
  
|资源代码|资源字符串|  
|-------------------|---------------------|  
|ConfigBindingCannotBeConfigured|无法配置服务终结点上的绑定。|  
|ConfigElementKeyNull|特定的配置元素键不能为 Null。|  
|ConfigExtensionTypeNotRegisteredInCollection|特定的扩展类型未在特定的扩展集合中注册。|  
|ConfigIndexOutOfRange|特定属性的值超出范围。|  
|ConfigInvalidBindingConfigurationName|特定的配置未与特定的名称绑定。|  
|ConfigInvalidBindingName|特定的配置未与特定的名称绑定。 对于该绑定，此值无效。|  
|ConfigInvalidCommonEndpointBehaviorType|无法将特定的行为扩展添加到常见终结点行为，因为它未实现特定的类型。|  
|ConfigInvalidCommonServiceBehaviorType|无法将特定的行为扩展添加到常见服务行为，因为它未实现特定的类型。|  
|ConfigInvalidEndpointBehaviorType|无法将特定的行为扩展添加到特定的终结点行为，因为基础行为类型未实现 IServiceBehavior 接口。|  
|ConfigInvalidExtensionType|该特定类型必须派生自要在集合中使用的特定扩展。|  
|ConfigInvalidServiceBehaviorType|无法将行为扩展添加到具有特定名称的服务行为，因为基础行为类型未实现 IServiceBehavior 接口。|  
|ConfigMessageEncodingAlreadyInBinding|无法添加特定的消息编码元素。 另一个消息编码元素已存在于特定的绑定中。 每个绑定只能有一个消息编码元素。|  
|ConfigNoExtensionCollectionAssociatedWithType|找不到与特定类型的扩展关联的扩展集合。|  
|ConfigSectionNotFound|无法创建该特定配置节。 Machine.config 文件中缺少信息。 请验证是否正确注册了此配置节以及节名的拼写是否正确。 对于 Windows Communication Foundation 节，请运行 ServiceModelReg.exe -i 来修复此错误。|  
|ConfigTransportAlreadyInBinding|无法添加特定的传输元素。 另一个传输元素已存在于特定的绑定中。 每个绑定只能有一个消息编码元素。|
