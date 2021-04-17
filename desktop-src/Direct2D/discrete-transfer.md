---
title: Effet de transfert discret
description: Utilisez l’effet de transfert discret pour mapper les intensités de couleur d’une image à l’aide d’une fonction de transfert par étape créée à partir d’une liste de valeurs que vous fournissez.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- effet de transfert discret
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104564742"
---
# <a name="discrete-transfer-effect"></a><span data-ttu-id="cb1a0-104">Effet de transfert discret</span><span class="sxs-lookup"><span data-stu-id="cb1a0-104">Discrete transfer effect</span></span>

<span data-ttu-id="cb1a0-105">Utilisez l’effet de transfert discret pour mapper les intensités de couleur d’une image à l’aide d’une fonction de transfert par étape créée à partir d’une liste de valeurs que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-105">Use the discrete transfer effect to map the color intensities of an image using a step transfer function created from a list of values you provide.</span></span>

<span data-ttu-id="cb1a0-106">Le CLSID de cet effet est CLSID \_ D2D1DiscreteTransfer.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-106">The CLSID for this effect is CLSID\_D2D1DiscreteTransfer.</span></span>

-   [<span data-ttu-id="cb1a0-107">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="cb1a0-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="cb1a0-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="cb1a0-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="cb1a0-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb1a0-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cb1a0-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb1a0-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="cb1a0-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="cb1a0-111">Example image</span></span>

<span data-ttu-id="cb1a0-112">L’image ci-dessous montre l’entrée et la sortie de l’effet de transfert discret.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-112">The image here shows the input and output of the discrete transfer effect.</span></span>



| <span data-ttu-id="cb1a0-113">Avant</span><span class="sxs-lookup"><span data-stu-id="cb1a0-113">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)        |
| <span data-ttu-id="cb1a0-115">After</span><span class="sxs-lookup"><span data-stu-id="cb1a0-115">After</span></span>                                                             |
| ![image après la transformation.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="cb1a0-117">La fonction de transfert est basée sur la liste des entrées : V = (v0, v1, v2, V3, V ?</span><span class="sxs-lookup"><span data-stu-id="cb1a0-117">The transfer function is based on the list of inputs: V=(V0,V1,V2,V3,V?</span></span> <span data-ttu-id="cb1a0-118">, V<sub>N</sub>), où N est le nombre d’éléments-1.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="cb1a0-119">L’intensité en pixels d’entrée est représentée par C. L’intensité en pixels de sortie, C est calculée avec l’équation :</span><span class="sxs-lookup"><span data-stu-id="cb1a0-119">The input pixel intensity is represented as C. The output pixel intensity, C  is calculated with the equation:</span></span>

<span data-ttu-id="cb1a0-120">Pour une valeur C, choisissez une valeur k, telle que :</span><span class="sxs-lookup"><span data-stu-id="cb1a0-120">For a value C, pick a value k, such that:</span></span>

![formule du processus.](images/discrete-transfer1.png)

<span data-ttu-id="cb1a0-122">La sortie C peut être calculée à l’aide de l’équation : C' = V ?</span><span class="sxs-lookup"><span data-stu-id="cb1a0-122">The output C  can be calculated using the equation: C' = V?</span></span>

<span data-ttu-id="cb1a0-123">Cet effet fonctionne sur les images alpha directes et prémultipliées.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-123">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="cb1a0-124">L’effet génère des bitmaps alpha prémultipliés.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-124">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="cb1a0-125">Voici à quoi ressemble le graphique de la fonction de transfert discret si les entrées sont `[0.25, 0.5, 0.75, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="cb1a0-125">Here is what the graph of discrete transfer function looks like if the inputs are `[0.25, 0.5, 0.75, 1.0]`.</span></span>

![graphique d’intensité de pixel pour la fonction de transfert discrète.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="cb1a0-127">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="cb1a0-127">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="cb1a0-128">Les valeurs de tous les canaux des propriétés de transfert discrètes sont sans unité et ont un minimum de 0,0 et un maximum de 1,0.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-128">The values of all channels of the discrete transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="cb1a0-129">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="cb1a0-129">Display name and index enumeration</span></span>                                              | <span data-ttu-id="cb1a0-130">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="cb1a0-130">Type and default value</span></span>                       | <span data-ttu-id="cb1a0-131">Description</span><span class="sxs-lookup"><span data-stu-id="cb1a0-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb1a0-132">RedTable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-132">RedTable</span></span><br/> <span data-ttu-id="cb1a0-133">\_ \_ \_ Table rouge d2d1 DISCRETETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="cb1a0-133">D2D1\_DISCRETETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="cb1a0-134">DISSOCIÉ\[\]</span><span class="sxs-lookup"><span data-stu-id="cb1a0-134">FLOAT\[\]</span></span><br/> <span data-ttu-id="cb1a0-135">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cb1a0-135">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="cb1a0-136">Liste des valeurs utilisées pour définir la fonction de transfert pour le canal rouge.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-136">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cb1a0-137">RedDisable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-137">RedDisable</span></span><br/> <span data-ttu-id="cb1a0-138">D2D1 \_ DISCRETETRANSFER \_ prop \_ rouge \_ Disable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-138">D2D1\_DISCRETETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="cb1a0-139">BOOL</span><span class="sxs-lookup"><span data-stu-id="cb1a0-139">BOOL</span></span><br/> <span data-ttu-id="cb1a0-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="cb1a0-140">FALSE</span></span><br/>             | <span data-ttu-id="cb1a0-141">Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal rouge.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-141">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="cb1a0-142">Si vous affectez la valeur FALSe, l’effet applique la fonction RedDiscreteTransfer au canal rouge.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-142">If you set this to FALSE the effect applies the RedDiscreteTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cb1a0-143">GreenTable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-143">GreenTable</span></span><br/> <span data-ttu-id="cb1a0-144">\_ \_ \_ Table verte d2d1 DISCRETETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="cb1a0-144">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="cb1a0-145">DISSOCIÉ\[\]</span><span class="sxs-lookup"><span data-stu-id="cb1a0-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="cb1a0-146">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cb1a0-146">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="cb1a0-147">Liste des valeurs qui définissent la fonction de transfert pour le canal vert.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-147">The list of values that define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cb1a0-148">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-148">GreenDisable</span></span><br/> <span data-ttu-id="cb1a0-149">D2D1 \_ DISCRETETRANSFER \_ prop \_ vert \_ Disable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-149">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="cb1a0-150">BOOL</span><span class="sxs-lookup"><span data-stu-id="cb1a0-150">BOOL</span></span><br/> <span data-ttu-id="cb1a0-151">FALSE</span><span class="sxs-lookup"><span data-stu-id="cb1a0-151">FALSE</span></span><br/>             | <span data-ttu-id="cb1a0-152">Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal vert.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-152">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="cb1a0-153">Si vous affectez la valeur FALSe, l’effet applique la fonction GreenDiscreteTransfer au canal vert.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-153">If you set this to FALSE the effect applies the GreenDiscreteTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cb1a0-154">BlueTable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-154">BlueTable</span></span><br/> <span data-ttu-id="cb1a0-155">\_ \_ \_ Table bleue d2d1 DISCRETETRANSFER \_ prop</span><span class="sxs-lookup"><span data-stu-id="cb1a0-155">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="cb1a0-156">DISSOCIÉ\[\]</span><span class="sxs-lookup"><span data-stu-id="cb1a0-156">FLOAT\[\]</span></span><br/> <span data-ttu-id="cb1a0-157">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cb1a0-157">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="cb1a0-158">Liste des valeurs qui définissent la fonction de transfert pour le canal bleu.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-158">The list of values that define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cb1a0-159">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-159">BlueDisable</span></span><br/> <span data-ttu-id="cb1a0-160">D2D1 \_ DISCRETETRANSFER \_ prop \_ bleu \_ Disable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-160">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="cb1a0-161">BOOL</span><span class="sxs-lookup"><span data-stu-id="cb1a0-161">BOOL</span></span><br/> <span data-ttu-id="cb1a0-162">FALSE</span><span class="sxs-lookup"><span data-stu-id="cb1a0-162">FALSE</span></span><br/>             | <span data-ttu-id="cb1a0-163">Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal bleu.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-163">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="cb1a0-164">Si vous affectez la valeur FALSe, l’effet applique la fonction BlueDiscreteTransfer au canal bleu.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-164">If you set this to FALSE the effect applies the BlueDiscreteTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cb1a0-165">AlphaTable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-165">AlphaTable</span></span><br/> <span data-ttu-id="cb1a0-166">D2D1 \_ DISCRETETRANSFER \_ prop \_ alpha, \_ table</span><span class="sxs-lookup"><span data-stu-id="cb1a0-166">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>     | <span data-ttu-id="cb1a0-167">DISSOCIÉ\[\]</span><span class="sxs-lookup"><span data-stu-id="cb1a0-167">FLOAT\[\]</span></span><br/> <span data-ttu-id="cb1a0-168">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="cb1a0-168">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="cb1a0-169">Liste des valeurs qui définissent la fonction de transfert pour le canal alpha.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-169">The list of values that define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cb1a0-170">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-170">AlphaDisable</span></span><br/> <span data-ttu-id="cb1a0-171">D2D1 \_ DISCRETETRANSFER \_ prop \_ alpha \_ Disable</span><span class="sxs-lookup"><span data-stu-id="cb1a0-171">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="cb1a0-172">BOOL</span><span class="sxs-lookup"><span data-stu-id="cb1a0-172">BOOL</span></span><br/> <span data-ttu-id="cb1a0-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="cb1a0-173">FALSE</span></span><br/>             | <span data-ttu-id="cb1a0-174">Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal alpha.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-174">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="cb1a0-175">Si vous affectez la valeur FALSe, l’effet applique la fonction AlphaDiscreteTransfer au canal alpha.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-175">If you set this to FALSE the effect applies the AlphaDiscreteTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cb1a0-176">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="cb1a0-176">ClampOutput</span></span><br/> <span data-ttu-id="cb1a0-177">\_Sortie de Clamp d2d1 DISCRETETRANSFER \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="cb1a0-177">D2D1\_DISCRETETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="cb1a0-178">BOOL</span><span class="sxs-lookup"><span data-stu-id="cb1a0-178">BOOL</span></span><br/> <span data-ttu-id="cb1a0-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="cb1a0-179">FALSE</span></span><br/>             | <span data-ttu-id="cb1a0-180">Si l’effet fixe les valeurs de couleur entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-180">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="cb1a0-181">L’effet serre les valeurs avant de prémultiplier le alpha.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-181">The effect clamps the values before it premultiplies the alpha.</span></span><br/> <span data-ttu-id="cb1a0-182">Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-182">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="cb1a0-183">Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.</span><span class="sxs-lookup"><span data-stu-id="cb1a0-183">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb1a0-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb1a0-184">Requirements</span></span>



| <span data-ttu-id="cb1a0-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb1a0-185">Requirement</span></span> | <span data-ttu-id="cb1a0-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb1a0-186">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb1a0-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb1a0-187">Minimum supported client</span></span> | <span data-ttu-id="cb1a0-188">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="cb1a0-188">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cb1a0-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb1a0-189">Minimum supported server</span></span> | <span data-ttu-id="cb1a0-190">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="cb1a0-190">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cb1a0-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb1a0-191">Header</span></span>                   | <span data-ttu-id="cb1a0-192">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="cb1a0-192">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="cb1a0-193">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb1a0-193">Library</span></span>                  | <span data-ttu-id="cb1a0-194">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="cb1a0-194">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="cb1a0-195">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb1a0-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb1a0-196">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="cb1a0-196">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

