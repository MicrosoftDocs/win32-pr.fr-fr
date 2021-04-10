---
title: Effet composite arithmétique
description: Utilisez l’effet composite arithmétique pour combiner 2 images à l’aide d’une somme pondérée de pixels à partir des images d’entrée.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- effet composite arithmétique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942598"
---
# <a name="arithmetic-composite-effect"></a><span data-ttu-id="b43d0-104">Effet composite arithmétique</span><span class="sxs-lookup"><span data-stu-id="b43d0-104">Arithmetic composite effect</span></span>

<span data-ttu-id="b43d0-105">Utilisez l’effet composite arithmétique pour combiner 2 images à l’aide d’une somme pondérée de pixels à partir des images d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b43d0-105">Use the arithmetic composite effect to combine 2 images using a weighted sum of pixels from the input images.</span></span>

<span data-ttu-id="b43d0-106">Le CLSID de cet effet est CLSID \_ D2D1ArithmeticComposite.</span><span class="sxs-lookup"><span data-stu-id="b43d0-106">The CLSID for this effect is CLSID\_D2D1ArithmeticComposite.</span></span>

-   [<span data-ttu-id="b43d0-107">Formule</span><span class="sxs-lookup"><span data-stu-id="b43d0-107">Formula</span></span>](#formula)
-   [<span data-ttu-id="b43d0-108">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="b43d0-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="b43d0-109">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="b43d0-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b43d0-110">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="b43d0-110">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="b43d0-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b43d0-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b43d0-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b43d0-112">Related topics</span></span>](#related-topics)

## <a name="formula"></a><span data-ttu-id="b43d0-113">Formule</span><span class="sxs-lookup"><span data-stu-id="b43d0-113">Formula</span></span>

<span data-ttu-id="b43d0-114">La formule ici est utilisée pour calculer cet effet.</span><span class="sxs-lookup"><span data-stu-id="b43d0-114">The formula here is used to compute this effect.</span></span>

<span data-ttu-id="b43d0-115">En sortie<sub>RVBA</sub> = C1 \* source<sub>RVBA</sub> \* destination<sub>RVBA</sub> + C2 \* source<sub>RVBA</sub> + C3 \* destination<sub>RVBA</sub> + C4</span><span class="sxs-lookup"><span data-stu-id="b43d0-115">Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4</span></span>

<span data-ttu-id="b43d0-116">Où C1, C2, C3, C4 sont des coefficients que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="b43d0-116">Where C1, C2, C3, C4 are coefficients that you set.</span></span>

<span data-ttu-id="b43d0-117">Les coefficients correspondent aux valeurs d’un vecteur D2D1 \_ \_ 4F (x, y, z, w) :</span><span class="sxs-lookup"><span data-stu-id="b43d0-117">The coefficients map to the values in a D2D1\_VECTOR\_4F (x, y, z, w):</span></span>

-   <span data-ttu-id="b43d0-118">x = C1</span><span class="sxs-lookup"><span data-stu-id="b43d0-118">x = C1</span></span>
-   <span data-ttu-id="b43d0-119">y = C2</span><span class="sxs-lookup"><span data-stu-id="b43d0-119">y = C2</span></span>
-   <span data-ttu-id="b43d0-120">z = C3</span><span class="sxs-lookup"><span data-stu-id="b43d0-120">z = C3</span></span>
-   <span data-ttu-id="b43d0-121">w = C4</span><span class="sxs-lookup"><span data-stu-id="b43d0-121">w = C4</span></span>

## <a name="example-image"></a><span data-ttu-id="b43d0-122">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="b43d0-122">Example image</span></span>

<span data-ttu-id="b43d0-123">Un exemple simple consiste à ajouter les pixels source et de destination.</span><span class="sxs-lookup"><span data-stu-id="b43d0-123">A simple example is to add the source and destination pixels.</span></span> <span data-ttu-id="b43d0-124">Dans l’exemple, 2 rectangles arrondis sont composés ensemble.</span><span class="sxs-lookup"><span data-stu-id="b43d0-124">In the example, 2 rounded rectangles are composited together.</span></span> <span data-ttu-id="b43d0-125">Le rectangle source est bleu et la destination est rouge.</span><span class="sxs-lookup"><span data-stu-id="b43d0-125">The source rectangle is blue and the destination is red.</span></span>

<span data-ttu-id="b43d0-126">L’image ici est la sortie de l’effet composite arithmétique avec les coefficients de l’équation définie sur les valeurs ici.</span><span class="sxs-lookup"><span data-stu-id="b43d0-126">The image here is the output of the Arithmetic Composite effect with the coefficients of the equation set to the values here.</span></span>

-   <span data-ttu-id="b43d0-127">C1 = 0</span><span class="sxs-lookup"><span data-stu-id="b43d0-127">C1 = 0</span></span>
-   <span data-ttu-id="b43d0-128">C2 = 1</span><span class="sxs-lookup"><span data-stu-id="b43d0-128">C2 = 1</span></span>
-   <span data-ttu-id="b43d0-129">C3 = 1</span><span class="sxs-lookup"><span data-stu-id="b43d0-129">C3 = 1</span></span>
-   <span data-ttu-id="b43d0-130">C4 = 0</span><span class="sxs-lookup"><span data-stu-id="b43d0-130">C4 = 0</span></span>

![exemple d’image indiquant 2 rectangles arrondis de la même taille qui se chevauchent à l’aide de l’effet composite arithmétique.](images/arithmetic-50-percent.png)

<span data-ttu-id="b43d0-132">Le résultat est que les valeurs en pixels pour la source et la destination sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="b43d0-132">The result is that the pixel values for the source and destination are added.</span></span> <span data-ttu-id="b43d0-133">Les zones où les rectangles ne chevauchent pas les valeurs RVBA sont toutes 0.</span><span class="sxs-lookup"><span data-stu-id="b43d0-133">The regions where the rectangles don't overlap the RGBA values are all 0.</span></span> <span data-ttu-id="b43d0-134">L’emplacement des rectangles qui chevauchent la couleur est magenta, car les valeurs R et B sont toutes les deux au maximum.</span><span class="sxs-lookup"><span data-stu-id="b43d0-134">Where the rectangles overlap the color is magenta because the R and B values are both at maximum.</span></span>

<span data-ttu-id="b43d0-135">Voici un autre exemple d’image avec du code.</span><span class="sxs-lookup"><span data-stu-id="b43d0-135">Here's another example image with code.</span></span>



| <span data-ttu-id="b43d0-136">Avant image 1</span><span class="sxs-lookup"><span data-stu-id="b43d0-136">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![première image source avant l’effet.](images/default-before.jpg)    |
| <span data-ttu-id="b43d0-138">Avant image 2</span><span class="sxs-lookup"><span data-stu-id="b43d0-138">Before image 2</span></span>                                                             |
| ![deuxième image avant l’effet.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="b43d0-140">After</span><span class="sxs-lookup"><span data-stu-id="b43d0-140">After</span></span>                                                                      |
| ![image après la transformation.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="b43d0-142">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="b43d0-142">Effect properties</span></span>



| <span data-ttu-id="b43d0-143">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="b43d0-143">Display name and index enumeration</span></span>                                               | <span data-ttu-id="b43d0-144">Description</span><span class="sxs-lookup"><span data-stu-id="b43d0-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b43d0-145">Coefficients</span><span class="sxs-lookup"><span data-stu-id="b43d0-145">Coefficients</span></span><br/> <span data-ttu-id="b43d0-146">\_COefficients d2d1 ARITHMETICCOMPOSITE \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="b43d0-146">D2D1\_ARITHMETICCOMPOSITE\_PROP\_COEFFICIENTS</span></span><br/> | <span data-ttu-id="b43d0-147">Coefficients de l’équation utilisée pour composer les deux images d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b43d0-147">The coefficients for the equation used to composite the two input images.</span></span> <span data-ttu-id="b43d0-148">Les coefficients sont sans unité et illimités.</span><span class="sxs-lookup"><span data-stu-id="b43d0-148">The coefficients are unitless and unbounded.</span></span> <span data-ttu-id="b43d0-149">Le type est D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="b43d0-149">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="b43d0-150">La valeur par défaut est {1.0 f, 0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="b43d0-150">Default value is {1.0f, 0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="b43d0-151">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="b43d0-151">ClampOutput</span></span><br/> <span data-ttu-id="b43d0-152">\_Sortie de Clamp d2d1 ARITHMETICCOMPOSITE \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="b43d0-152">D2D1\_ARITHMETICCOMPOSITE\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="b43d0-153">L’effet fixe les valeurs de couleur à entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="b43d0-153">The effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <br/> <span data-ttu-id="b43d0-154">Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées.</span><span class="sxs-lookup"><span data-stu-id="b43d0-154">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="b43d0-155">Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.</span><span class="sxs-lookup"><span data-stu-id="b43d0-155">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="b43d0-156">Le type est BOOL.</span><span class="sxs-lookup"><span data-stu-id="b43d0-156">Type is BOOL.</span></span><br/> <span data-ttu-id="b43d0-157">La valeur par défaut est FALSe.</span><span class="sxs-lookup"><span data-stu-id="b43d0-157">Default value is FALSE.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="b43d0-158">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="b43d0-158">Output bitmap</span></span>

<span data-ttu-id="b43d0-159">La bitmap de sortie dépend des valeurs de coefficient.</span><span class="sxs-lookup"><span data-stu-id="b43d0-159">The output bitmap depends on the coefficient values.</span></span> <span data-ttu-id="b43d0-160">Il s’agit des tailles de bitmap de sortie possibles.</span><span class="sxs-lookup"><span data-stu-id="b43d0-160">These are the possible output bitmap sizes.</span></span>

-   <span data-ttu-id="b43d0-161">Si C1 est le seul coefficient non nul, la taille de sortie est l’intersection des rectangles d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b43d0-161">If C1 is the only non-zero coefficient, the output size is the intersection of the input rectangles.</span></span>
-   <span data-ttu-id="b43d0-162">Si C2 est le seul coefficient non nul, la taille de sortie est la taille du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="b43d0-162">If C2 is the only non-zero coefficient, the output size is the size of the Source rectangle.</span></span>
-   <span data-ttu-id="b43d0-163">Si C3 est le seul coefficient non nul, la taille de sortie est la taille du rectangle de destination..</span><span class="sxs-lookup"><span data-stu-id="b43d0-163">If C3 is the only non-zero coefficient, the output size is the size of the Destination rectangle..</span></span>
-   <span data-ttu-id="b43d0-164">Si tous les coefficients sont nuls, la taille de sortie est un rectangle vide.</span><span class="sxs-lookup"><span data-stu-id="b43d0-164">If all coefficients are zero, the output size is an empty rectangle.</span></span>
-   <span data-ttu-id="b43d0-165">Pour toutes les autres valeurs de coefficient, la taille de sortie est l’Union des rectangles d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b43d0-165">For all other coefficient values, the output size is the union of the input rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="b43d0-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b43d0-166">Requirements</span></span>



| <span data-ttu-id="b43d0-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b43d0-167">Requirement</span></span> | <span data-ttu-id="b43d0-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="b43d0-168">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b43d0-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b43d0-169">Minimum supported client</span></span> | <span data-ttu-id="b43d0-170">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b43d0-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b43d0-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b43d0-171">Minimum supported server</span></span> | <span data-ttu-id="b43d0-172">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b43d0-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b43d0-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="b43d0-173">Header</span></span>                   | <span data-ttu-id="b43d0-174">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b43d0-174">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b43d0-175">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b43d0-175">Library</span></span>                  | <span data-ttu-id="b43d0-176">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b43d0-176">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b43d0-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b43d0-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b43d0-178">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b43d0-178">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

