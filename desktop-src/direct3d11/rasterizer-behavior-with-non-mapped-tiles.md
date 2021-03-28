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
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a><span data-ttu-id="3045e-103">Comportement du rastériseur avec les vignettes non mappées</span><span class="sxs-lookup"><span data-stu-id="3045e-103">Rasterizer behavior with non-mapped tiles</span></span>

<span data-ttu-id="3045e-104">Cette section décrit le comportement du rastériseur avec les vignettes non mappées.</span><span class="sxs-lookup"><span data-stu-id="3045e-104">This section describes rasterizer behavior with non-mapped tiles.</span></span>

## <a name="depthstencilview"></a><span data-ttu-id="3045e-105">DepthStencilView</span><span class="sxs-lookup"><span data-stu-id="3045e-105">DepthStencilView</span></span>

<span data-ttu-id="3045e-106">Le comportement des lectures et écritures de vue stencil (DSV) dépend du niveau de support matériel.</span><span class="sxs-lookup"><span data-stu-id="3045e-106">Behavior of depth stencil view (DSV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="3045e-107">Pour une répartition des spécifications, consultez comportement global en lecture et en écriture pour les [niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="3045e-107">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="3045e-108">Voici le comportement idéal :</span><span class="sxs-lookup"><span data-stu-id="3045e-108">Here is the ideal behavior:</span></span>

<span data-ttu-id="3045e-109">Si une vignette n’est pas mappée dans DepthStencilView, la valeur de retour de la profondeur de lecture est 0, qui est ensuite alimentée dans toutes les opérations configurées pour la valeur de lecture de profondeur.</span><span class="sxs-lookup"><span data-stu-id="3045e-109">If a tile isn't mapped in the DepthStencilView, the return value from reading depth is 0, which is then fed into whatever operations are configured for the depth read value.</span></span> <span data-ttu-id="3045e-110">Les écritures dans la vignette de profondeur manquante sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="3045e-110">Writes to the missing depth tile are dropped.</span></span> <span data-ttu-id="3045e-111">Cette définition idéale pour la gestion des écritures n’est pas requise par le [niveau 2](tier-2.md). les écritures dans des vignettes non mappées peuvent se trouver dans un cache que les lectures suivantes pourraient récupérer.</span><span class="sxs-lookup"><span data-stu-id="3045e-111">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="rendertargetview"></a><span data-ttu-id="3045e-112">RenderTargetView</span><span class="sxs-lookup"><span data-stu-id="3045e-112">RenderTargetView</span></span>

<span data-ttu-id="3045e-113">Le comportement des lectures et des écritures de la vue de la cible de rendu dépend du niveau de support matériel.</span><span class="sxs-lookup"><span data-stu-id="3045e-113">Behavior of render target view (RTV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="3045e-114">Pour une répartition des spécifications, consultez comportement global en lecture et en écriture pour les [niveaux de fonctionnalités des ressources en mosaïque](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="3045e-114">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="3045e-115">Sur toutes les implémentations, différentes limites de RTVs (et de DSV) peuvent avoir des zones mappées et non mappées différentes et peuvent avoir des formats de surface de taille différents (ce qui signifie des formes de mosaïques différentes).</span><span class="sxs-lookup"><span data-stu-id="3045e-115">On all implementations, different RTVs (and DSV) bound simultaneously can have different areas mapped versus non-mapped and can have different sized surface formats (which means different tile shapes).</span></span>

<span data-ttu-id="3045e-116">Voici le comportement idéal :</span><span class="sxs-lookup"><span data-stu-id="3045e-116">Here is the ideal behavior:</span></span>

<span data-ttu-id="3045e-117">Les lectures à partir de RTVs retournent 0 dans les vignettes et les écritures manquantes sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="3045e-117">Reads from RTVs return 0 in missing tiles and writes are dropped.</span></span> <span data-ttu-id="3045e-118">Cette définition idéale pour la gestion des écritures n’est pas requise par le [niveau 2](tier-2.md). les écritures dans des vignettes non mappées peuvent se trouver dans un cache que les lectures suivantes pourraient récupérer.</span><span class="sxs-lookup"><span data-stu-id="3045e-118">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3045e-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3045e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3045e-120">Accès du pipeline aux ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="3045e-120">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




