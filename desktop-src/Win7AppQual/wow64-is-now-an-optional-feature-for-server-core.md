---
description: WoW64 est désormais une fonctionnalité facultative pour Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: État WoW64 dans Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084047"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>WoW64 est désormais une fonctionnalité facultative pour Server Core

## <a name="affected-platforms"></a>Plateformes affectées

**Serveurs** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

L’option d’installation Server Core pour Windows Server 2008 R2 vous permet de désinstaller WoW64. WoW64 est désormais une fonctionnalité facultative que vous pouvez désinstaller si vous n’avez pas besoin d’exécuter du code 32 bits.

En outre, les rôles Active Directory et services AD LDS (Active Directory Lightweight Directory Services) requièrent WoW64 pour s’exécuter dans Windows Server 2008 R2.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

Si vous désinstallez WoW64, les administrateurs qui exécutent le code 32 bits sur Server Core recevront un message d’erreur indiquant que l’application ne peut pas être exécutée. Si les administrateurs essaient d’exécuter Active Directory et services AD LDS (Active Directory Lightweight Directory Services), ils recevront un message d’erreur.

## <a name="mitigation"></a>Limitation des risques

Installez WoW64.

## <a name="solution"></a>Solution

La solution recommandée consiste à fournir une version 64 bits du code pour lui permettre de s’exécuter sur Server Core sans avoir besoin de WoW64.

Au minimum, fournissez une documentation utilisateur indiquant que pour exécuter le code 32 bits, ils doivent installer WoW64.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

Vérifiez que tout le code utilisé est 64 bits.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Détails de l’implémentation WOW64](../winprog64/wow64-implementation-details.md)
-   [Débogage de WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
