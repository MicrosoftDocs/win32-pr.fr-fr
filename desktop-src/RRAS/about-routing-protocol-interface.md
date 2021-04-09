---
title: À propos de l’interface de protocole de routage
description: La documentation suivante décrit l’intégration de protocoles de routage tiers dans le service de routage et d’accès à distance (RRAS).
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- Routage et accès à distance service RRAS, interface de protocole de routage
- Routage et accès à distance service RRAS, interface de protocole de routage, décrite
- Service RRAS de l’interface de protocole de routage
- Interface de protocole de routage RRAS, décrite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674093"
---
# <a name="about-routing-protocol-interface"></a>À propos de l’interface de protocole de routage

La documentation suivante décrit l’intégration de protocoles de routage tiers dans le service de routage et d’accès à distance (RRAS). Le service RRAS est une fonctionnalité de Windows qui joue le rôle de routeur multi-protocole. Le service RRAS définit l’interface entre le gestionnaire de routeur et le protocole de routage. Le protocole de routage est implémenté dans une bibliothèque de liens dynamiques (DLL).

Utilisez cette interface pour implémenter des protocoles de routage, tels que IGRP, NLSP et BGP, en tant que dll en mode utilisateur qui fonctionnent avec RRAS.

Cette documentation décrit les rubriques suivantes :

-   [Adaptateurs](adapters.md)
-   [Interfaces](interfaces.md)
-   [Itinéraires statiques et statiques](static-and-autostatic-routes.md)

 

 




