---
title: Comportement de l’UAV avec les vignettes non mappées
description: Le comportement des lectures et écritures de la vue d’accès non triée (UAV) dépend du niveau de support matériel.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939717"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a><span data-ttu-id="c4f7a-103">Comportement de l’UAV avec les vignettes non mappées</span><span class="sxs-lookup"><span data-stu-id="c4f7a-103">UAV behavior with non-mapped tiles</span></span>

<span data-ttu-id="c4f7a-104">Le comportement des lectures et écritures de la vue d’accès non triée (UAV) dépend du niveau de support matériel.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-104">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="c4f7a-105">Pour une répartition des spécifications, consultez comportement global en lecture et en écriture pour les [niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="c4f7a-105">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="c4f7a-106">Cette section résume le comportement idéal.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-106">This section summarizes the ideal behavior.</span></span>

<span data-ttu-id="c4f7a-107">Les opérations de nuanceur qui lisent à partir d’une vignette non mappée dans un UAV retournent 0 dans tous les composants non manquants du format, et la valeur par défaut pour les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-107">Shader operations that read from a non-mapped tile in a UAV return 0 in all non-missing components of the format, and the default for missing components.</span></span>

<span data-ttu-id="c4f7a-108">Les opérations de nuanceur qui tentent d’écrire sur une vignette non mappée n’entraînent pas l’écriture dans la zone non mappée (alors que les écritures dans une zone mappée se poursuivent).</span><span class="sxs-lookup"><span data-stu-id="c4f7a-108">Shader operations that attempt to write to a non-mapped tile cause nothing to be written to the non-mapped area (while writes to a mapped area proceed).</span></span> <span data-ttu-id="c4f7a-109">Cette définition idéale pour la gestion des écritures n’est pas requise par le [niveau 2](tier-2.md). les écritures dans des vignettes non mappées peuvent se trouver dans un cache que les lectures suivantes pourraient récupérer.</span><span class="sxs-lookup"><span data-stu-id="c4f7a-109">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4f7a-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4f7a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4f7a-111">Accès du pipeline aux ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="c4f7a-111">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




