---
title: Comportement du SRV avec les vignettes non mappées
description: Le comportement des lectures de la vue de ressource de nuanceur (SRV) qui impliquent des vignettes non mappées dépend du niveau de support matériel.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edb1dd6e291fb1bdeb691349a74b8483773cf3fbb5a49fb2ee1a5e950fab452
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850869"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a>Comportement du SRV avec les vignettes non mappées

Le comportement des lectures de la vue de ressource de nuanceur (SRV) qui impliquent des vignettes non mappées dépend du niveau de support matériel. Pour une répartition des spécifications, consultez comportement de lecture pour les [niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md). Cette section résume le comportement idéal, qui est requis par le [niveau 2](tier-2.md) .

Prenons l’exemple d’une opération de filtre de texture qui lit à partir d’un jeu de texels dans un SRV. Les texels qui se trouvent sur des vignettes non mappées contribuent à 0 dans tous les composants non manquants du format (et à la valeur par défaut pour les composants manquants) dans l’opération de filtre globale, avec les contributions des texels mappés. Les texels sont tous pondérés et combinés indépendamment du fait que les données proviennent de vignettes mappées ou non mappées.

Un matériel de niveau [2](tier-2.md) de premier niveau de génération ne répond pas à cette exigence de spécification et retourne le 0 avec les valeurs par défaut décrites ci-dessus comme résultat de filtre global si des texels (avec une pondération différente de zéro) tombent sur des vignettes non mappées. Aucun autre matériel ne sera autorisé à manquer l’obligation d’inclure tous les texels (pondération différente de zéro) dans le filtre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès du pipeline aux ressources en mosaïque](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




