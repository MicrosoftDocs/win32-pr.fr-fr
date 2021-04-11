---
description: Vue d’ensemble des problèmes de confiance partielle et de l’interface de programmation d’applications (API) StylusInput.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Considérations relatives à la confiance partielle pour l’API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204041"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a><span data-ttu-id="10742-103">Considérations relatives à la confiance partielle pour l’API StylusInput</span><span class="sxs-lookup"><span data-stu-id="10742-103">Partial Trust Considerations for the StylusInput API</span></span>

<span data-ttu-id="10742-104">L' [**RealTimeStylus**](realtimestylus-class.md) qui prend le paramètre *handle* requiert les autorisations [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) , en plus des autorisations requises par le constructeur qui prend le paramètre *attachedControl* .</span><span class="sxs-lookup"><span data-stu-id="10742-104">The [**RealTimeStylus**](realtimestylus-class.md) that takes the *handle* parameter requires the [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) and [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/) permissions, in addition to the permissions required by the constructor that takes the *attachedControl* parameter.</span></span>

<span data-ttu-id="10742-105">Pour plus d’informations sur les problèmes de sécurité et d’approbation, consultez [sécurité et confiance](security-and-trust.md).</span><span class="sxs-lookup"><span data-stu-id="10742-105">For more information about security and trust issues, see [Security and Trust](security-and-trust.md).</span></span>

 

 
