---
title: "官方 .NET Docker 映像"
description: "适用于容器化 .NET 应用程序的 .NET 微服务体系结构 | 官方 .NET Docker 映像"
keywords: "Docker, 微服务, ASP.NET, 容器"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 42872caa1a9306187daeefd35feb9bec3fae60af
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/23/2017
---
# <a name="official-net-docker-images"></a>官方 .NET Docker 映像

官方 .NET Docker 映像是由 Microsoft 创建和优化的 Docker 映像。 这些映像在 [Docker 中心](https://hub.docker.com/u/microsoft/)的 Microsoft 存储库中公开提供。 每个存储库可以包含多个映像，具体取决于 .NET 版本以及操作系统和版本（Linux Debian、Linux Alpine、Windows Nano Server、Windows Server Core 等）。

Microsoft 对 .NET 存储库的愿景是要具有细粒度和集中存储库，其中存储库表示特定方案或工作负荷。 例如，当在 Docker 上使用 ASP.NET Core 时，应使用 [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) 映像，因为这些 ASP.NET Core 映像提供了额外的优化，以便容器可以更快地启动。

另一方面，.NET Core 映像 (microsoft/dotnet) 适用于基于 .NET Core 的控制台应用。 例如，批处理、Azure WebJobs 和其他控制台方案应使用 .NET Core。 这些映像不包括 ASP.NET Core 堆栈，因此导致容器映像更小。

大多数映像存储库提供广泛的标记，以帮助选择特定的框架版本以及 OS（Linux 发行版或 Windows 版本）。

有关 Microsoft 提供的官方 .NET Docker 映像的详细信息，请参阅 [.NET Docker 映像摘要](https://aka.ms/dotnetdockerimages)。

## <a name="net-core-and-docker-image-optimizations-for-development-versus-production"></a>适用于开发与生产的 .NET Core 和 Docker 映像优化

为开发人员生成 Docker 映像时，Microsoft 侧重于以下主要方案：

-   用于开发和生成 .NET Core 应用的映像。

-   用于运行 .NET Core 应用的映像。

为什么是多个映像？ 因为在开发、生成和运行容器化应用程序时，通常具有不同的优先级。 通过为这些单独的任务提供不同的映像，Microsoft 有助于优化开发、生成和部署应用程序的单独进程。

### <a name="during-development-and-build"></a>在开发和生成过程中

在开发期间，重要的是可循环访问更改的速度以及调试更改的能力。 与更改代码的能力和快速查看更改相比，映像的大小不是那么重要。 某些工具和“build-agent 容器”在开发和生成过程中使用开发 ASP.NET Core 映像 (microsoft/aspnetcore-build)。 在 Docker 容器中生成时，重要方面是为了编译应用所需要的元素。 这包括编译器和任何其他 .NET 依赖项，以及 npm、Gulp和 Bower 等 Web 开发依赖项。

为什么此类型的生成映像很重要？ 不能将此映像部署到生产中。 相反，它是用于生成放置在生产映像中的内容的映像。 此映像将用于持续集成 (CI) 环境或生成环境中。 例如，生成代理会将 .NET Core 实例化，其中包含构建应用程序所需的所有依赖项，而不是直接在生成代理主机（例如 VM）上手动安装所有应用程序依赖项。 生成代理只需要了解如何运行此 Docker 映像即可。 这简化了 CI 环境，并使其更可预测。

### <a name="in-production"></a>生产中

在生产中重要的是基于生产 .NET Core 映像部署和启动容器的速度。 因此，基于 [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) 的仅运行时映像很小，以便它可以通过网络从 Docker 注册表快速传输到 Docker 主机。 已准备运行内容，以此实现从启动容器到处理结果的最快时间。 在 Docker 模型中，不需要编译 C\# 代码，但在使用生成容器运行 dotnet 生成或 dotnet 发布时需要。

在此优化的映像中，只放置运行应用程序所需的二进制文件和其他内容。 例如，由 dotnet 发布创建的内容仅包含已编译的.NET 二进制文件、映像、.js 和 .css 文件。 随着时间的推移，用户将看到包含预实时编译的包。

虽然 .NET Core 和 ASP.NET Core 映像有多个版本，但它们全都共享一个或多个层，包括基本层。 因此，存储映像所需的磁盘空间量很小；它仅包含自定义映像和其基础映像之间的增量。 结果，从注册表中提取映像速度会很快。

在 Docker 中心浏览 .NET 映像存储库时，会发现已使用标记将多个映像版本进行分类或标记。 这些标记有助于决定使用哪一个，具体取决于需要的版本，如下表所示：

-   microsoft/**aspnetcore:2.0**

        ASP.NET Core, with runtime only and ASP.NET Core optimizations, on Linux and Windows (multi-arch)

-   microsoft/aspnetcore-build:2.0

        ASP.NET Core, with SDKs included, on Linux and Windows (multi-arch)


>[!div class="step-by-step"]
[上一篇] (net-container-os-targets.md) [下一篇] (../architect-microservice-container-applications/index.md)
