---
title: Étape du rastériseur
description: L’étape de pixellisation convertit les informations vectorielles (composées de formes ou de Primitives) en une image raster (composée de pixels) pour l’affichage de graphiques 3D en temps réel.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941498"
---
# <a name="rasterizer-stage"></a><span data-ttu-id="a326c-103">Étape du rastériseur</span><span class="sxs-lookup"><span data-stu-id="a326c-103">Rasterizer Stage</span></span>

<span data-ttu-id="a326c-104">L’étape de pixellisation convertit les informations vectorielles (composées de formes ou de Primitives) en une image raster (composée de pixels) pour l’affichage de graphiques 3D en temps réel.</span><span class="sxs-lookup"><span data-stu-id="a326c-104">The rasterization stage converts vector information (composed of shapes or primitives) into a raster image (composed of pixels) for the purpose of displaying real-time 3D graphics.</span></span>

<span data-ttu-id="a326c-105">Pendant la pixellisation, chaque primitive est convertie en pixels, tout en interpolant les valeurs par vertex sur chaque primitive.</span><span class="sxs-lookup"><span data-stu-id="a326c-105">During rasterization, each primitive is converted into pixels, while interpolating per-vertex values across each primitive.</span></span> <span data-ttu-id="a326c-106">La pixellisation comprend des sommets de découpage pour la vue frustum, en effectuant une division par z pour fournir une perspective, en mappant les primitives à une fenêtre d’affichage 2D et en déterminant comment appeler le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="a326c-106">Rasterization includes clipping vertices to the view frustum, performing a divide by z to provide perspective, mapping primitives to a 2D viewport, and determining how to invoke the pixel shader.</span></span> <span data-ttu-id="a326c-107">Bien que l’utilisation d’un nuanceur de pixels soit facultative, l’étape de rastérisation effectue toujours le découpage, une division de perspective pour transformer les points en un espace homogène et mappe les vertex à la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a326c-107">While using a pixel shader is optional, the rasterizer stage always performs clipping, a perspective divide to transform the points into homogeneous space, and maps the vertices to the viewport.</span></span>

<span data-ttu-id="a326c-108">Les sommets (x, y, z, w), arrivant à l’étape de rastérisation, sont supposés être dans l’espace de clip homogène.</span><span class="sxs-lookup"><span data-stu-id="a326c-108">Vertices (x,y,z,w), coming into the rasterizer stage are assumed to be in homogeneous clip-space.</span></span> <span data-ttu-id="a326c-109">Dans cet espace de coordonnées, les points de l’axe X sont à droite, Y pointe vers le haut et Z points loin de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="a326c-109">In this coordinate space the X axis points right, Y points up and Z points away from camera.</span></span>

<span data-ttu-id="a326c-110">Vous pouvez désactiver la pixellisation en indiquant au pipeline qu’il n’existe aucun nuanceur de pixels (définissez l’étape nuanceur de pixels sur **null** avec [**ID3D11DeviceContext ::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) et désactivez les tests de profondeur et de stencil (définissez **DepthEnable** et **StencilEnable** sur **false** dans le [**stencil de profondeur d3d11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span><span class="sxs-lookup"><span data-stu-id="a326c-110">You may disable rasterization by telling the pipeline there is no pixel shader (set the pixel shader stage to **NULL** with [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)), and disabling depth and stencil testing (set **DepthEnable** and **StencilEnable** to **FALSE** in [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span> <span data-ttu-id="a326c-111">Quand la rastérisation est désactivée, les compteurs du pipeline relatif à la rastérisation ne sont pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="a326c-111">While disabled, rasterization-related pipeline counters will not update.</span></span> <span data-ttu-id="a326c-112">Il existe également une description complète des [règles de pixellisation](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span><span class="sxs-lookup"><span data-stu-id="a326c-112">There is also a complete description of the [rasterization rules](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span></span>

<span data-ttu-id="a326c-113">Sur le matériel qui implémente des optimisations hiérarchiques de la mémoire tampon Z, vous pouvez activer le préchargement de la mémoire tampon z en affectant à l’étape nuanceur de pixels la **valeur null** tout en activant le test de profondeur et de stencil.</span><span class="sxs-lookup"><span data-stu-id="a326c-113">On hardware that implements hierarchical Z-buffer optimizations, you may enable preloading the z-buffer by setting the pixel shader stage to **NULL** while enabling depth and stencil testing.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="a326c-114">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="a326c-114">In this section</span></span>



| <span data-ttu-id="a326c-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a326c-115">Topic</span></span>                                                                                                                         | <span data-ttu-id="a326c-116">Description</span><span class="sxs-lookup"><span data-stu-id="a326c-116">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a326c-117">Prise en main avec l’étape de rastérisation</span><span class="sxs-lookup"><span data-stu-id="a326c-117">Getting Started with the Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | <span data-ttu-id="a326c-118">Cette section décrit la définition de la fenêtre d’affichage, du rectangle de ciseaux, de l’état du rastériseur et de l’échantillonnage multiple.</span><span class="sxs-lookup"><span data-stu-id="a326c-118">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="a326c-119">Règles de pixellisation</span><span class="sxs-lookup"><span data-stu-id="a326c-119">Rasterization Rules</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | <span data-ttu-id="a326c-120">Les règles de pixellisation définissent la façon dont les données vectorielles sont mappées dans les données raster.</span><span class="sxs-lookup"><span data-stu-id="a326c-120">Rasterization rules define how vector data is mapped into raster data.</span></span> <span data-ttu-id="a326c-121">Les données raster sont alignées sur les emplacements d’entiers qui sont ensuite éliminés et découpés (pour dessiner le nombre minimal de pixels), et les attributs par pixel sont interpolés (à partir des attributs par vertex) avant d’être passés à un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="a326c-121">The raster data is snapped to integer locations that are then culled and clipped (to draw the minimum number of pixels), and per-pixel attributes are interpolated (from per-vertex attributes) before being passed to a pixel shader.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a326c-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a326c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a326c-123">Pipeline graphique</span><span class="sxs-lookup"><span data-stu-id="a326c-123">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="a326c-124">Étapes de pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a326c-124">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

