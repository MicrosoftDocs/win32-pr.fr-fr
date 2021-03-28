---
title: Comportement du rastériseur avec les vignettes non mappées
description: Cette section décrit le comportement du rastériseur avec les vignettes non mappées.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990629"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a>Comportement du rastériseur avec les vignettes non mappées

Cette section décrit le comportement du rastériseur avec les vignettes non mappées.

## <a name="depthstencilview"></a>DepthStencilView

Le comportement des lectures et écritures de vue stencil (DSV) dépend du niveau de support matériel. Pour une répartition des spécifications, consultez comportement global en lecture et en écriture pour les [niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md).

Voici le comportement idéal :

Si une vignette n’est pas mappée dans DepthStencilView, la valeur de retour de la profondeur de lecture est 0, qui est ensuite alimentée dans toutes les opérations configurées pour la valeur de lecture de profondeur. Les écritures dans la vignette de profondeur manquante sont supprimées. Cette définition idéale pour la gestion des écritures n’est pas requise par le [niveau 2](tier-2.md). les écritures dans des vignettes non mappées peuvent se trouver dans un cache que les lectures suivantes pourraient récupérer.

## <a name="rendertargetview"></a>RenderTargetView

Le comportement des lectures et des écritures de la vue de la cible de rendu dépend du niveau de support matériel. Pour une répartition des spécifications, consultez comportement global en lecture et en écriture pour les [niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md).

Sur toutes les implémentations, différentes limites de RTVs (et de DSV) peuvent avoir des zones mappées et non mappées différentes et peuvent avoir des formats de surface de taille différents (ce qui signifie des formes de mosaïques différentes).

Voici le comportement idéal :

Les lectures à partir de RTVs retournent 0 dans les vignettes et les écritures manquantes sont supprimées. Cette définition idéale pour la gestion des écritures n’est pas requise par le [niveau 2](tier-2.md). les écritures dans des vignettes non mappées peuvent se trouver dans un cache que les lectures suivantes pourraient récupérer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès du pipeline aux ressources en mosaïque](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




