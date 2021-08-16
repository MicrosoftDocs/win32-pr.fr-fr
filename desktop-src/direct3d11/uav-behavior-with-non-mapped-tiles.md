---
title: Comportement de l’UAV avec les vignettes non mappées
description: Le comportement des lectures et écritures de la vue d’accès non triée (UAV) dépend du niveau de support matériel.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed676403e5eb1fdc838ac080b8be530b5004e6734fedc5674664f4d75304ee37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857659"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a>Comportement de l’UAV avec les vignettes non mappées

Le comportement des lectures et écritures de la vue d’accès non triée (UAV) dépend du niveau de support matériel. Pour une répartition des spécifications, consultez comportement global en lecture et en écriture pour les [niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md). Cette section résume le comportement idéal.

Les opérations de nuanceur qui lisent à partir d’une vignette non mappée dans un UAV retournent 0 dans tous les composants non manquants du format, et la valeur par défaut pour les composants manquants.

Les opérations de nuanceur qui tentent d’écrire sur une vignette non mappée n’entraînent pas l’écriture dans la zone non mappée (alors que les écritures dans une zone mappée se poursuivent). Cette définition idéale pour la gestion des écritures n’est pas requise par le [niveau 2](tier-2.md). les écritures dans des vignettes non mappées peuvent se trouver dans un cache que les lectures suivantes pourraient récupérer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès du pipeline aux ressources en mosaïque](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




