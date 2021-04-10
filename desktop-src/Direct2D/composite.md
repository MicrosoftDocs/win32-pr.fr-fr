---
title: Effet composite
description: Utilisez l’effet composite pour combiner 2 images ou plus. Cet effet a 13 modes composites différents.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- effet composite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942276"
---
# <a name="composite-effect"></a><span data-ttu-id="6e993-105">Effet composite</span><span class="sxs-lookup"><span data-stu-id="6e993-105">Composite effect</span></span>

<span data-ttu-id="6e993-106">Utilisez l’effet composite pour combiner 2 images ou plus.</span><span class="sxs-lookup"><span data-stu-id="6e993-106">Use the composite effect to combine 2 or more images.</span></span> <span data-ttu-id="6e993-107">Cet effet a 13 modes composites différents.</span><span class="sxs-lookup"><span data-stu-id="6e993-107">This effect has 13 different composite modes.</span></span> <span data-ttu-id="6e993-108">T</span><span class="sxs-lookup"><span data-stu-id="6e993-108">T</span></span>

<span data-ttu-id="6e993-109">L’effet composite accepte au moins 2 entrées.</span><span class="sxs-lookup"><span data-stu-id="6e993-109">The composite effect accepts 2 or more inputs.</span></span> <span data-ttu-id="6e993-110">Lorsque vous spécifiez 2 images, la destination est la première entrée (index 0) et la source est la deuxième entrée (index 1).</span><span class="sxs-lookup"><span data-stu-id="6e993-110">When you specify 2 images, destination is the first input (index 0) and the source is the second input (index 1).</span></span> <span data-ttu-id="6e993-111">Si vous spécifiez plus de 2 entrées, les images sont composées à partir de la première entrée, puis de la seconde, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e993-111">If you specify more than 2 inputs the images are composited starting with the first input and the second and so on.</span></span>

<span data-ttu-id="6e993-112">Cet effet implémente tous les modes à l’aide de l’unité de fusion de l’unité de traitement graphique (GPU).</span><span class="sxs-lookup"><span data-stu-id="6e993-112">This effect implements all of the modes using the blending unit of the graphics processing unit (GPU).</span></span>

<span data-ttu-id="6e993-113">Le CLSID de cet effet est CLSID \_ D2D1Composite.</span><span class="sxs-lookup"><span data-stu-id="6e993-113">The CLSID for this effect is CLSID\_D2D1Composite.</span></span>

