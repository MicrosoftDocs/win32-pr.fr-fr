---
description: Gestionnaire des ressources de carte à puce
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Gestionnaire des ressources de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536555"
---
# <a name="smart-card-resource-manager"></a>Gestionnaire des ressources de carte à puce

Le [*Gestionnaire de ressources*](../secgloss/r-gly.md) de [*carte à puce*](../secgloss/s-gly.md) gère l’accès aux [*lecteurs*](../secgloss/r-gly.md) et aux *cartes à puce*. Pour gérer ces ressources, il exécute les fonctions suivantes.

-   Identifie et effectue le suivi des ressources.
-   Alloue des lecteurs et des ressources sur plusieurs applications.
-   Prend en charge les primitives de [*transaction*](../secgloss/t-gly.md) pour accéder aux services disponibles sur une carte donnée.
    > [!Note]  
    > Il s’agit d’un point important, car les cartes actuelles sont des appareils à thread unique qui nécessitent souvent l’exécution de plusieurs commandes pour effectuer une seule fonction. Les [*transactions*](../secgloss/t-gly.md) permettent l’exécution de plusieurs commandes sans interruption, garantissant ainsi que les informations d' [*État*](../secgloss/s-gly.md) intermédiaires ne sont pas endommagées.

     

Le gestionnaire de ressources est accessible directement par le biais de l’API Resource Manager ou indirectement par le biais de n’importe quel [*fournisseur de services*](../secgloss/s-gly.md)de carte à puce.

L’API Resource Manager est un ensemble de fonctions Windows qui fournissent un accès direct aux services de Resource Manager. Pour obtenir une vue d’ensemble des fonctions Windows fournies par l’API, consultez [api gestionnaire des ressources de carte à puce](smart-card-resource-manager-api.md). En comparaison, les fournisseurs de services de carte à puce utilisent des interfaces COM.

La plupart des fonctions Windows de l’API Resource Manager ont des équivalents dans les propriétés et les méthodes des interfaces COM des fournisseurs de services de carte à puce. Et même si la plupart des développeurs d’applications trouveront COM plus facile à utiliser, certaines applications devront toujours utiliser les fonctions Windows pour effectuer certaines tâches. Par exemple, les applications qui doivent manipuler la liste des lecteurs ou des groupes de lecteurs dans la [*base de données des cartes à puce*](../secgloss/s-gly.md), et celles qui ont besoin d’un contrôle direct d’un lecteur, doivent utiliser l’API Resource Manager. Les services qui offrent ces fonctionnalités sont disponibles uniquement dans les fonctions Windows, et non dans le COM fourni par les fournisseurs de services.

Pour plus d’informations sur l’implémentation de [*Resource Manager*](../secgloss/r-gly.md) dans Windows, consultez [Gestionnaire des ressources Implementation](resource-manager-implementation.md).

 

 
