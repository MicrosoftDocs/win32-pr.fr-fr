---
title: Comportement du SRV avec les vignettes non mappées
description: Le comportement des lectures de la vue de ressource de nuanceur (SRV) qui impliquent des vignettes non mappées dépend du niveau de support matériel.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190724"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a><span data-ttu-id="654fb-103">Comportement du SRV avec les vignettes non mappées</span><span class="sxs-lookup"><span data-stu-id="654fb-103">SRV behavior with non-mapped tiles</span></span>

<span data-ttu-id="654fb-104">Le comportement des lectures de la vue de ressource de nuanceur (SRV) qui impliquent des vignettes non mappées dépend du niveau de support matériel.</span><span class="sxs-lookup"><span data-stu-id="654fb-104">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <span data-ttu-id="654fb-105">Pour une répartition des spécifications, consultez comportement de lecture pour les [niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="654fb-105">For a breakdown of requirements, see read behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="654fb-106">Cette section résume le comportement idéal, qui est requis par le [niveau 2](tier-2.md) .</span><span class="sxs-lookup"><span data-stu-id="654fb-106">This section summarizes the ideal behavior, which [Tier 2](tier-2.md) requires.</span></span>

<span data-ttu-id="654fb-107">Prenons l’exemple d’une opération de filtre de texture qui lit à partir d’un jeu de texels dans un SRV.</span><span class="sxs-lookup"><span data-stu-id="654fb-107">Consider a texture filter operation that reads from a set of texels in an SRV.</span></span> <span data-ttu-id="654fb-108">Les texels qui se trouvent sur des vignettes non mappées contribuent à 0 dans tous les composants non manquants du format (et à la valeur par défaut pour les composants manquants) dans l’opération de filtre globale, avec les contributions des texels mappés.</span><span class="sxs-lookup"><span data-stu-id="654fb-108">Texels that fall on non-mapped tiles contribute 0 in all non-missing components of the format (and the default for missing components) into the overall filter operation alongside contributions from mapped texels.</span></span> <span data-ttu-id="654fb-109">Les texels sont tous pondérés et combinés indépendamment du fait que les données proviennent de vignettes mappées ou non mappées.</span><span class="sxs-lookup"><span data-stu-id="654fb-109">The texels are all weighted and combined together independent of whether the data came from mapped or non-mapped tiles.</span></span>

<span data-ttu-id="654fb-110">Un matériel de niveau [2](tier-2.md) de premier niveau de génération ne répond pas à cette exigence de spécification et retourne le 0 avec les valeurs par défaut décrites ci-dessus comme résultat de filtre global si des texels (avec une pondération différente de zéro) tombent sur des vignettes non mappées.</span><span class="sxs-lookup"><span data-stu-id="654fb-110">Some first generation [Tier 2](tier-2.md) level hardware does not meet this spec requirement and returns the 0 with defaults described preceding as the overall filter result if any texels (with nonzero weight) fall on non-mapped tiles.</span></span> <span data-ttu-id="654fb-111">Aucun autre matériel ne sera autorisé à manquer l’obligation d’inclure tous les texels (pondération différente de zéro) dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="654fb-111">No other hardware will be allowed to miss the requirement to include all (nonzero weight) texels in the filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="654fb-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="654fb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="654fb-113">Accès du pipeline aux ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="654fb-113">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




