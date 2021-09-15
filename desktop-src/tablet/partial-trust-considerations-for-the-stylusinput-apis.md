---
description: Vue d’ensemble des problèmes de confiance partielle et de l’interface de programmation d’applications (API) StylusInput.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Considérations relatives à la confiance partielle pour l’API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294498"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Considérations relatives à la confiance partielle pour l’API StylusInput

L' [**RealTimeStylus**](realtimestylus-class.md) qui prend le paramètre *handle* requiert les autorisations [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) , en plus des autorisations requises par le constructeur qui prend le paramètre *attachedControl* .

Pour plus d’informations sur les problèmes de sécurité et d’approbation, consultez [sécurité et confiance](security-and-trust.md).

 

 
