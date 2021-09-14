---
title: À propos du gestionnaire de table de routage version 2
description: La documentation suivante décrit la technologie du gestionnaire de tables de routage version 2 (RTMv2).
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- Routage et accès à distance service RRAS, gestionnaire de tables de routage version 2
- Routage et accès à distance service RRAS, gestionnaire de table de routage version 2, Description
- Gestionnaire de routage de la version 2 RRAS
- Gestionnaire de routage de la version 2 RRAS, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119045"
---
# <a name="about-routing-table-manager-version-2"></a>À propos du gestionnaire de table de routage version 2

La documentation suivante décrit la technologie du gestionnaire de tables de routage version 2 (RTMv2). l’API RTMv2 est une fonctionnalité de Windows 2000 et des systèmes d’exploitation ultérieurs que vous pouvez utiliser pour écrire des protocoles de routage qui interagissent avec le gestionnaire de tables de routage.

Le gestionnaire de tables de routage est le référentiel central des informations de routage pour tous les protocoles de routage qui fonctionnent sous le service de routage et d’accès à distance (RRAS).

RTMv2 n’est pas disponible pour Windows NT version 4,0. en outre, RTMv2 ne peut pas être utilisé pour les protocoles de routage IPX qui s’exécutent sur Windows NT 4,0 ou Windows 2000. Si vous utilisez IPX ou si vous écrivez des protocoles de routage pour Windows NT 4,0, reportez-vous à la rubrique à [propos du gestionnaire de tables de routage version 1](about-routing-table-manager-version-1.md).

Cette vue d’ensemble décrit les rubriques suivantes :

-   [Composants de l’architecture du gestionnaire de tables de routage](components-of-the-routing-table-manager-architecture.md)
-   [Inscription auprès du gestionnaire de tables de routage](registering-with-the-routing-table-manager.md)
-   [Énumération des entités inscrites](enumerating-registered-entities.md)
-   [Utilisation de méthodes](using-methods.md)
-   [Utilisation de pointeurs opaques](using-opaque-pointers.md)
-   [Marquage des itinéraires pour l’État Hold-Down](marking-routes-for-the-hold-down-state.md)
-   [Ajout d’itinéraires](adding-routes.md)
-   [Récupération des informations d’itinéraire](retrieving-route-information.md)
-   [Mise à jour des itinéraires](updating-routes.md)
-   [Réception des notifications de modifications](receiving-notification-of-changes.md)
-   [Utilisation des tronçons suivants](working-with-next-hops.md)
-   [Énumération des entrées de table de routage](enumerating-routing-table-entries.md)
-   [Recherche d’informations spécifiques dans la table de routage](finding-specific-information-in-the-routing-table.md)
-   [Maintenance des listes de Client-Specific](maintaining-client-specific-lists.md)
-   [Gestion des handles](managing-handles.md)

 

 




