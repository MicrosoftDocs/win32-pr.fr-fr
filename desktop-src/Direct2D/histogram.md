---
title: Effet d’histogramme
description: Utilisez l’effet histogramme pour générer un histogramme pour l’image bitmap d’entrée en fonction du nombre spécifié d’emplacements.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- effet d’histogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384492"
---
# <a name="histogram-effect"></a><span data-ttu-id="0bf42-104">Effet d’histogramme</span><span class="sxs-lookup"><span data-stu-id="0bf42-104">Histogram effect</span></span>

<span data-ttu-id="0bf42-105">Utilisez l’effet histogramme pour générer un histogramme pour l’image bitmap d’entrée en fonction du nombre spécifié d’emplacements.</span><span class="sxs-lookup"><span data-stu-id="0bf42-105">Use the histogram effect to generate a histogram for the input bitmap based on the specified number of bins.</span></span>

<span data-ttu-id="0bf42-106">Le CLSID de cet effet est CLSID \_ D2D1Histogram.</span><span class="sxs-lookup"><span data-stu-id="0bf42-106">The CLSID for this effect is CLSID\_D2D1Histogram.</span></span>

-   [<span data-ttu-id="0bf42-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="0bf42-107">Example</span></span>](#example)
-   [<span data-ttu-id="0bf42-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="0bf42-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="0bf42-109">Sélecteurs de canaux</span><span class="sxs-lookup"><span data-stu-id="0bf42-109">Channel selectors</span></span>](#channel-selectors)
-   [<span data-ttu-id="0bf42-110">Sortie des données</span><span class="sxs-lookup"><span data-stu-id="0bf42-110">Data output</span></span>](#data-output)
-   [<span data-ttu-id="0bf42-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="0bf42-111">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="0bf42-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bf42-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0bf42-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0bf42-113">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="0bf42-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="0bf42-114">Example</span></span>



| <span data-ttu-id="0bf42-115">Avant</span><span class="sxs-lookup"><span data-stu-id="0bf42-115">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| <span data-ttu-id="0bf42-117">Graphique des données de sortie de l’histogramme</span><span class="sxs-lookup"><span data-stu-id="0bf42-117">Graph of the histogram output data</span></span>                         |
| ![image après la transformation.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a><span data-ttu-id="0bf42-119">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="0bf42-119">Effect properties</span></span>

<span data-ttu-id="0bf42-120">Voici l’équation permettant de générer la sortie.</span><span class="sxs-lookup"><span data-stu-id="0bf42-120">Here's the equation to generate the output.</span></span>

![équation permettant de générer la sortie de l’effet de l’histogramme.](images/histogram-formula.png)

<span data-ttu-id="0bf42-122">la valeur de *i* est comprise entre 0 et le nombre d’emplacements. L’effet génère un histogramme pour les valeurs de pixel comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="0bf42-122">*i* is evaluated from 0 to the number of bins. The effect generates a histogram for pixel values between 0 and 1.</span></span> <span data-ttu-id="0bf42-123">Les valeurs en dehors de cette plage sont ancrées à la plage.</span><span class="sxs-lookup"><span data-stu-id="0bf42-123">Values outside of this range are clamped to the range.</span></span> <span data-ttu-id="0bf42-124">La plage d’un compartiment particulier dépend du nombre de compartiments.</span><span class="sxs-lookup"><span data-stu-id="0bf42-124">The range of a particular bucket depends on the number of buckets.</span></span> <span data-ttu-id="0bf42-125">Cet effet fonctionne sur des pixels de bitmap droits.</span><span class="sxs-lookup"><span data-stu-id="0bf42-125">This effect works on straight bitmap pixels.</span></span> <span data-ttu-id="0bf42-126">Les canaux de couleur de la bitmap d’entrée sont divisés par le canal alpha pour calculer cet effet.</span><span class="sxs-lookup"><span data-stu-id="0bf42-126">The color channels of the input bitmap are divided by the alpha channel to compute this effect.</span></span>



| <span data-ttu-id="0bf42-127">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="0bf42-127">Display name and index enumeration</span></span>                                             | <span data-ttu-id="0bf42-128">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="0bf42-128">Type and default value</span></span>                                                   | <span data-ttu-id="0bf42-129">Description</span><span class="sxs-lookup"><span data-stu-id="0bf42-129">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf42-130">NumBins</span><span class="sxs-lookup"><span data-stu-id="0bf42-130">NumBins</span></span><br/> <span data-ttu-id="0bf42-131">D2D1 de l' \_ histogramme \_ prop \_ nombre d' \_ emplacements</span><span class="sxs-lookup"><span data-stu-id="0bf42-131">D2D1\_HISTOGRAM\_PROP\_NUM\_BINS</span></span><br/>                 | <span data-ttu-id="0bf42-132">UINT32</span><span class="sxs-lookup"><span data-stu-id="0bf42-132">UINT32</span></span><br/> <span data-ttu-id="0bf42-133">256</span><span class="sxs-lookup"><span data-stu-id="0bf42-133">256</span></span><br/>                                         | <span data-ttu-id="0bf42-134">Spécifie le nombre d’emplacements utilisés pour l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="0bf42-134">Specifies the number of bins used for the histogram.</span></span> <span data-ttu-id="0bf42-135">La plage de valeurs d’intensité qui se trouvent dans un compartiment particulier dépend du nombre de compartiments spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0bf42-135">The range of intensity values that fall into a particular bucket depend on the number of specified buckets.</span></span>                              |
| <span data-ttu-id="0bf42-136">ChannelSelect</span><span class="sxs-lookup"><span data-stu-id="0bf42-136">ChannelSelect</span></span><br/> <span data-ttu-id="0bf42-137">\_Sélection du \_ \_ canal \_ d2d1 de l’histogramme</span><span class="sxs-lookup"><span data-stu-id="0bf42-137">D2D1\_HISTOGRAM\_PROP\_CHANNEL\_SELECT</span></span><br/>     | <span data-ttu-id="0bf42-138">\_Sélecteur de canal d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="0bf42-138">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="0bf42-139">\_Sélecteur de canal d2d1 \_ \_ R</span><span class="sxs-lookup"><span data-stu-id="0bf42-139">D2D1\_CHANNEL\_SELECTOR\_R</span></span><br/> | <span data-ttu-id="0bf42-140">Spécifie le canal utilisé pour générer l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="0bf42-140">Specifies the channel used to generate the histogram.</span></span> <span data-ttu-id="0bf42-141">Cet effet a une sortie de données unique correspondant au canal spécifié.</span><span class="sxs-lookup"><span data-stu-id="0bf42-141">This effect has a single data output corresponding to the specified channel.</span></span> <span data-ttu-id="0bf42-142">Pour plus d’informations, consultez [sélecteurs de canaux](#channel-selectors) .</span><span class="sxs-lookup"><span data-stu-id="0bf42-142">See [Channel selectors](#channel-selectors) for more info.</span></span> |
| <span data-ttu-id="0bf42-143">HistogramOutput</span><span class="sxs-lookup"><span data-stu-id="0bf42-143">HistogramOutput</span></span><br/> <span data-ttu-id="0bf42-144">Sortie de l’histogramme D2D1 de l' \_ histogramme \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="0bf42-144">D2D1\_HISTOGRAM\_PROP\_HISTOGRAM\_OUTPUT</span></span><br/> | <span data-ttu-id="0bf42-145">DISSOCIÉ\[\]</span><span class="sxs-lookup"><span data-stu-id="0bf42-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="0bf42-146">Propriété de sortie uniquement.</span><span class="sxs-lookup"><span data-stu-id="0bf42-146">Output property only.</span></span><br/>                    | <span data-ttu-id="0bf42-147">Tableau de sortie.</span><span class="sxs-lookup"><span data-stu-id="0bf42-147">The output array.</span></span>                                                                                                                                                                             |



 

## <a name="channel-selectors"></a><span data-ttu-id="0bf42-148">Sélecteurs de canaux</span><span class="sxs-lookup"><span data-stu-id="0bf42-148">Channel selectors</span></span>



| <span data-ttu-id="0bf42-149">Énumération</span><span class="sxs-lookup"><span data-stu-id="0bf42-149">Enumeration</span></span>                | <span data-ttu-id="0bf42-150">Description</span><span class="sxs-lookup"><span data-stu-id="0bf42-150">Description</span></span>                                                           |
|----------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0bf42-151">\_Sélecteur de canal d2d1 \_ \_ R</span><span class="sxs-lookup"><span data-stu-id="0bf42-151">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="0bf42-152">L’effet génère la sortie de l’histogramme en fonction du canal rouge.</span><span class="sxs-lookup"><span data-stu-id="0bf42-152">The effect generates the histogram output based on the red channel.</span></span>   |
| <span data-ttu-id="0bf42-153">\_Sélecteur de canal d2d1 \_ \_ G</span><span class="sxs-lookup"><span data-stu-id="0bf42-153">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="0bf42-154">L’effet génère la sortie de l’histogramme en fonction du canal vert.</span><span class="sxs-lookup"><span data-stu-id="0bf42-154">The effect generates the histogram output based on the green channel.</span></span> |
| <span data-ttu-id="0bf42-155">\_Sélecteur de canal d2d1 \_ \_ B</span><span class="sxs-lookup"><span data-stu-id="0bf42-155">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="0bf42-156">L’effet génère la sortie de l’histogramme en fonction du canal bleu.</span><span class="sxs-lookup"><span data-stu-id="0bf42-156">The effect generates the histogram output based on the blue channel.</span></span>  |
| <span data-ttu-id="0bf42-157">\_ \_ Sélecteur de canal d2d1 \_ A</span><span class="sxs-lookup"><span data-stu-id="0bf42-157">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="0bf42-158">L’effet génère la sortie de l’histogramme en fonction du canal alpha.</span><span class="sxs-lookup"><span data-stu-id="0bf42-158">The effect generates the histogram output based on the alpha channel.</span></span> |



 

## <a name="data-output"></a><span data-ttu-id="0bf42-159">Sortie des données</span><span class="sxs-lookup"><span data-stu-id="0bf42-159">Data output</span></span>

<span data-ttu-id="0bf42-160">Cet effet génère une valeur FLOAT \[ \] , avec le nombre d’éléments correspondant au nombre d’emplacements spécifiés. Chaque élément de la \[ \] valeur float est un float.</span><span class="sxs-lookup"><span data-stu-id="0bf42-160">This effect outputs a FLOAT\[\], with the number of elements corresponding to the number of specified bins. Each element in the FLOAT\[\] is a float.</span></span> <span data-ttu-id="0bf42-161">La valeur de l’élément correspond au nombre d’éléments dans cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="0bf42-161">The value of the element corresponds to the number of elements in that bin.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bf42-162">Notes</span><span class="sxs-lookup"><span data-stu-id="0bf42-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0bf42-163">La méthode [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) échoue si l’appareil ne prend pas en charge DirectCompute et retourne HRESULT = D2DERR \_ fonctionnalités d’appareil insuffisantes \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0bf42-163">The [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method fails if the device doesn't support DirectCompute and returns HRESULT = D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES.</span></span> <span data-ttu-id="0bf42-164">Toutes les cartes DirectX11 et DirectX10 qui prennent en charge DirectCompute peuvent utiliser l’effet.</span><span class="sxs-lookup"><span data-stu-id="0bf42-164">All DirectX11 cards and DirectX10 cards that support DirectCompute can use the effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0bf42-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bf42-165">Requirements</span></span>



| <span data-ttu-id="0bf42-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bf42-166">Requirement</span></span> | <span data-ttu-id="0bf42-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bf42-167">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf42-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bf42-168">Minimum supported client</span></span> | <span data-ttu-id="0bf42-169">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="0bf42-169">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0bf42-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bf42-170">Minimum supported server</span></span> | <span data-ttu-id="0bf42-171">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="0bf42-171">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0bf42-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bf42-172">Header</span></span>                   | <span data-ttu-id="0bf42-173">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="0bf42-173">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="0bf42-174">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0bf42-174">Library</span></span>                  | <span data-ttu-id="0bf42-175">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="0bf42-175">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0bf42-176">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0bf42-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bf42-177">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="0bf42-177">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

