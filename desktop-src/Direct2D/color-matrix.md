---
title: Effet matrice de couleurs
description: Utilisez l’effet matrice de couleurs pour modifier les valeurs RVBA d’une image bitmap.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- effet matrice de couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032736"
---
# <a name="color-matrix-effect"></a><span data-ttu-id="ad480-104">Effet matrice de couleurs</span><span class="sxs-lookup"><span data-stu-id="ad480-104">Color matrix effect</span></span>

<span data-ttu-id="ad480-105">Utilisez l’effet matrice de couleurs pour modifier les valeurs RVBA d’une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ad480-105">Use the color matrix effect to alter the RGBA values of a bitmap.</span></span>

<span data-ttu-id="ad480-106">Vous pouvez utiliser cet effet pour :</span><span class="sxs-lookup"><span data-stu-id="ad480-106">You can use this effect to:</span></span>

-   <span data-ttu-id="ad480-107">Supprimer un canal de couleur d’une image.</span><span class="sxs-lookup"><span data-stu-id="ad480-107">Remove a color channel from an image.</span></span>
-   <span data-ttu-id="ad480-108">Réduisez la couleur d’une image.</span><span class="sxs-lookup"><span data-stu-id="ad480-108">Reduce the color in an image.</span></span>
-   <span data-ttu-id="ad480-109">Permuter les canaux de couleurs.</span><span class="sxs-lookup"><span data-stu-id="ad480-109">Swap color channels.</span></span>
-   <span data-ttu-id="ad480-110">Combiner des canaux de couleurs.</span><span class="sxs-lookup"><span data-stu-id="ad480-110">Combine color channels.</span></span>

<span data-ttu-id="ad480-111">De nombreux effets intégrés sont des spécialisations de matrice de couleur optimisées pour l’utilisation prévue des effets.</span><span class="sxs-lookup"><span data-stu-id="ad480-111">Many built-in effects are specializations of color matrix that are optimized for the intended use of the effects.</span></span> <span data-ttu-id="ad480-112">Les exemples incluent [saturation](saturation.md), [teinte](hue-rotate.md), [sépia](sepia-effect.md), [température et teinte](temperature-and-tint-effect.md).</span><span class="sxs-lookup"><span data-stu-id="ad480-112">Examples include [saturation](saturation.md), [hue rotate](hue-rotate.md), [sepia](sepia-effect.md), and [temperature and tint](temperature-and-tint-effect.md).</span></span>

<span data-ttu-id="ad480-113">Le CLSID de cet effet est CLSID \_ D2D1ColorMatrix.</span><span class="sxs-lookup"><span data-stu-id="ad480-113">The CLSID for this effect is CLSID\_D2D1ColorMatrix.</span></span>