-   [<span data-ttu-id="6e993-114">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="6e993-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="6e993-115">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="6e993-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="6e993-116">Types de mode</span><span class="sxs-lookup"><span data-stu-id="6e993-116">Mode types</span></span>](#mode-types)
-   [<span data-ttu-id="6e993-117">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="6e993-117">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="6e993-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e993-118">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6e993-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e993-119">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6e993-120">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="6e993-120">Example image</span></span>

<span data-ttu-id="6e993-121">L’image ici montre 2 rectangles arrondis de la même taille qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="6e993-121">The image here shows 2 rounded rectangles of the same size that overlap.</span></span> <span data-ttu-id="6e993-122">Le rectangle bleu est la source et le rectangle rouge est la destination.</span><span class="sxs-lookup"><span data-stu-id="6e993-122">The blue rectangle is the source and the red rectangle is the destination.</span></span> <span data-ttu-id="6e993-123">Les images ont été composites avec le mode Source sur.</span><span class="sxs-lookup"><span data-stu-id="6e993-123">The images were composited with the Source Over mode.</span></span>

![exemple d’image indiquant 2 rectangles arrondis de la même taille qui se chevauchent à l’aide du mode Source sur.](images/composite-over.png)

<span data-ttu-id="6e993-125">Voici un autre exemple utilisant le mode par défaut.</span><span class="sxs-lookup"><span data-stu-id="6e993-125">Here's another example using the default mode.</span></span>



| <span data-ttu-id="6e993-126">Avant image 1</span><span class="sxs-lookup"><span data-stu-id="6e993-126">Before image 1</span></span>                                                          |
|-------------------------------------------------------------------------|
| ![première image source avant l’effet.](images/default-before.jpg) |
| <span data-ttu-id="6e993-128">Avant image 2</span><span class="sxs-lookup"><span data-stu-id="6e993-128">Before image 2</span></span>                                                          |
| ![deuxième image avant l’effet.](images/3-composite(2of2).png)    |
| <span data-ttu-id="6e993-130">After</span><span class="sxs-lookup"><span data-stu-id="6e993-130">After</span></span>                                                                   |
| ![image après la transformation.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="6e993-132">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="6e993-132">Effect properties</span></span>



| <span data-ttu-id="6e993-133">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="6e993-133">Display name and index enumeration</span></span>                     | <span data-ttu-id="6e993-134">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="6e993-134">Type and default value</span></span>                                                          | <span data-ttu-id="6e993-135">Description</span><span class="sxs-lookup"><span data-stu-id="6e993-135">Description</span></span>                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="6e993-136">Mode</span><span class="sxs-lookup"><span data-stu-id="6e993-136">Mode</span></span><br/> <span data-ttu-id="6e993-137">\_Mode d2d1 composite \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="6e993-137">D2D1\_COMPOSITE\_PROP\_MODE</span></span><br/> | <span data-ttu-id="6e993-138">D2D1 \_ mode composite \_</span><span class="sxs-lookup"><span data-stu-id="6e993-138">D2D1\_COMPOSITE\_MODE</span></span><br/> <span data-ttu-id="6e993-139">\_ \_ Source en mode composite d2d1 \_ \_ sur</span><span class="sxs-lookup"><span data-stu-id="6e993-139">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span><br/> | <span data-ttu-id="6e993-140">Mode utilisé pour l’effet.</span><span class="sxs-lookup"><span data-stu-id="6e993-140">The mode used for the effect.</span></span> |



 

## <a name="mode-types"></a><span data-ttu-id="6e993-141">Types de mode</span><span class="sxs-lookup"><span data-stu-id="6e993-141">Mode types</span></span>

<span data-ttu-id="6e993-142">Le tableau ci-dessous montre les modes de cet effet.</span><span class="sxs-lookup"><span data-stu-id="6e993-142">The table here shows the modes of this effect.</span></span> <span data-ttu-id="6e993-143">Les équations figurant dans le tableau utilisent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6e993-143">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="6e993-144">O = sortie</span><span class="sxs-lookup"><span data-stu-id="6e993-144">O = Output</span></span>
-   <span data-ttu-id="6e993-145">S = source</span><span class="sxs-lookup"><span data-stu-id="6e993-145">S = Source</span></span>
-   <span data-ttu-id="6e993-146">SA = source alpha</span><span class="sxs-lookup"><span data-stu-id="6e993-146">SA = Source Alpha</span></span>
-   <span data-ttu-id="6e993-147">D = destination</span><span class="sxs-lookup"><span data-stu-id="6e993-147">D = Destination</span></span>
-   <span data-ttu-id="6e993-148">DA = alpha de destination</span><span class="sxs-lookup"><span data-stu-id="6e993-148">DA = Destination Alpha</span></span>



| <span data-ttu-id="6e993-149">Énumération</span><span class="sxs-lookup"><span data-stu-id="6e993-149">Enumeration</span></span>                                  | <span data-ttu-id="6e993-150">Sommaire</span><span class="sxs-lookup"><span data-stu-id="6e993-150">Equation</span></span>                          | <span data-ttu-id="6e993-151">Taille de la bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="6e993-151">Output Bitmap Size</span></span>                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e993-152">\_ \_ Source en mode composite d2d1 \_ \_ sur</span><span class="sxs-lookup"><span data-stu-id="6e993-152">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span>          | <span data-ttu-id="6e993-153">O = S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="6e993-153">O = S + (1   SA) \* D</span></span>             | <span data-ttu-id="6e993-154">Union des bitmaps sources et de destination</span><span class="sxs-lookup"><span data-stu-id="6e993-154">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="6e993-155">\_Destination du mode composite d2d1 \_ \_ \_ sur</span><span class="sxs-lookup"><span data-stu-id="6e993-155">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OVER</span></span>     | <span data-ttu-id="6e993-156">O = (1 DA) \* S + D</span><span class="sxs-lookup"><span data-stu-id="6e993-156">O = (1   DA) \* S + D</span></span>             | <span data-ttu-id="6e993-157">Union des bitmaps sources et de destination</span><span class="sxs-lookup"><span data-stu-id="6e993-157">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="6e993-158">\_ \_ Source en mode composite d2d1 \_ \_ dans</span><span class="sxs-lookup"><span data-stu-id="6e993-158">D2D1\_COMPOSITE\_MODE\_SOURCE\_IN</span></span>            | <span data-ttu-id="6e993-159">O = DA \* S</span><span class="sxs-lookup"><span data-stu-id="6e993-159">O = DA \* S</span></span>                       | <span data-ttu-id="6e993-160">Intersection des bitmaps de source et de destination</span><span class="sxs-lookup"><span data-stu-id="6e993-160">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="6e993-161">\_ \_ Destination du mode composite d2d1 \_ \_ dans</span><span class="sxs-lookup"><span data-stu-id="6e993-161">D2D1\_COMPOSITE\_MODE\_DESTINATION\_IN</span></span>       | <span data-ttu-id="6e993-162">O = SA \* D</span><span class="sxs-lookup"><span data-stu-id="6e993-162">O = SA \* D</span></span>                       | <span data-ttu-id="6e993-163">Intersection des bitmaps de source et de destination</span><span class="sxs-lookup"><span data-stu-id="6e993-163">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="6e993-164">\_ \_ Source en mode composite d2d1 \_ \_ out</span><span class="sxs-lookup"><span data-stu-id="6e993-164">D2D1\_COMPOSITE\_MODE\_SOURCE\_OUT</span></span>           | <span data-ttu-id="6e993-165">O = (1-DA) \* S</span><span class="sxs-lookup"><span data-stu-id="6e993-165">O = (1 - DA) \* S</span></span>                 | <span data-ttu-id="6e993-166">Région de la bitmap source</span><span class="sxs-lookup"><span data-stu-id="6e993-166">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="6e993-167">D2D1 \_ \_ sortie de \_ destination en mode composite \_</span><span class="sxs-lookup"><span data-stu-id="6e993-167">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OUT</span></span>      | <span data-ttu-id="6e993-168">O = (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="6e993-168">O = (1 - SA) \* D</span></span>                 | <span data-ttu-id="6e993-169">Région de la bitmap de destination</span><span class="sxs-lookup"><span data-stu-id="6e993-169">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="6e993-170">D2D1 \_ \_ source en mode composite haut \_ \_</span><span class="sxs-lookup"><span data-stu-id="6e993-170">D2D1\_COMPOSITE\_MODE\_SOURCE\_ATOP</span></span>          | <span data-ttu-id="6e993-171">O = DA \* S + (1-sa) \* D</span><span class="sxs-lookup"><span data-stu-id="6e993-171">O = DA \* S + (1 - SA) \* D</span></span>       | <span data-ttu-id="6e993-172">Région de la bitmap de destination</span><span class="sxs-lookup"><span data-stu-id="6e993-172">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="6e993-173">D2D1 \_ de \_ destination en mode composite par- \_ \_ dessus</span><span class="sxs-lookup"><span data-stu-id="6e993-173">D2D1\_COMPOSITE\_MODE\_DESTINATION\_ATOP</span></span>     | <span data-ttu-id="6e993-174">O = (1-DA) \* S + sa \* D</span><span class="sxs-lookup"><span data-stu-id="6e993-174">O = (1 - DA) \* S + SA \* D</span></span>       | <span data-ttu-id="6e993-175">Région de la bitmap source</span><span class="sxs-lookup"><span data-stu-id="6e993-175">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="6e993-176">D2D1 \_ mode composite \_ \_ Xor</span><span class="sxs-lookup"><span data-stu-id="6e993-176">D2D1\_COMPOSITE\_MODE\_XOR</span></span>                   | <span data-ttu-id="6e993-177">O = (1-DA) \* S + (1-sa) \* D</span><span class="sxs-lookup"><span data-stu-id="6e993-177">O = (1 - DA) \* S + (1 - SA) \* D</span></span> | <span data-ttu-id="6e993-178">Union des bitmaps sources et de destination</span><span class="sxs-lookup"><span data-stu-id="6e993-178">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="6e993-179">D2D1 \_ mode composite \_ \_ plus</span><span class="sxs-lookup"><span data-stu-id="6e993-179">D2D1\_COMPOSITE\_MODE\_PLUS</span></span>                  | <span data-ttu-id="6e993-180">O = S + D</span><span class="sxs-lookup"><span data-stu-id="6e993-180">O = S + D</span></span>                         | <span data-ttu-id="6e993-181">Union des bitmaps sources et de destination</span><span class="sxs-lookup"><span data-stu-id="6e993-181">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="6e993-182">\_ \_ Copie source en mode COMPOSite d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="6e993-182">D2D1\_COMPOSITE\_MODE\_SOURCE\_COPY</span></span>          | <span data-ttu-id="6e993-183">O = S</span><span class="sxs-lookup"><span data-stu-id="6e993-183">O = S</span></span>                             | <span data-ttu-id="6e993-184">Région de la bitmap source</span><span class="sxs-lookup"><span data-stu-id="6e993-184">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="6e993-185">\_ \_ \_ Copie source délimitée en \_ mode composite d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="6e993-185">D2D1\_COMPOSITE\_MODE\_BOUNDED\_SOURCE\_COPY</span></span> | <span data-ttu-id="6e993-186">O = S (uniquement lorsque la source existe)</span><span class="sxs-lookup"><span data-stu-id="6e993-186">O = S (only where source exists)</span></span>  | <span data-ttu-id="6e993-187">Union des bitmaps sources et de destination.</span><span class="sxs-lookup"><span data-stu-id="6e993-187">Union of source and destination bitmaps.</span></span> <span data-ttu-id="6e993-188">La destination n’est pas remplacée lorsque la source n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="6e993-188">Destination is not overwritten where the source doesn't exist.</span></span> |
| <span data-ttu-id="6e993-189">\_Masque d2d1 \_ mode composite \_ \_ inversé</span><span class="sxs-lookup"><span data-stu-id="6e993-189">D2D1\_COMPOSITE\_MODE\_MASK\_INVERT</span></span>          | <span data-ttu-id="6e993-190">O = (1 D) \* S + (1 sa) \* D</span><span class="sxs-lookup"><span data-stu-id="6e993-190">O = (1   D) \* S + (1   SA) \* D</span></span>  | <span data-ttu-id="6e993-191">Union des bitmaps sources et de destination. Les valeurs alpha sont inchangées.</span><span class="sxs-lookup"><span data-stu-id="6e993-191">Union of source and destination bitmaps.The alpha values are unchanged.</span></span>                                 |



 

<span data-ttu-id="6e993-192">La figure ci-dessous montre un exemple de chacun des modes avec des images qui ont une opacité de 1,0 ou 0,5.</span><span class="sxs-lookup"><span data-stu-id="6e993-192">The figure here shows an example of each of the modes with images that have an opacity of 1.0 or 0.5.</span></span>

![exemple d’image de chacun des modes avec opacité défini sur 1,0 ou 0,5.](images/composite-types.png)

## <a name="sample-code"></a><span data-ttu-id="6e993-194">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="6e993-194">Sample code</span></span>

<span data-ttu-id="6e993-195">Pour obtenir un exemple de cet effet, téléchargez l' [exemple de modes d’effet composite de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="6e993-195">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e993-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e993-196">Requirements</span></span>



| <span data-ttu-id="6e993-197">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e993-197">Requirement</span></span> | <span data-ttu-id="6e993-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e993-198">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e993-199">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e993-199">Minimum supported client</span></span> | <span data-ttu-id="6e993-200">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="6e993-200">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6e993-201">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e993-201">Minimum supported server</span></span> | <span data-ttu-id="6e993-202">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="6e993-202">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6e993-203">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e993-203">Header</span></span>                   | <span data-ttu-id="6e993-204">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="6e993-204">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="6e993-205">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6e993-205">Library</span></span>                  | <span data-ttu-id="6e993-206">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="6e993-206">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="6e993-207">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e993-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e993-208">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="6e993-208">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

