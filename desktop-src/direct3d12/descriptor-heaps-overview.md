---
title: Vue d’ensemble des tas de descripteurs
description: Les tas de descripteurs contiennent de nombreux types d’objets qui ne font pas partie d’un objet d’État du pipeline (PSO), tels que les vues des ressources de nuanceur (SRVs), les vues d’accès non ordonnées (UAVs), les vues de mémoire tampon constante (CBVs) et les échantillonneurs.
ms.assetid: 14561E77-44E0-4A58-8456-F40D59ECA175
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d0017f10a6027fc7ce48618a9d28bd4e92262d83d0f3aa81cc0bc8d02b7edc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124334"
---
# <a name="descriptor-heaps-overview"></a>Vue d’ensemble des tas de descripteurs

Les tas de descripteurs contiennent de nombreux types d’objets qui ne font pas partie d’un objet d’État du pipeline (PSO), tels que les vues des ressources de nuanceur (SRVs), les vues d’accès non ordonnées (UAVs), les vues de mémoire tampon constante (CBVs) et les échantillonneurs.

-   [Rôle des tas de descripteurs](#the-purpose-of-descriptor-heaps)
-   [Synchronisation](#synchronization)
-   [Binding](#binding)
-   [Basculement des tas](#switching-heaps)
-   [Offres groupées](#bundles)
-   [Gestion](#management)
-   [Rubriques connexes](#related-topics)

## <a name="the-purpose-of-descriptor-heaps"></a>Rôle des tas de descripteurs

L’objectif principal d’un tas de descripteur est d’englober la majeure partie de l’allocation de mémoire nécessaire pour stocker les spécifications de descripteur des types d’objets que les nuanceurs font référence à une fenêtre de rendu aussi grande que possible (idéalement une image entière de rendu ou plus). Si une application bascule les textures que le pipeline voit rapidement à partir de l’API, il doit y avoir de l’espace dans le tas du descripteur pour définir les tables de descripteurs à la volée pour chaque ensemble d’États requis. L’application peut choisir de réutiliser les définitions si les ressources sont réutilisées dans un autre objet, par exemple, ou simplement assigner l’espace du tas séquentiellement lorsqu’il change de différents types d’objets.

Les tas de descripteurs permettent également aux composants logiciels individuels de gérer le stockage du descripteur séparément.

Tous les segments de mémoire sont visibles par le processeur. L’application peut également demander les propriétés d’accès de l’UC qu’un tas de descripteur doit avoir (le cas échéant) : écriture combinée, écriture différée, etc. Les applications peuvent créer autant de tas de descripteurs que vous le souhaitez, quelles que soient les propriétés souhaitées. Les applications ont toujours la possibilité de créer des tas de descripteurs qui sont exclusivement à des fins de préproduction qui sont sans contrainte et qui sont copiés dans des tas de descripteurs qui sont utilisés pour le rendu si nécessaire.

Il existe des restrictions concernant ce que peut atteindre le même tas de descripteur. Les entrées CBV, UAV et SRV peuvent se trouver dans le même tas de descripteur. Toutefois, les entrées d’échantillonneurs ne peuvent pas partager un segment de mémoire avec des entrées CBV, UAV ou SRV. En règle générale, il existe deux ensembles de tas de descripteurs, l’un pour les ressources communes et le second pour les échantillonneurs.

L’utilisation de tas de descripteurs par Direct3D 12 reflète ce que fait la majeure partie du matériel GPU, qui consiste soit à exiger des descripteurs en temps réel uniquement dans des tas de descripteurs, soit à réduire le nombre de bits d’adressage si ces tas sont utilisés. Direct3D 12 requiert l’utilisation de tas de descripteurs, il n’est pas possible de placer des descripteurs n’importe où dans la mémoire.

Les tas de descripteurs ne peuvent être modifiés qu’immédiatement par le processeur, il n’est pas possible de modifier un tas de descripteur par le GPU.

## <a name="synchronization"></a>Synchronisation

Le contenu du tas du descripteur peut être modifié avant, pendant et après l’enregistrement des listes de commandes qui le référencent. Toutefois, les descripteurs ne peuvent pas être modifiés lorsqu’une liste de commandes soumise pour l’exécution peut référencer cet emplacement, car cela pourrait appeler une condition de concurrence.

## <a name="binding"></a>Liaison

Au plus un tas combiné CBV/SRV/UAV et un tas d’échantillonneur peuvent être liés à un moment donné. Ces tas sont partagés entre les graphiques et les pipelines de calcul (décrits dans leurs objets PSO).

## <a name="switching-heaps"></a>Basculement des tas

Il est acceptable pour une application de basculer les tas dans la même liste de commandes ou dans d’autres, à l’aide des API [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) et [**Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) . Sur un matériel, il peut s’agir d’une opération coûteuse, nécessitant un blocage du GPU pour vider tout le travail dépendant du tas du descripteur actuellement lié. Par conséquent, si les tas de descripteurs doivent être modifiés, les applications doivent essayer de le faire lorsque la charge de travail GPU est relativement légère, peut-être limiter les modifications au début d’une liste de commandes.

## <a name="bundles"></a>Offres groupées

Avec les offres groupées, il ne peut y avoir qu’un seul appel à la méthode [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) , et les tas de descripteurs définis doivent correspondre exactement à ceux de la liste de commandes qui appelle le bundle. Si le bundle ne modifie pas les tables de descripteurs, il n’a pas besoin de définir les tas de descripteurs.

Pour obtenir la liste des appels d’API qui ne peuvent pas être utilisés avec les offres groupées, consultez [création et enregistrement des listes de commandes et des offres groupées](recording-command-lists-and-bundles.md).

## <a name="management"></a>Gestion

Pour afficher tous les objets d’une scène, de nombreux descripteurs seront nécessaires et des stratégies de gestion différentes peuvent être suivies.

La stratégie la plus simple consisterait à remplir une nouvelle zone du tas de descripteur avec toutes les exigences pour l’appel de dessin suivant. Ainsi, juste avant d’émettre l’appel de dessin sur la liste de commandes, un pointeur de table de descripteur est défini sur le début de la table nouvellement remplie. L’avantage est qu’il n’est pas nécessaire d’enregistrer l’emplacement d’un descripteur particulier dans le tas.

L’inconvénient de cette stratégie est qu’il peut y avoir un grand nombre de descripteurs dans le tas du descripteur, en particulier lors du rendu d’une scène très similaire et que l’espace du tas du descripteur va être utilisé rapidement. Des tas de descripteurs distincts pour ceux qui sont affichés sur le GPU et pour ceux qui sont enregistrés par le processeur, seraient probablement nécessaires pour éviter les conflits. Vous pouvez également utiliser un système de sous-allocation.

En outre, le système de base peut être optimisé davantage en utilisant avec précaution les tables de descripteurs qui se chevauchent d’un appel de dessin à l’étape suivante, afin que seuls les nouveaux descripteurs nécessaires soient ajoutés.

Une stratégie plus efficace que la plus simple consisterait à préremplir les tas de descripteurs avec les descripteurs requis pour les objets (ou les matériaux) qui sont connus pour faire partie de la scène. L’idée est qu’il n’est nécessaire de définir la table du descripteur qu’au moment du dessin, car le tas du descripteur est rempli à l’avance.

Une variante de la stratégie de préremplissage consiste à traiter le tas du descripteur comme un tableau énorme, contenant tous les descripteurs requis dans des emplacements connus fixes. L’appel de dessin doit ensuite uniquement recevoir un ensemble de constantes qui sont les index dans le tableau de où les descripteurs doivent être utilisés.

Une autre optimisation consiste à s’assurer que les constantes racine et les descripteurs racine contiennent des constantes qui changent le plus souvent, plutôt que de placer des constantes dans le tas du descripteur. Pour la plupart des matériels, il s’agit d’un moyen efficace de gérer les constantes.

Dans la pratique, un moteur graphique peut utiliser une stratégie différente dans différentes situations, et combiner des éléments de chaque stratégie pour répondre aux exigences de dessin particulières.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tas de descripteurs](descriptor-heaps.md)
</dt> </dl>

 

 




