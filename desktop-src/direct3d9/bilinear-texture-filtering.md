---
description: Les textures sont toujours traitées de manière linéaire (0,0, 0,0) dans le coin supérieur gauche pour (1,0, 1,0) dans le coin inférieur droit, comme indiqué dans l’illustration suivante.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Filtrage de texture bilinéaire (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393187"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a><span data-ttu-id="b0f95-103">Filtrage de texture bilinéaire (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0f95-103">Bilinear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="b0f95-104">Les textures sont toujours traitées de manière linéaire (0,0, 0,0) dans le coin supérieur gauche pour (1,0, 1,0) dans le coin inférieur droit, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="b0f95-104">Textures are always linearly addressed from (0.0, 0.0) at the top-left corner to (1.0, 1.0) at the bottom-right corner, as shown in the following illustration.</span></span>

![illustration de la texture 4x4 avec des blocs de couleur solides](images/bilinear-fig7a.png)

<span data-ttu-id="b0f95-106">Les textures sont généralement représentées comme si elles étaient composées de blocs de couleur solides, mais il est en fait plus approprié de considérer les textures de la même façon que l’affichage raster : chaque Texel est défini au centre exact d’une cellule de grille, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="b0f95-106">Textures are usually represented as if they were composed of solid blocks of color, but it's actually more correct to think of textures the same way you should think of the raster display: Each texel is defined at the exact center of a grid cell, as shown in the following illustration.</span></span>

![illustration de la texture 4x4 avec des texels définis au centre des cellules de la grille](images/bilinear-fig7b.png)

<span data-ttu-id="b0f95-108">Si vous demandez l’échantillonneur de texture pour la couleur de cette texture aux coordonnées UV (0,375, 0,375), vous obtenez un rouge Uni (255, 0,0).</span><span class="sxs-lookup"><span data-stu-id="b0f95-108">If you ask the texture sampler for this texture's color at UV coordinates (0.375, 0.375) you'll get solid red (255, 0, 0).</span></span> <span data-ttu-id="b0f95-109">Cela est parfait, car le centre exact de la cellule Texel rouge est UV (0,375, 0,375).</span><span class="sxs-lookup"><span data-stu-id="b0f95-109">That makes perfect sense because the exact center of the red texel cell is at UV (0.375, 0.375).</span></span> <span data-ttu-id="b0f95-110">Que se passe-t-il si vous demandez à l’échantillonneur la couleur de la texture sur UV (0,25, 0,25) ?</span><span class="sxs-lookup"><span data-stu-id="b0f95-110">What if you ask the sampler for the texture's color at UV (0.25, 0.25)?</span></span> <span data-ttu-id="b0f95-111">Ce n’est pas tout aussi simple, car le point à UV (0,25, 0,25) se trouve à l’angle exact de 4 texels.</span><span class="sxs-lookup"><span data-stu-id="b0f95-111">That's not quite as easy, because the point at UV (0.25, 0.25) lies at the exact corner of 4 texels.</span></span>

<span data-ttu-id="b0f95-112">Le schéma le plus simple consiste simplement à faire en sorte que l’échantillonneur retourne la couleur de la Texel la plus proche. C’est ce que l’on appelle le filtrage des points (voir [échantillonnage à point le plus proche (Direct3D 9)](nearest-point-sampling.md)) et qui est généralement indésirable en raison des résultats de granularité ou de blocage.</span><span class="sxs-lookup"><span data-stu-id="b0f95-112">The simplest scheme is simply to have the sampler return the color of the closest texel; this is called Point filtering (see [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md)), and is usually undesirable due to grainy or blocky results.</span></span> <span data-ttu-id="b0f95-113">L’échantillonnage par pointage de notre texture à l’UV (0,25, 0,25) illustre un autre problème subtil avec le filtrage de point le plus proche : il y a quatre texels équidistants à partir du point d’échantillonnage. il n’y a donc pas de Texel unique le plus proche.</span><span class="sxs-lookup"><span data-stu-id="b0f95-113">Point-sampling our texture at UV (0.25, 0.25) shows another subtle problem with nearest-point filtering: there are four texels equidistant from the sampling point, so there's no single nearest texel.</span></span> <span data-ttu-id="b0f95-114">L’un de ces quatre texels est choisi comme couleur renvoyée, mais la sélection dépend de la manière dont la coordonnée est arrondie, ce qui peut introduire des artefacts de déchirement (consultez l’article Nearest-Point d’échantillonnage dans le kit de développement logiciel (SDK)).</span><span class="sxs-lookup"><span data-stu-id="b0f95-114">One of those four texels will be chosen as the returned color, but the selection depends on how the coordinate is rounded, which may introduce tearing artifacts (see the Nearest-Point Sampling article in the SDK).</span></span>

<span data-ttu-id="b0f95-115">Un schéma de filtrage légèrement plus précis et plus courant consiste à calculer la moyenne pondérée des 4 texels les plus proches du point d’échantillonnage ; C’est ce que l’on appelle le filtrage bilinéaire et le coût de calcul supplémentaire est généralement négligeable, car cette routine est implémentée dans le matériel graphique moderne.</span><span class="sxs-lookup"><span data-stu-id="b0f95-115">A slightly more accurate and more common filtering scheme is to calculate the weighted average of the 4 texels closest to the sampling point; this is called Bilinear filtering, and the extra computational cost is usually negligible because this routine is implemented in modern graphics hardware.</span></span> <span data-ttu-id="b0f95-116">Voici les couleurs que nous obtenons à quelques points d’échantillonnage différents en utilisant le filtrage bilinéaire :</span><span class="sxs-lookup"><span data-stu-id="b0f95-116">Here are the colors we get at a few different sample points using bilinear filtering:</span></span>


```
UV: (0.5, 0.5)
```



<span data-ttu-id="b0f95-117">Ce point se trouve à la bordure exacte entre les texels rouge, vert, bleu et blanc.</span><span class="sxs-lookup"><span data-stu-id="b0f95-117">This point is at the exact border between red, green, blue, and white texels.</span></span> <span data-ttu-id="b0f95-118">La couleur renvoyée par l’échantillonneur est grise :</span><span class="sxs-lookup"><span data-stu-id="b0f95-118">The color the sampler returns is gray:</span></span>


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



<span data-ttu-id="b0f95-119">Ce point se trouve au milieu de la bordure entre les texels rouges et verts.</span><span class="sxs-lookup"><span data-stu-id="b0f95-119">This point is at the midpoint of the border between red and green texels.</span></span> <span data-ttu-id="b0f95-120">La couleur renvoyée par l’échantillonneur est jaune-gris (Notez que les contributions des texels bleu et blanc sont mises à l’échelle sur 0) :</span><span class="sxs-lookup"><span data-stu-id="b0f95-120">The color the sampler returns is yellow-gray (note that the contributions of the blue and white texels are scaled to 0):</span></span>


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



<span data-ttu-id="b0f95-121">Il s’agit de l’adresse du Texel rouge, qui est la couleur retournée (toutes les autres textures dans le calcul de filtrage sont pondérées à 0) :</span><span class="sxs-lookup"><span data-stu-id="b0f95-121">This is the address of the red texel, which is the returned color (all other texels in the filtering calculation are weighted to 0):</span></span>


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



<span data-ttu-id="b0f95-122">Comparez ces calculs à l’illustration suivante, qui montre ce qui se passe si le calcul de filtrage bilinéaire est effectué à chaque adresse de texture à travers la texture 4x4.</span><span class="sxs-lookup"><span data-stu-id="b0f95-122">Compare these calculations against the following illustration, which shows what happens if the bilinear filtering calculation is performed at every texture address across the 4x4 texture.</span></span>

![illustration de la texture 4x4 avec Filtrage bilinéaire effectué à chaque adresse de texture](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a><span data-ttu-id="b0f95-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0f95-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f95-125">Filtrage de texture</span><span class="sxs-lookup"><span data-stu-id="b0f95-125">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 



