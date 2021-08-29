---
description: Gestionnaire des ressources de carte à puce
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Gestionnaire des ressources de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9d78b1d54a4db3fa8146b2689173c264e8320da024d0dc3e165dd648b8a33d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917508"
---
# <a name="smart-card-resource-manager"></a>Gestionnaire des ressources de carte à puce

Le [*Gestionnaire de ressources*](../secgloss/r-gly.md) de [*carte à puce*](../secgloss/s-gly.md) gère l’accès aux [*lecteurs*](../secgloss/r-gly.md) et aux *cartes à puce*. Pour gérer ces ressources, il exécute les fonctions suivantes.

-   Identifie et effectue le suivi des ressources.
-   Alloue des lecteurs et des ressources sur plusieurs applications.
-   Prend en charge les primitives de [*transaction*](../secgloss/t-gly.md) pour accéder aux services disponibles sur une carte donnée.
    > [!Note]  
    > Il s’agit d’un point important, car les cartes actuelles sont des appareils à thread unique qui nécessitent souvent l’exécution de plusieurs commandes pour effectuer une seule fonction. Les [*transactions*](../secgloss/t-gly.md) permettent l’exécution de plusieurs commandes sans interruption, garantissant ainsi que les informations d' [*État*](../secgloss/s-gly.md) intermédiaires ne sont pas endommagées.

     

Le gestionnaire de ressources est accessible directement par le biais de l’API Resource Manager ou indirectement par le biais de n’importe quel [*fournisseur de services*](../secgloss/s-gly.md)de carte à puce.

l’API resource manager est un ensemble de fonctions de Windows qui fournissent un accès direct aux services du gestionnaire de ressources. pour obtenir une vue d’ensemble des Windows fonctions fournies par l’api, consultez [api Gestionnaire des ressources de carte à puce](smart-card-resource-manager-api.md). En comparaison, les fournisseurs de services de carte à puce utilisent des interfaces COM.

la plupart des fonctions de Windows dans l’API resource manager ont des équivalents dans les propriétés et les méthodes des interfaces COM des fournisseurs de services de carte à puce. et même si la plupart des développeurs d’applications trouveront COM plus facile à utiliser, certaines applications devront toujours utiliser les fonctions de Windows pour effectuer certaines tâches. Par exemple, les applications qui doivent manipuler la liste des lecteurs ou des groupes de lecteurs dans la [*base de données des cartes à puce*](../secgloss/s-gly.md), et celles qui ont besoin d’un contrôle direct d’un lecteur, doivent utiliser l’API Resource Manager. les services qui offrent ces fonctionnalités sont disponibles uniquement dans les fonctions Windows, et non dans le COM fourni par les fournisseurs de services.

pour plus d’informations sur l’implémentation de [*resource manager*](../secgloss/r-gly.md) dans Windows, consultez [Gestionnaire des ressources implementation](resource-manager-implementation.md).

 

 