-   [<span data-ttu-id="ad480-114">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="ad480-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ad480-115">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="ad480-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ad480-116">Modes alpha</span><span class="sxs-lookup"><span data-stu-id="ad480-116">Alpha modes</span></span>](#alpha-modes)
-   [<span data-ttu-id="ad480-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad480-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ad480-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad480-118">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ad480-119">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="ad480-119">Example image</span></span>

<span data-ttu-id="ad480-120">L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet de matrice de couleurs qui échangent les canaux rouge et bleu.</span><span class="sxs-lookup"><span data-stu-id="ad480-120">The example here shows the input and output images of the color matrix effect that swaps the red and blue channels.</span></span>



| <span data-ttu-id="ad480-121">Avant</span><span class="sxs-lookup"><span data-stu-id="ad480-121">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)   |
| <span data-ttu-id="ad480-123">After</span><span class="sxs-lookup"><span data-stu-id="ad480-123">After</span></span>                                                        |
| ![image après la transformation.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="ad480-125">Cet effet multiplie les valeurs RVBA de l’image par une matrice principale de colonne 5x4, comme indiqué dans cette équation.</span><span class="sxs-lookup"><span data-stu-id="ad480-125">This effect multiplies the RGBA values of the image by a 5x4, column major matrix as shown in this equation.</span></span>

![exemple de définition de matrice.](images/color-matrix-formula.png)

<span data-ttu-id="ad480-127">Cet effet fonctionne sur les images alpha directes et prémultipliées.</span><span class="sxs-lookup"><span data-stu-id="ad480-127">This effect works on straight and premultiplied alpha images.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="ad480-128">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="ad480-128">Effect properties</span></span>



| <span data-ttu-id="ad480-129">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="ad480-129">Display name and index enumeration</span></span>                                       | <span data-ttu-id="ad480-130">Description</span><span class="sxs-lookup"><span data-stu-id="ad480-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad480-131">ColorMatrix</span><span class="sxs-lookup"><span data-stu-id="ad480-131">ColorMatrix</span></span><br/> <span data-ttu-id="ad480-132">\_Matrice de couleurs d2d1 COLORMATRIX \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad480-132">D2D1\_COLORMATRIX\_PROP\_COLOR\_MATRIX</span></span><br/> | <span data-ttu-id="ad480-133">Matrice 5x4 de valeurs float.</span><span class="sxs-lookup"><span data-stu-id="ad480-133">A 5x4 matrix of float values.</span></span> <span data-ttu-id="ad480-134">Les éléments de la matrice ne sont pas limités et sont sans unité.</span><span class="sxs-lookup"><span data-stu-id="ad480-134">The elements in the matrix are not bounded and are unitless.</span></span><br/> <span data-ttu-id="ad480-135">La valeur par défaut est la matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="ad480-135">The default is the identity matrix.</span></span><br/> <span data-ttu-id="ad480-136">Le type est D2D1 \_ Matrix \_ 5x4 \_ F.</span><span class="sxs-lookup"><span data-stu-id="ad480-136">The type is D2D1\_MATRIX\_5X4\_F.</span></span><br/> <span data-ttu-id="ad480-137">La valeur par défaut est Matrix5x4F (1, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="ad480-137">The default value is Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span></span> <br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="ad480-138">AlphaMode</span><span class="sxs-lookup"><span data-stu-id="ad480-138">AlphaMode</span></span><br/> <span data-ttu-id="ad480-139">\_ \_ \_ Mode Alpha d2d1 COLORMATRIX \_ prop</span><span class="sxs-lookup"><span data-stu-id="ad480-139">D2D1\_COLORMATRIX\_PROP\_ALPHA\_MODE</span></span><br/>     | <span data-ttu-id="ad480-140">Mode Alpha de la sortie.</span><span class="sxs-lookup"><span data-stu-id="ad480-140">The alpha mode of the output.</span></span> <span data-ttu-id="ad480-141">Pour plus d’informations, consultez [modes alpha](#alpha-modes) .</span><span class="sxs-lookup"><span data-stu-id="ad480-141">See [Alpha modes](#alpha-modes) for more info.</span></span> <br/> <span data-ttu-id="ad480-142">Le type est D2D1 \_ COLORMATRIX \_ alpha \_ mode.</span><span class="sxs-lookup"><span data-stu-id="ad480-142">The type is D2D1\_COLORMATRIX\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="ad480-143">La valeur par défaut est \_ d2d1 \_ COLORMATRIX \_ en mode Alpha \_ prémultiplié.</span><span class="sxs-lookup"><span data-stu-id="ad480-143">The default value is D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ad480-144">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="ad480-144">ClampOutput</span></span><br/> <span data-ttu-id="ad480-145">\_Sortie de Clamp d2d1 COLORMATRIX \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad480-145">D2D1\_COLORMATRIX\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="ad480-146">Si l’effet fixe les valeurs de couleur entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="ad480-146">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="ad480-147">L’effet serre les valeurs avant de prémultiplier le alpha.</span><span class="sxs-lookup"><span data-stu-id="ad480-147">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="ad480-148">Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées.</span><span class="sxs-lookup"><span data-stu-id="ad480-148">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="ad480-149">Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.</span><span class="sxs-lookup"><span data-stu-id="ad480-149">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="ad480-150">Le type est BOOL.</span><span class="sxs-lookup"><span data-stu-id="ad480-150">The type is BOOL.</span></span><br/> <span data-ttu-id="ad480-151">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="ad480-151">The default value is FALSE.</span></span><br/> |



 

## <a name="alpha-modes"></a><span data-ttu-id="ad480-152">Modes alpha</span><span class="sxs-lookup"><span data-stu-id="ad480-152">Alpha modes</span></span>



| <span data-ttu-id="ad480-153">Nom</span><span class="sxs-lookup"><span data-stu-id="ad480-153">Name</span></span>                                          | <span data-ttu-id="ad480-154">Description</span><span class="sxs-lookup"><span data-stu-id="ad480-154">Description</span></span>                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad480-155">D2D1 \_ COLORMATRIX \_ \_ en mode Alpha \_ prémultiplié</span><span class="sxs-lookup"><span data-stu-id="ad480-155">D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="ad480-156">L’effet annule la prémultiplication de l’entrée, applique la matrice de couleurs et prémultiplie la sortie.</span><span class="sxs-lookup"><span data-stu-id="ad480-156">The effect un-premultiplies the input, applies the color matrix, and premultiplies the output.</span></span><br/> |
| <span data-ttu-id="ad480-157">\_Mode d2d1 \_ COLORMATRIX \_ alpha \_ simple</span><span class="sxs-lookup"><span data-stu-id="ad480-157">D2D1\_COLORMATRIX\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="ad480-158">L’effet applique la matrice de couleurs directement à l’entrée et ne prémultiplie pas la sortie.</span><span class="sxs-lookup"><span data-stu-id="ad480-158">The effect applies the color matrix directly to the input, and doesn't premultiply the output.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad480-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad480-159">Requirements</span></span>



| <span data-ttu-id="ad480-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad480-160">Requirement</span></span> | <span data-ttu-id="ad480-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad480-161">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad480-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad480-162">Minimum supported client</span></span> | <span data-ttu-id="ad480-163">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ad480-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ad480-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad480-164">Minimum supported server</span></span> | <span data-ttu-id="ad480-165">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ad480-165">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ad480-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad480-166">Header</span></span>                   | <span data-ttu-id="ad480-167">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ad480-167">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ad480-168">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad480-168">Library</span></span>                  | <span data-ttu-id="ad480-169">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ad480-169">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ad480-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad480-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad480-171">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ad480-171">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

