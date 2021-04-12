---
title: Effet de transfert de table
description: Utilisez l’effet de transfert de table pour mapper les intensités de couleur d’une image à l’aide d’une fonction de transfert créée à partir de l’interpolation d’une liste de valeurs que vous fournissez.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- effet de transfert de table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465331"
---
# <a name="table-transfer-effect"></a><span data-ttu-id="1cf15-104">Effet de transfert de table</span><span class="sxs-lookup"><span data-stu-id="1cf15-104">Table transfer effect</span></span>

<span data-ttu-id="1cf15-105">Utilisez l’effet de transfert de table pour mapper les intensités de couleur d’une image à l’aide d’une fonction de transfert créée à partir de l’interpolation d’une liste de valeurs que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="1cf15-105">Use the table transfer effect to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.</span></span>

<span data-ttu-id="1cf15-106">Le CLSID de cet effet est CLSID \_ D2D1TableTransfer.</span><span class="sxs-lookup"><span data-stu-id="1cf15-106">The CLSID for this effect is CLSID\_D2D1TableTransfer.</span></span>

-   [<span data-ttu-id="1cf15-107">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="1cf15-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="1cf15-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="1cf15-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="1cf15-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cf15-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1cf15-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1cf15-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="1cf15-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="1cf15-111">Example image</span></span>

<span data-ttu-id="1cf15-112">L’image ci-dessous montre l’entrée et la sortie de l’effet de transfert de table.</span><span class="sxs-lookup"><span data-stu-id="1cf15-112">The image here shows the input and output of the table transfer effect.</span></span>



| <span data-ttu-id="1cf15-113">Avant</span><span class="sxs-lookup"><span data-stu-id="1cf15-113">Before</span></span>                                                         |
|----------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)     |
| <span data-ttu-id="1cf15-115">After</span><span class="sxs-lookup"><span data-stu-id="1cf15-115">After</span></span>                                                          |
| ![image après la transformation.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="1cf15-117">La fonction de transfert est basée sur une liste d’entrées V = (v0, v1, v2, V3, V ?</span><span class="sxs-lookup"><span data-stu-id="1cf15-117">The transfer function is based on a list of inputs V=(V0,V1,V2,V3, V?</span></span> <span data-ttu-id="1cf15-118">, V<sub>N</sub>), où N est le nombre d’éléments-1.</span><span class="sxs-lookup"><span data-stu-id="1cf15-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="1cf15-119">L’intensité en pixels d’entrée est représentée par C. L’intensité en pixels de sortie, C peut être calculée avec l’équation.</span><span class="sxs-lookup"><span data-stu-id="1cf15-119">The input pixel intensity is represented as C. The output pixel intensity, C  can be calculated with the equation.</span></span>

<span data-ttu-id="1cf15-120">Pour une valeur C, choisissez une valeur k, telle que : k/N = C < (k + 1)/N</span><span class="sxs-lookup"><span data-stu-id="1cf15-120">For a value C, pick a value k, such that: k/N = C < (k+1)/N</span></span>

<span data-ttu-id="1cf15-121">La sortie C est calculée à l’aide de l’équation suivante : C' = V ?</span><span class="sxs-lookup"><span data-stu-id="1cf15-121">The output C  is calculated using the following equation: C' = V?</span></span> <span data-ttu-id="1cf15-122">+ (C-k/N) \* N \* (V ??? 1,0?</span><span class="sxs-lookup"><span data-stu-id="1cf15-122">+ (C -  k/N) \* N \* (V???1?</span></span> <span data-ttu-id="1cf15-123">-V ?)</span><span class="sxs-lookup"><span data-stu-id="1cf15-123">- V?)</span></span>

<span data-ttu-id="1cf15-124">Cet effet fonctionne sur les images alpha directes et prémultipliées.</span><span class="sxs-lookup"><span data-stu-id="1cf15-124">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="1cf15-125">L’effet génère des bitmaps alpha prémultipliés.</span><span class="sxs-lookup"><span data-stu-id="1cf15-125">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="1cf15-126">Voici à quoi ressemble le graphique de la fonction de transfert de table si la propriété de table a la valeur `[0.0, 0.25, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="1cf15-126">Here is what the graph of table transfer function looks like if the table property is set to `[0.0, 0.25, 1.0]`.</span></span>

![graphique d’intensité de pixel pour la fonction de transfert de table.](images/table-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="1cf15-128">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="1cf15-128">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="1cf15-129">Les valeurs de tous les canaux des propriétés de transfert de table sont sans unité et ont un minimum de 0,0 et un maximum de 1,0.</span><span class="sxs-lookup"><span data-stu-id="1cf15-129">The values of all channels of the table transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="1cf15-130">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="1cf15-130">Display name and index enumeration</span></span>                                           | <span data-ttu-id="1cf15-131">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="1cf15-131">Type and default value</span></span>                       | <span data-ttu-id="1cf15-132">Description</span><span class="sxs-lookup"><span data-stu-id="1cf15-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf15-133">RedTable</span><span class="sxs-lookup"><span data-stu-id="1cf15-133">RedTable</span></span><br/> <span data-ttu-id="1cf15-134">\_ \_ \_ Table rouge d2d1 TABLETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="1cf15-134">D2D1\_TABLETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="1cf15-135">DISSOCIÉ\[\]</span><span class="sxs-lookup"><span data-stu-id="1cf15-135">FLOAT\[\]</span></span><br/> <span data-ttu-id="1cf15-136">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="1cf15-136">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="1cf15-137">Liste des valeurs utilisées pour définir la fonction de transfert pour le canal rouge.</span><span class="sxs-lookup"><span data-stu-id="1cf15-137">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1cf15-138">RedDisable</span><span class="sxs-lookup"><span data-stu-id="1cf15-138">RedDisable</span></span><br/> <span data-ttu-id="1cf15-139">D2D1 \_ TABLETRANSFER \_ prop \_ rouge \_ Disable</span><span class="sxs-lookup"><span data-stu-id="1cf15-139">D2D1\_TABLETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="1cf15-140">BOOL</span><span class="sxs-lookup"><span data-stu-id="1cf15-140">BOOL</span></span><br/> <span data-ttu-id="1cf15-141">FALSE</span><span class="sxs-lookup"><span data-stu-id="1cf15-141">FALSE</span></span><br/>             | <span data-ttu-id="1cf15-142">Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal rouge.</span><span class="sxs-lookup"><span data-stu-id="1cf15-142">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="1cf15-143">Si vous définissez cette valeur sur FALSe, elle applique la fonction RedTableTransfer au canal rouge.</span><span class="sxs-lookup"><span data-stu-id="1cf15-143">If you set this to FALSE it applies the RedTableTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="1cf15-144">GreenTable</span><span class="sxs-lookup"><span data-stu-id="1cf15-144">GreenTable</span></span><br/> <span data-ttu-id="1cf15-145">\_ \_ \_ Table verte d2d1 TABLETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="1cf15-145">D2D1\_TABLETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="1cf15-146">DISSOCIÉ\[\]</span><span class="sxs-lookup"><span data-stu-id="1cf15-146">FLOAT\[\]</span></span><br/> <span data-ttu-id="1cf15-147">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="1cf15-147">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="1cf15-148">Liste des valeurs utilisées pour définir la fonction de transfert pour le canal vert.</span><span class="sxs-lookup"><span data-stu-id="1cf15-148">The list of values used to define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1cf15-149">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="1cf15-149">GreenDisable</span></span><br/> <span data-ttu-id="1cf15-150">D2D1 \_ TABLETRANSFER \_ prop \_ vert \_ Disable</span><span class="sxs-lookup"><span data-stu-id="1cf15-150">D2D1\_TABLETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="1cf15-151">BOOL</span><span class="sxs-lookup"><span data-stu-id="1cf15-151">BOOL</span></span><br/> <span data-ttu-id="1cf15-152">FALSE</span><span class="sxs-lookup"><span data-stu-id="1cf15-152">FALSE</span></span><br/>             | <span data-ttu-id="1cf15-153">Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal vert.</span><span class="sxs-lookup"><span data-stu-id="1cf15-153">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="1cf15-154">Si vous définissez cette valeur sur FALSe, elle applique la fonction GreenTableTransfer au canal vert.</span><span class="sxs-lookup"><span data-stu-id="1cf15-154">If you set this to FALSE it applies the GreenTableTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1cf15-155">BlueTable</span><span class="sxs-lookup"><span data-stu-id="1cf15-155">BlueTable</span></span><br/> <span data-ttu-id="1cf15-156">\_ \_ \_ Table bleue d2d1 TABLETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="1cf15-156">D2D1\_TABLETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="1cf15-157">DISSOCIÉ\[\]</span><span class="sxs-lookup"><span data-stu-id="1cf15-157">FLOAT\[\]</span></span><br/> <span data-ttu-id="1cf15-158">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="1cf15-158">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="1cf15-159">Liste des valeurs utilisées pour définir la fonction de transfert pour le canal bleu.</span><span class="sxs-lookup"><span data-stu-id="1cf15-159">The list of values used to define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="1cf15-160">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="1cf15-160">BlueDisable</span></span><br/> <span data-ttu-id="1cf15-161">D2D1 \_ TABLETRANSFER \_ prop \_ bleu \_ Disable</span><span class="sxs-lookup"><span data-stu-id="1cf15-161">D2D1\_TABLETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="1cf15-162">BOOL</span><span class="sxs-lookup"><span data-stu-id="1cf15-162">BOOL</span></span><br/> <span data-ttu-id="1cf15-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="1cf15-163">FALSE</span></span><br/>             | <span data-ttu-id="1cf15-164">Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal bleu.</span><span class="sxs-lookup"><span data-stu-id="1cf15-164">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="1cf15-165">Si vous définissez cette valeur sur FALSe, elle applique la fonction BlueTableTransfer au canal bleu.</span><span class="sxs-lookup"><span data-stu-id="1cf15-165">If you set this to FALSE it applies the BlueTableTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1cf15-166">AlphaTable</span><span class="sxs-lookup"><span data-stu-id="1cf15-166">AlphaTable</span></span><br/> <span data-ttu-id="1cf15-167">\_ \_ \_ \_ Table alpha de transfert de table d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="1cf15-167">D2D1\_TABLE\_TRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>   | <span data-ttu-id="1cf15-168">DISSOCIÉ\[\]</span><span class="sxs-lookup"><span data-stu-id="1cf15-168">FLOAT\[\]</span></span><br/> <span data-ttu-id="1cf15-169">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="1cf15-169">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="1cf15-170">Liste des valeurs utilisées pour définir la fonction de transfert pour le canal alpha.</span><span class="sxs-lookup"><span data-stu-id="1cf15-170">The list of values used to define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1cf15-171">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="1cf15-171">AlphaDisable</span></span><br/> <span data-ttu-id="1cf15-172">D2D1 \_ TABLETRANSFER \_ prop \_ alpha \_ Disable</span><span class="sxs-lookup"><span data-stu-id="1cf15-172">D2D1\_TABLETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="1cf15-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="1cf15-173">BOOL</span></span><br/> <span data-ttu-id="1cf15-174">FALSE</span><span class="sxs-lookup"><span data-stu-id="1cf15-174">FALSE</span></span><br/>             | <span data-ttu-id="1cf15-175">Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal alpha.</span><span class="sxs-lookup"><span data-stu-id="1cf15-175">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="1cf15-176">Si vous définissez cette valeur sur FALSe, elle applique la fonction AlphaTableTransfer au canal alpha.</span><span class="sxs-lookup"><span data-stu-id="1cf15-176">If you set this to FALSE it applies the AlphaTableTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1cf15-177">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="1cf15-177">ClampOutput</span></span><br/> <span data-ttu-id="1cf15-178">\_Sortie de Clamp d2d1 TABLETRANSFER \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cf15-178">D2D1\_TABLETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="1cf15-179">BOOL</span><span class="sxs-lookup"><span data-stu-id="1cf15-179">BOOL</span></span><br/> <span data-ttu-id="1cf15-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="1cf15-180">FALSE</span></span><br/>             | <span data-ttu-id="1cf15-181">Si l’effet fixe les valeurs de couleur entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="1cf15-181">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="1cf15-182">L’effet serre les valeurs avant de prémultiplier le alpha.</span><span class="sxs-lookup"><span data-stu-id="1cf15-182">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="1cf15-183">Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées.</span><span class="sxs-lookup"><span data-stu-id="1cf15-183">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="1cf15-184">Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.</span><span class="sxs-lookup"><span data-stu-id="1cf15-184">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1cf15-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cf15-185">Requirements</span></span>



| <span data-ttu-id="1cf15-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cf15-186">Requirement</span></span> | <span data-ttu-id="1cf15-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cf15-187">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf15-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf15-188">Minimum supported client</span></span> | <span data-ttu-id="1cf15-189">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="1cf15-189">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1cf15-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf15-190">Minimum supported server</span></span> | <span data-ttu-id="1cf15-191">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="1cf15-191">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1cf15-192">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cf15-192">Header</span></span>                   | <span data-ttu-id="1cf15-193">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="1cf15-193">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="1cf15-194">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1cf15-194">Library</span></span>                  | <span data-ttu-id="1cf15-195">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="1cf15-195">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="1cf15-196">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1cf15-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cf15-197">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="1cf15-197">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

