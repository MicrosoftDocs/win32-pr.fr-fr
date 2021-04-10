---
title: Définition de la priorité cible du serveur DFS
description: La définition de priorités de serveur DFS est une fonctionnalité disponible dans Microsoft Windows Server 2003 avec Service Pack 1 (SP1) et les systèmes d’exploitation ultérieurs.
ms.assetid: 0aacebf7-49cc-4287-a5c4-0d25a416d227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e784a540a67f624ca5b8075009cd862c6063427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201116"
---
# <a name="dfs-server-target-prioritization"></a>Définition de la priorité cible du serveur DFS

La définition de priorités de serveur DFS est une fonctionnalité disponible dans Microsoft Windows Server 2003 avec Service Pack 1 (SP1) et les systèmes d’exploitation ultérieurs. Cette fonctionnalité permet aux serveurs DFS de tirer parti des informations de coût de site Active Directory disponibles pour hiérarchiser les cibles dans les références des clients.

Avant Windows Server 2003 avec SP1, les cibles étaient regroupées en deux ensembles : un groupe pour contenir toutes les cibles dans le même site que le client. et un autre groupe pour toutes les autres cibles. Ces cibles partageant le même site que le client sont appelées « dans le site » et si le coût des sites est activé, un coût spécifique est attribué à chaque site, avec des coûts de site inférieurs par rapport à ceux d’une valeur supérieure.

Avec la disponibilité de ces données de coût de site, les cibles de serveur peuvent être classées par ordre de priorité pour des stratégies de basculement de serveur DFS plus efficaces. Dans le passé, ce niveau granulaire de détails n’était pas disponible et les administrateurs devaient recourir à des moyens artificiels (tels que des sites factices dans Active Directory) pour prendre en charge des exigences encore plus simples, telles que la désignation de serveurs spécifiques en tant que serveur de « sauvegarde » ou « secondaire » dans le cas où un serveur DFS « principal » échoue. Désormais, avec les détails supplémentaires fournis par les stratégies de basculement de site, des stratégies de basculement à plusieurs niveaux sont possibles.

La discussion suivante suppose que le coût des sites est activé.

## <a name="target-prioritization"></a>Priorité cible

La priorité cible est un ordre spécifique du point de vue administratif, la classification et le classement des serveurs sur site en termes de préférences explicites en fonction du coût de leur site à partir d’un client DFS. La priorité globale est indépendante du coût du site. Notez que les classes de priorité globale n’indiquent pas nécessairement les cibles les plus optimales du point de vue d’un client DFS, mais reflètent plutôt l’importance, ou l’absence d’importance, des cibles spécifiques du point de vue d’un administrateur de site.

La priorité du serveur cible est divisée en deux catégories de valeurs : classe de priorité et rang de priorité. Les classes de priorité sont divisées en deux niveaux : local et global. Au sein de ces classes, il existe un classement approximatif des cibles en fonction du coût du site, regroupé comme élevé, normal et basse priorité. Le résultat est cinq classes de priorité, dans l’ordre de priorité la plus élevée à la plus basse, comme suit :

- Haute priorité globale
- Site-haute priorité
- Site-coût normal priorité
- Site-coût faible priorité
- Priorité basse globale

Les classes de coût de site peuvent être considérées comme des sous-divisions de la « priorité normale globale ». Le rang de priorité est un classement d’entiers simple basé sur les valeurs ordinales : 0, 1, 2 et à partir de, avec 0 étant la valeur la plus élevée et toutes les valeurs suivantes indiquant une diminution du rang.

Les priorités globales haute et basse ne tiennent pas compte des valeurs de coût de site. Les cibles avec une priorité élevée globale reçoivent une préférence sur toutes les autres cibles, et les cibles avec une priorité basse globale reçoivent le moins de préférence.

Dans le classement d’une référence, le processus complet présente les étapes suivantes :

1. Les jeux de cibles globales haute et basse sont identifiés, ainsi que les cibles « globales » restantes.
2. Si l’option « INSITE » est définie, toutes les cibles situées en dehors du site du client sont supprimées. L’option « inactive » n’est pas appliquée aux ensembles globaux haute et basse priorité.
3. Dans chacun de ces trois ensembles, les cibles sont triées à l’aide du mécanisme de coût de site Active Directory, à l’aide d’une évaluation de site locale ou complète. Le résultat est un ensemble de cibles de même coût de site.
4. Dans les ensembles de cibles globales « normal » de même coût de site, les cibles sont affectées d’une classe de priorité à partir des classements de niveau élevé, normal et basse priorité du site.
5. Dans les ensembles de cibles de la classe de priorité et de coût de site identiques, les cibles sont désormais classées par rang de priorité, 0 étant le rang le plus élevé.
6. Dans les ensembles de cibles de même coût de site, classe de priorité et rang de priorité, les cibles sont mélangées de façon aléatoire pour l’équilibrage de charge.

Graphiquement, un ensemble de cibles est ordonné comme indiqué ci-dessous :

- cibles de classe de priorité élevée globale 
- cibles de classe de niveau haute priorité site avec coût du site = 0
- normal avec coût du site = 0
- faible avec coût du site = 0
- cibles de classe de niveau haute priorité site avec coût du site = 1
- normal avec coût du site = 1
- faible avec coût du site = 1
- et ainsi de suite
- cibles de classe de priorité basse globale

Dans chacun de ces jeux, les cibles sont triées en fonction du rang de priorité. Le rang le plus élevé est égal à zéro, avec chaque valeur entière suivante (1, 2, etc.) indiquant un rang de plus en plus faible.

La priorité cible est définie sur une cible spécifique d’un lien (ou racine) dans un espace de noms DFS. La priorité d’une cible pour un lien n’influe pas sur l’ordre des autres liens si ce même chemin cible est utilisé plusieurs fois. Par exemple, si deux liens ont \\ \\ \\ un serveur Share1 en tant que cible, la priorité du \\ \\ serveur \\ Share1 est définie séparément pour les deux liens.

La priorité par défaut pour tous les liens est le niveau de priorité site-coût normal avec le rang 0. La priorité cible n’affecte pas l’ordre des références, sauf si elle est utilisée, et si tous les liens existants sont triés à mesure qu’ils sont reçus.

La réponse de référence d’un serveur DFS se compose de jeux de cibles classés comme indiqué ci-dessus, avec chaque ensemble de cibles non global contenant des cibles du même coût de site, de la classe de priorité et du rang de priorité. Les cibles dans chaque ensemble sont triées de façon aléatoire. Les clients DFS qui reçoivent la référence commencent par la première cible du premier jeu et continuent d’accéder à la liste jusqu’à ce qu’une cible disponible pour une racine ou un lien DFS donné soit trouvée.

Pour l’implémentation d’API spécifique de cette fonctionnalité, consultez les rubriques de référence suivantes :

[**DFS_INFO_6**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6) 
 [**DFS_INFO_104**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104) 
 [**DFS_INFO_106**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106) 
 [**DFS_TARGET_PRIORITY**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority) 
 [**DFS_TARGET_PRIORITY_CLASS**](/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1)
