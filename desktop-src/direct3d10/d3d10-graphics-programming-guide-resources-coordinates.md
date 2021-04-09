---
description: Les systèmes de coordonnées pour Direct3D 10 sont définis pour les pixels et les texels.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Systèmes de coordonnées (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748972"
---
# <a name="coordinate-systems-direct3d-10"></a><span data-ttu-id="b941e-103">Systèmes de coordonnées (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b941e-103">Coordinate Systems (Direct3D 10)</span></span>

<span data-ttu-id="b941e-104">Les systèmes de coordonnées pour Direct3D 10 sont définis pour les pixels et les texels.</span><span class="sxs-lookup"><span data-stu-id="b941e-104">Coordinate systems for Direct3D 10 are defined for pixels and texels.</span></span>



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b941e-105">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="b941e-105">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="b941e-106">Direct3D 10 définit le coin supérieur gauche du pixel supérieur gauche comme l’origine d’une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="b941e-106">Direct3D 10 defines the upper-left corner of the upper-left pixel as the origin of a render target.</span></span><br/> <span data-ttu-id="b941e-107">Direct3D 9 définit le centre du pixel supérieur gauche comme l’origine d’une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="b941e-107">Direct3D 9 defines the center of the upper-left pixel as the origin of a render target.</span></span><br/> |



 

-   [<span data-ttu-id="b941e-108">Système de coordonnées de pixels</span><span class="sxs-lookup"><span data-stu-id="b941e-108">Pixel Coordinate System</span></span>](#pixel-coordinate-system)
    -   [<span data-ttu-id="b941e-109">Système de coordonnées en pixels pour Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="b941e-109">Pixel Coordinate System for Direct3D 9</span></span>](#pixel-coordinate-system-for-direct3d-9)
-   [<span data-ttu-id="b941e-110">Système de coordonnées Texel</span><span class="sxs-lookup"><span data-stu-id="b941e-110">Texel Coordinate System</span></span>](#texel-coordinate-system)
    -   [<span data-ttu-id="b941e-111">Système de coordonnées Texel</span><span class="sxs-lookup"><span data-stu-id="b941e-111">Texel Coordinate System</span></span>](#texel-coordinate-system)
-   [<span data-ttu-id="b941e-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b941e-112">Related topics</span></span>](#related-topics)

## <a name="pixel-coordinate-system"></a><span data-ttu-id="b941e-113">Système de coordonnées de pixels</span><span class="sxs-lookup"><span data-stu-id="b941e-113">Pixel Coordinate System</span></span>

<span data-ttu-id="b941e-114">Le système de coordonnées en pixels dans Direct3D 10 définit l’origine d’une cible de rendu dans l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="b941e-114">The pixel coordinate system in Direct3D 10 defines the origin of a render target at the upper-left corner.</span></span> <span data-ttu-id="b941e-115">comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b941e-115">as shown in the following diagram.</span></span> <span data-ttu-id="b941e-116">Les centres de pixels sont décalés de (0,5 f, 0,5 f) à partir des emplacements d’entiers.</span><span class="sxs-lookup"><span data-stu-id="b941e-116">Pixel centers are offset by (0.5f,0.5f) from integer locations.</span></span>

![diagramme du système de coordonnées en pixels dans Direct3D 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a><span data-ttu-id="b941e-118">Système de coordonnées en pixels pour Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="b941e-118">Pixel Coordinate System for Direct3D 9</span></span>

<span data-ttu-id="b941e-119">Pour référence, voici le système de coordonnées en pixels pour Direct3D 9, qui a défini l’origine ou une cible de rendu en tant que centre du pixel supérieur gauche, (0.5, 0.5) en dehors de l’angle supérieur gauche, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b941e-119">For reference, here is the pixel coordinate system for Direct3D 9, which defined the origin or a render target as the center of the upper-left pixel, (0.5,0.5) away from the upper left corner, as shown in the following diagram.</span></span> <span data-ttu-id="b941e-120">Dans Direct3D 9, les centres de pixels sont à des emplacements entiers.</span><span class="sxs-lookup"><span data-stu-id="b941e-120">In Direct3D 9, pixel centers are at integer locations.</span></span>

![diagramme du système de coordonnées en pixels dans Direct3D 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a><span data-ttu-id="b941e-122">Système de coordonnées Texel</span><span class="sxs-lookup"><span data-stu-id="b941e-122">Texel Coordinate System</span></span>

<span data-ttu-id="b941e-123">Le système de coordonnées Texel a son origine dans l’angle supérieur gauche de la texture, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b941e-123">The texel coordinate system has its origin at the top-left corner of the texture, as shown in the following diagram.</span></span> <span data-ttu-id="b941e-124">Cela rend le rendu des textures alignées à l’écran trivial (dans Direct3D 10), car le système de coordonnées de pixels est aligné avec le système de coordonnées Texel.</span><span class="sxs-lookup"><span data-stu-id="b941e-124">This makes rendering screen-aligned textures trivial (in Direct3D 10), as the pixel coordinate system is aligned with the texel coordinate system.</span></span>

![diagramme du système de coordonnées texels](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a><span data-ttu-id="b941e-126">Système de coordonnées Texel</span><span class="sxs-lookup"><span data-stu-id="b941e-126">Texel Coordinate System</span></span>

<span data-ttu-id="b941e-127">Les coordonnées de texture sont représentées par un nombre normalisé ou à l’échelle ; chaque coordonnée de texture est mappée à un Texel spécifique comme suit :</span><span class="sxs-lookup"><span data-stu-id="b941e-127">Texture coordinates are represented with either a normalized or a scaled number; each texture coordinate is mapped to a specific texel as follows:</span></span>

<span data-ttu-id="b941e-128">Pour une coordonnée normalisée :</span><span class="sxs-lookup"><span data-stu-id="b941e-128">For a normalized coordinate:</span></span>

-   <span data-ttu-id="b941e-129">Échantillonnage de point : Texel \# = Floor ( \* largeur U)</span><span class="sxs-lookup"><span data-stu-id="b941e-129">Point sampling: Texel \# = floor(U \* Width)</span></span>
-   <span data-ttu-id="b941e-130">Échantillonnage linéaire : Texel gauche \# = plancher ( \* largeur U), Texel à droite \# = Texel gauche \# + 1</span><span class="sxs-lookup"><span data-stu-id="b941e-130">Linear sampling: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="b941e-131">Pour une coordonnée mise à l’échelle :</span><span class="sxs-lookup"><span data-stu-id="b941e-131">For a scaled coordinate:</span></span>

-   <span data-ttu-id="b941e-132">Échantillonnage de point : Texel \# = Floor (U)</span><span class="sxs-lookup"><span data-stu-id="b941e-132">Point sampling: Texel \# = floor(U)</span></span>
-   <span data-ttu-id="b941e-133">Échantillonnage linéaire : Texel gauche \# = Floor (U-0,5), Texel Right \# = Texel gauche \# + 1</span><span class="sxs-lookup"><span data-stu-id="b941e-133">Linear sampling: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="b941e-134">Où la largeur correspond à la largeur de la texture (dans les texels).</span><span class="sxs-lookup"><span data-stu-id="b941e-134">Where the width, is the width of the texture (in texels).</span></span>

<span data-ttu-id="b941e-135">L’encapsulation d’adresse de texture se produit après le calcul de l’emplacement de Texel.</span><span class="sxs-lookup"><span data-stu-id="b941e-135">Texture address wrapping occurs after the texel location is computed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b941e-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b941e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b941e-137">Ressources (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b941e-137">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




