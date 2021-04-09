---
description: Les sommets de l’espace de la caméra sont calculés en transformant les vertex de l’objet avec la matrice de la vue du monde.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Transformations d’espace de caméra (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110767"
---
# <a name="camera-space-transformations-direct3d-9"></a><span data-ttu-id="3c0be-103">Transformations d’espace de caméra (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3c0be-103">Camera Space Transformations (Direct3D 9)</span></span>

<span data-ttu-id="3c0be-104">Les sommets de l’espace de la caméra sont calculés en transformant les vertex de l’objet avec la matrice de la vue du monde.</span><span class="sxs-lookup"><span data-stu-id="3c0be-104">Vertices in the camera space are computed by transforming the object vertices with the world view matrix.</span></span>

<span data-ttu-id="3c0be-105">V = V \* wvMatrix</span><span class="sxs-lookup"><span data-stu-id="3c0be-105">V = V \* wvMatrix</span></span>

<span data-ttu-id="3c0be-106">Les normales des sommets, dans l’espace de l’appareil photo, sont calculées en transformant les normales de l’objet avec la transposer inverse de la matrice de la vue du monde.</span><span class="sxs-lookup"><span data-stu-id="3c0be-106">Vertex normals, in camera space, are computed by transforming the object normals with the inverse transpose of the world view matrix.</span></span> <span data-ttu-id="3c0be-107">La matrice de la vue du monde peut être ou non orthogonale.</span><span class="sxs-lookup"><span data-stu-id="3c0be-107">The world view matrix may or may not be orthogonal.</span></span>

<span data-ttu-id="3c0be-108">N = N \* (wvMatrix ⁻ ¹)<sup>T</sup></span><span class="sxs-lookup"><span data-stu-id="3c0be-108">N = N \* (wvMatrix⁻¹)<sup>T</sup></span></span>

<span data-ttu-id="3c0be-109">L’inversion de matrice et la permutation de matrice fonctionnent sur une matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="3c0be-109">The matrix inversion and matrix transpose operate on a 4x4 matrix.</span></span> <span data-ttu-id="3c0be-110">La multiplication combine la normale avec la partie 3x3 de la matrice 4x4 résultante.</span><span class="sxs-lookup"><span data-stu-id="3c0be-110">The multiply combines the normal with the 3x3 portion of the resulting 4x4 matrix.</span></span>

<span data-ttu-id="3c0be-111">Si l’état de rendu D3DRENDERSTATE \_ NORMALIZENORMALS est défini sur **true**, les vecteurs normaux de vertex sont normalisés après la transformation en espace de caméra comme suit :</span><span class="sxs-lookup"><span data-stu-id="3c0be-111">If the render state, D3DRENDERSTATE\_NORMALIZENORMALS is set to **TRUE**, vertex normal vectors are normalized after transformation to camera space as follows:</span></span>

<span data-ttu-id="3c0be-112">N = normal (N)</span><span class="sxs-lookup"><span data-stu-id="3c0be-112">N = norm(N)</span></span>

<span data-ttu-id="3c0be-113">La position de la lumière dans l’espace de l’appareil photo est calculée en transformant la position de la source de lumière avec la matrice de vue.</span><span class="sxs-lookup"><span data-stu-id="3c0be-113">Light position in camera space is computed by transforming the light source position with the view matrix.</span></span>

<span data-ttu-id="3c0be-114">LP = LP \* vMatrix</span><span class="sxs-lookup"><span data-stu-id="3c0be-114">Lₚ = Lₚ \* vMatrix</span></span>

<span data-ttu-id="3c0be-115">La direction de la lumière dans l’espace de caméra pour une lumière directionnelle est calculée en multipliant la direction de la source de lumière par la matrice de vue, en normalisant et en annulant le résultat.</span><span class="sxs-lookup"><span data-stu-id="3c0be-115">The direction to the light in camera space for a directional light is computed by multiplying the light source direction by the view matrix, normalizing, and negating the result.</span></span>

<span data-ttu-id="3c0be-116">L<sub>Rép</sub> =-normal (L<sub>Rép</sub> \* wvMatrix)</span><span class="sxs-lookup"><span data-stu-id="3c0be-116">L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)</span></span>

<span data-ttu-id="3c0be-117">Pour le point de D3DLIGHT \_ et D3DLIGHT, \_ le sens de la lumière est calculé comme suit :</span><span class="sxs-lookup"><span data-stu-id="3c0be-117">For the D3DLIGHT\_POINT and D3DLIGHT\_SPOT the direction to light is computed as follows:</span></span>

