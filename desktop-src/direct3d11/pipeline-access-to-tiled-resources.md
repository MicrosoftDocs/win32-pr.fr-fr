---
title: Accès du pipeline aux ressources en mosaïque
description: Les ressources en mosaïque peuvent être utilisées dans les vues de ressource de nuanceur (SRV), les affichages de cible de rendu (RTV), les vues de stencil de profondeur (DSV) et les vues d’accès non ordonnées (UAV), ainsi que certains points de liaison où les vues ne sont pas utilisées, telles que les liaisons de mémoire tampon de vertex.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729253"
---
# <a name="pipeline-access-to-tiled-resources"></a><span data-ttu-id="eeb5d-103">Accès du pipeline aux ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="eeb5d-103">Pipeline access to tiled resources</span></span>

<span data-ttu-id="eeb5d-104">Les ressources en mosaïque peuvent être utilisées dans les vues de ressource de nuanceur (SRV), les affichages de cible de rendu (RTV), les vues de stencil de profondeur (DSV) et les vues d’accès non ordonnées (UAV), ainsi que certains points de liaison où les vues ne sont pas utilisées, telles que les liaisons de mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-104">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <span data-ttu-id="eeb5d-105">Pour obtenir la liste des liaisons prises en charge, consultez [paramètres de création de ressources en mosaïque](tiled-resource-creation-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eeb5d-105">For the list of supported bindings, see [Tiled resource creation parameters](tiled-resource-creation-parameters.md).</span></span> <span data-ttu-id="eeb5d-106">Les \* opérations de copie fonctionnent également sur les ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-106">Copy\* operations also work on tiled resources.</span></span>

<span data-ttu-id="eeb5d-107">Si plusieurs coordonnées de mosaïque dans une ou plusieurs vues sont liées au même emplacement de mémoire, les lectures et écritures à partir de différents chemins d’accès à la même mémoire se produisent dans un ordre non déterministe et non reproductible d’accès à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-107">If multiple tile coordinates in one or more views is bound to the same memory location, reads and writes from different paths to the same memory will occur in a non-deterministic and non-repeatable order of memory accesses.</span></span>

<span data-ttu-id="eeb5d-108">Si toutes les vignettes derrière un encombrement d’accès à la mémoire à partir d’un nuanceur sont mappées à des vignettes uniques, le comportement est identique sur toutes les implémentations à la surface ayant le même contenu de mémoire en mode non en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-108">If all tiles behind a memory access footprint from a shader are mapped to unique tiles, behavior is identical on all implementations to the surface having the same memory contents in a non-tiled fashion.</span></span>

<span data-ttu-id="eeb5d-109">Cette section fournit plus d’informations sur l’accès du pipeline aux ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-109">This section provides more info about pipeline access to tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eeb5d-110">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="eeb5d-110">In this section</span></span>



| <span data-ttu-id="eeb5d-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="eeb5d-111">Topic</span></span>                                                                                                              | <span data-ttu-id="eeb5d-112">Description</span><span class="sxs-lookup"><span data-stu-id="eeb5d-112">Description</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eeb5d-113">Comportement du SRV avec les vignettes non mappées</span><span class="sxs-lookup"><span data-stu-id="eeb5d-113">SRV behavior with non-mapped tiles</span></span>](srv-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="eeb5d-114">Le comportement des lectures de la vue de ressource de nuanceur (SRV) qui impliquent des vignettes non mappées dépend du niveau de support matériel.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-114">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <br/>                                          |
| [<span data-ttu-id="eeb5d-115">Comportement de l’UAV avec les vignettes non mappées</span><span class="sxs-lookup"><span data-stu-id="eeb5d-115">UAV behavior with non-mapped tiles</span></span>](uav-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="eeb5d-116">Le comportement des lectures et écritures de la vue d’accès non triée (UAV) dépend du niveau de support matériel.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-116">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <br/>                                                            |
| [<span data-ttu-id="eeb5d-117">Comportement du rastériseur avec les vignettes non mappées</span><span class="sxs-lookup"><span data-stu-id="eeb5d-117">Rasterizer behavior with non-mapped tiles</span></span>](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | <span data-ttu-id="eeb5d-118">Cette section décrit le comportement du rastériseur avec les vignettes non mappées.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-118">This section describes rasterizer behavior with non-mapped tiles.</span></span><br/>                                                                                              |
| [<span data-ttu-id="eeb5d-119">Restrictions d’accès aux vignettes avec des mappages en double</span><span class="sxs-lookup"><span data-stu-id="eeb5d-119">Tile access limitations with duplicate mappings</span></span>](tile-access-limitations-with-duplicate-mappings-.md)<br/> | <span data-ttu-id="eeb5d-120">Cette section décrit les limitations d’accès aux vignettes avec des mappages en double.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-120">This section describes tile access limitations with duplicate mappings.</span></span><br/>                                                                                        |
| [<span data-ttu-id="eeb5d-121">Fonctionnalités d’échantillonnage de texture des ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="eeb5d-121">Tiled resources texture sampling features</span></span>](tiled-resources-texture-sampling-features.md)<br/>              | <span data-ttu-id="eeb5d-122">Cette section décrit les fonctionnalités d’échantillonnage de texture des ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="eeb5d-122">This section describes tiled resources texture sampling features.</span></span><br/>                                                                                              |
| [<span data-ttu-id="eeb5d-123">Exposition des ressources en mosaïque HLSL</span><span class="sxs-lookup"><span data-stu-id="eeb5d-123">HLSL tiled resources exposure</span></span>](hlsl-tiled-resources-exposure.md)<br/>                                      | <span data-ttu-id="eeb5d-124">La nouvelle syntaxe HLSL (High Level Shader Language) de Microsoft est requise pour prendre en charge les ressources en mosaïque dans le [nuancier Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span><span class="sxs-lookup"><span data-stu-id="eeb5d-124">New Microsoft High Level Shader Language (HLSL) syntax is required to support tiled resources in [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="eeb5d-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eeb5d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb5d-126">Ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="eeb5d-126">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

