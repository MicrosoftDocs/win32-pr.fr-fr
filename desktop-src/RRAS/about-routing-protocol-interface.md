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
ms.openlocfilehash: 76689e0e7ca40c2677491fc0673c596c902a73ee85b677161c208fe71d090367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792116"
---
# <a name="about-routing-protocol-interface"></a>À propos de l’interface de protocole de routage

La documentation suivante décrit l’intégration de protocoles de routage tiers dans le service de routage et d’accès à distance (RRAS). le service RRAS est une fonctionnalité de Windows qui joue le rôle de routeur multi-protocole. Le service RRAS définit l’interface entre le gestionnaire de routeur et le protocole de routage. Le protocole de routage est implémenté dans une bibliothèque de liens dynamiques (DLL).

Utilisez cette interface pour implémenter des protocoles de routage, tels que IGRP, NLSP et BGP, en tant que dll en mode utilisateur qui fonctionnent avec RRAS.

Cette documentation décrit les rubriques suivantes :

-   [Adaptateurs](adapters.md)
-   [Interfaces](interfaces.md)
-   [Itinéraires statiques et statiques](static-and-autostatic-routes.md)

 

 