<span data-ttu-id="3c0be-118">L<sub>Rép</sub> = normal (V \* LP), où les paramètres sont définis dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3c0be-118">L<sub>dir</sub> = norm(V \* Lₚ), where the parameters are defined in the following table.</span></span>



| <span data-ttu-id="3c0be-119">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3c0be-119">Parameter</span></span>       | <span data-ttu-id="3c0be-120">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="3c0be-120">Default value</span></span> | <span data-ttu-id="3c0be-121">Type</span><span class="sxs-lookup"><span data-stu-id="3c0be-121">Type</span></span>      | <span data-ttu-id="3c0be-122">Description</span><span class="sxs-lookup"><span data-stu-id="3c0be-122">Description</span></span>                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <span data-ttu-id="3c0be-123"><sub>Rép</sub> .</span><span class="sxs-lookup"><span data-stu-id="3c0be-123">L<sub>dir</sub></span></span> | <span data-ttu-id="3c0be-124">N/A</span><span class="sxs-lookup"><span data-stu-id="3c0be-124">N/A</span></span>           | <span data-ttu-id="3c0be-125">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="3c0be-125">D3DVECTOR</span></span> | <span data-ttu-id="3c0be-126">Vecteur de direction du sommet de l’objet vers la lumière</span><span class="sxs-lookup"><span data-stu-id="3c0be-126">Direction vector from object vertex to the light</span></span>          |
| <span data-ttu-id="3c0be-127">V</span><span class="sxs-lookup"><span data-stu-id="3c0be-127">V</span></span>               | <span data-ttu-id="3c0be-128">N/A</span><span class="sxs-lookup"><span data-stu-id="3c0be-128">N/A</span></span>           | <span data-ttu-id="3c0be-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="3c0be-129">D3DVECTOR</span></span> | <span data-ttu-id="3c0be-130">Position du vertex dans l’espace de l’appareil photo</span><span class="sxs-lookup"><span data-stu-id="3c0be-130">Vertex position in camera space</span></span>                           |
| <span data-ttu-id="3c0be-131">wvMatrix</span><span class="sxs-lookup"><span data-stu-id="3c0be-131">wvMatrix</span></span>        | <span data-ttu-id="3c0be-132">Identité</span><span class="sxs-lookup"><span data-stu-id="3c0be-132">Identity</span></span>      | <span data-ttu-id="3c0be-133">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="3c0be-133">D3DMATRIX</span></span> | <span data-ttu-id="3c0be-134">Matrice composite contenant les transformations universelles et de vue</span><span class="sxs-lookup"><span data-stu-id="3c0be-134">Composite matrix containing the world and view transforms</span></span> |
| <span data-ttu-id="3c0be-135">N</span><span class="sxs-lookup"><span data-stu-id="3c0be-135">N</span></span>               | <span data-ttu-id="3c0be-136">N/A</span><span class="sxs-lookup"><span data-stu-id="3c0be-136">N/A</span></span>           | <span data-ttu-id="3c0be-137">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="3c0be-137">D3DVECTOR</span></span> | <span data-ttu-id="3c0be-138">Vertex-normal</span><span class="sxs-lookup"><span data-stu-id="3c0be-138">Vertex normal</span></span>                                             |
| <span data-ttu-id="3c0be-139">Aid</span><span class="sxs-lookup"><span data-stu-id="3c0be-139">Lₚ</span></span>              | <span data-ttu-id="3c0be-140">N/A</span><span class="sxs-lookup"><span data-stu-id="3c0be-140">N/A</span></span>           | <span data-ttu-id="3c0be-141">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="3c0be-141">D3DVECTOR</span></span> | <span data-ttu-id="3c0be-142">Position de la lumière dans l’espace de l’appareil photo</span><span class="sxs-lookup"><span data-stu-id="3c0be-142">Light position in camera space</span></span>                            |
| <span data-ttu-id="3c0be-143">vMatrix</span><span class="sxs-lookup"><span data-stu-id="3c0be-143">vMatrix</span></span>         | <span data-ttu-id="3c0be-144">Identité</span><span class="sxs-lookup"><span data-stu-id="3c0be-144">Identity</span></span>      | <span data-ttu-id="3c0be-145">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="3c0be-145">D3DMATRIX</span></span> | <span data-ttu-id="3c0be-146">Matrice contenant la transformation de la vue</span><span class="sxs-lookup"><span data-stu-id="3c0be-146">Matrix containing the view transform</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="3c0be-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c0be-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c0be-148">Mathématiques d’éclairage</span><span class="sxs-lookup"><span data-stu-id="3c0be-148">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



