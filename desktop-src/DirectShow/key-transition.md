---
description: Transition de clé
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transition de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845974"
---
# <a name="key-transition"></a><span data-ttu-id="40785-103">Transition de clé</span><span class="sxs-lookup"><span data-stu-id="40785-103">Key Transition</span></span>

> [!Note]  
> <span data-ttu-id="40785-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="40785-104">\[Deprecated.</span></span> <span data-ttu-id="40785-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="40785-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="40785-106">La transition de clé effectue la génération de clés en fonction de la valeur RVB, de la valeur alpha, de la teinte ou de la luminance.</span><span class="sxs-lookup"><span data-stu-id="40785-106">The Key transition performs keying based on RGB value, alpha value, hue or luminance.</span></span>

<span data-ttu-id="40785-107">L’illustration suivante montre la transition de clé :</span><span class="sxs-lookup"><span data-stu-id="40785-107">The following image shows the key transition:</span></span>

![transition de clé](images/trans-key.png)

<span data-ttu-id="40785-109">ID de classe (CLSID) : {C5B19592-145E-11D3-9F04-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="40785-109">Class ID (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span></span>

<span data-ttu-id="40785-110">Nom de la variable CLSID : CLSID \_ DxtKey</span><span class="sxs-lookup"><span data-stu-id="40785-110">CLSID Variable Name: CLSID\_DxtKey</span></span>

<span data-ttu-id="40785-111">Nom convivial : « DxtKey »</span><span class="sxs-lookup"><span data-stu-id="40785-111">Friendly Name: "DxtKey"</span></span>

<span data-ttu-id="40785-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="40785-112">Properties</span></span>



| <span data-ttu-id="40785-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="40785-113">Property</span></span>   | <span data-ttu-id="40785-114">Type</span><span class="sxs-lookup"><span data-stu-id="40785-114">Type</span></span>  | <span data-ttu-id="40785-115">Plage valide</span><span class="sxs-lookup"><span data-stu-id="40785-115">Valid range</span></span>           | <span data-ttu-id="40785-116">Description</span><span class="sxs-lookup"><span data-stu-id="40785-116">Description</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="40785-117">S'applique à</span><span class="sxs-lookup"><span data-stu-id="40785-117">Applies To</span></span>                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="40785-118">Teinte</span><span class="sxs-lookup"><span data-stu-id="40785-118">Hue</span></span>        | <span data-ttu-id="40785-119">int</span><span class="sxs-lookup"><span data-stu-id="40785-119">int</span></span>   | <span data-ttu-id="40785-120">0 – 360</span><span class="sxs-lookup"><span data-stu-id="40785-120">0–360</span></span>                 | <span data-ttu-id="40785-121">Valeur de teinte sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="40785-121">The hue value on which to key.</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="40785-122">Teinte</span><span class="sxs-lookup"><span data-stu-id="40785-122">Hue</span></span>                            |
| <span data-ttu-id="40785-123">Inverser :</span><span class="sxs-lookup"><span data-stu-id="40785-123">Invert</span></span>     | <span data-ttu-id="40785-124">BOOL</span><span class="sxs-lookup"><span data-stu-id="40785-124">BOOL</span></span>  | <span data-ttu-id="40785-125">**False** ou **true**</span><span class="sxs-lookup"><span data-stu-id="40785-125">**FALSE** or **TRUE**</span></span> | <span data-ttu-id="40785-126">Valeur booléenne indiquant si l’opération par défaut de la clé doit être inversée.</span><span class="sxs-lookup"><span data-stu-id="40785-126">Boolean value indicating whether to invert the default operation of the key.</span></span> <span data-ttu-id="40785-127">Si la **valeur est false**, les pixels de l’image superposée sont rendus transparents par défaut.</span><span class="sxs-lookup"><span data-stu-id="40785-127">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span> <span data-ttu-id="40785-128">Si la **valeur est true**, l’opération est inversée.</span><span class="sxs-lookup"><span data-stu-id="40785-128">If **TRUE**, the operation inverts.</span></span>                                                   | <span data-ttu-id="40785-129">Chroma, teinte, luminance, Nonred</span><span class="sxs-lookup"><span data-stu-id="40785-129">Chroma, Hue, Luminance, Nonred</span></span> |
| <span data-ttu-id="40785-130">KeyType</span><span class="sxs-lookup"><span data-stu-id="40785-130">KeyType</span></span>    | <span data-ttu-id="40785-131">int</span><span class="sxs-lookup"><span data-stu-id="40785-131">int</span></span>   | <span data-ttu-id="40785-132">Voir les notes</span><span class="sxs-lookup"><span data-stu-id="40785-132">See Remarks</span></span>           | <span data-ttu-id="40785-133">Spécifie le type de clé.</span><span class="sxs-lookup"><span data-stu-id="40785-133">Specifies the type of key.</span></span> <span data-ttu-id="40785-134">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="40785-134">For more information, see Remarks.</span></span>                                                                                                                                                                                              | <span data-ttu-id="40785-135">Tous</span><span class="sxs-lookup"><span data-stu-id="40785-135">All</span></span>                            |
| <span data-ttu-id="40785-136">Luminance</span><span class="sxs-lookup"><span data-stu-id="40785-136">Luminance</span></span>  | <span data-ttu-id="40785-137">int</span><span class="sxs-lookup"><span data-stu-id="40785-137">int</span></span>   | <span data-ttu-id="40785-138">0 – 100</span><span class="sxs-lookup"><span data-stu-id="40785-138">0–100</span></span>                 | <span data-ttu-id="40785-139">Valeur de luminance sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="40785-139">The luminance value on which to key.</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="40785-140">Luminance</span><span class="sxs-lookup"><span data-stu-id="40785-140">Luminance</span></span>                      |
| <span data-ttu-id="40785-141">RGB</span><span class="sxs-lookup"><span data-stu-id="40785-141">RGB</span></span>        | <span data-ttu-id="40785-142">DWORD</span><span class="sxs-lookup"><span data-stu-id="40785-142">DWORD</span></span> | <span data-ttu-id="40785-143">0x0 – 0xFFFFFF</span><span class="sxs-lookup"><span data-stu-id="40785-143">0x0 – 0xFFFFFF</span></span>        | <span data-ttu-id="40785-144">Couleur sur laquelle la clé doit être représentée.</span><span class="sxs-lookup"><span data-stu-id="40785-144">The color on which to key.</span></span> <span data-ttu-id="40785-145">La valeur est un nombre hexadécimal au format 0x *RRVVBB*, où *RR* est la valeur rouge, *GG* est la valeur verte et *BB* est la valeur bleue.</span><span class="sxs-lookup"><span data-stu-id="40785-145">The value is a hexadecimal number with the format 0x *RRGGBB*, where *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="40785-146">(Les couleurs pures rouge, vert et bleu sont 0xFF0000, 0x00FF00 et 0x0000FF, respectivement).</span><span class="sxs-lookup"><span data-stu-id="40785-146">(Pure red, green, and blue are 0xFF0000, 0x00FF00, and 0x0000FF, respectively.)</span></span> | <span data-ttu-id="40785-147">Chromatique</span><span class="sxs-lookup"><span data-stu-id="40785-147">Chroma</span></span>                         |
| <span data-ttu-id="40785-148">Similarité</span><span class="sxs-lookup"><span data-stu-id="40785-148">Similarity</span></span> | <span data-ttu-id="40785-149">int</span><span class="sxs-lookup"><span data-stu-id="40785-149">int</span></span>   | <span data-ttu-id="40785-150">0 – 100</span><span class="sxs-lookup"><span data-stu-id="40785-150">0–100</span></span>                 | <span data-ttu-id="40785-151">Plage de données de couleur qui devient transparente.</span><span class="sxs-lookup"><span data-stu-id="40785-151">The range of color data that becomes transparent.</span></span> <span data-ttu-id="40785-152">À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente.</span><span class="sxs-lookup"><span data-stu-id="40785-152">At higher values, a wider range of similar colors is transparent.</span></span>                                                                                                                                        | <span data-ttu-id="40785-153">Chroma, Nonred</span><span class="sxs-lookup"><span data-stu-id="40785-153">Chroma, Nonred</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="40785-154">Notes</span><span class="sxs-lookup"><span data-stu-id="40785-154">Remarks</span></span>

<span data-ttu-id="40785-155">Le type de clé effectué dépend de la valeur de la propriété **KeyType** , qui doit être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="40785-155">The type of key that is performed depends on the value of the **KeyType** property, which must be one of the following:</span></span>



| <span data-ttu-id="40785-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="40785-156">Value</span></span> | <span data-ttu-id="40785-157">Énumération</span><span class="sxs-lookup"><span data-stu-id="40785-157">Enumeration</span></span>       | <span data-ttu-id="40785-158">Description</span><span class="sxs-lookup"><span data-stu-id="40785-158">Description</span></span>                                           |
|-------|-------------------|-------------------------------------------------------|
| <span data-ttu-id="40785-159">0</span><span class="sxs-lookup"><span data-stu-id="40785-159">0</span></span>     | <span data-ttu-id="40785-160">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="40785-160">DXTKEY\_RGB</span></span>       | <span data-ttu-id="40785-161">Clé Chroma (clé par valeur RVB).</span><span class="sxs-lookup"><span data-stu-id="40785-161">Chroma key (key by RGB value).</span></span>                        |
| <span data-ttu-id="40785-162">1</span><span class="sxs-lookup"><span data-stu-id="40785-162">1</span></span>     | <span data-ttu-id="40785-163">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="40785-163">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="40785-164">Clé Nonred.</span><span class="sxs-lookup"><span data-stu-id="40785-164">Nonred key.</span></span> <span data-ttu-id="40785-165">(Rend les zones bleues et vertes transparentes.)</span><span class="sxs-lookup"><span data-stu-id="40785-165">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="40785-166">2</span><span class="sxs-lookup"><span data-stu-id="40785-166">2</span></span>     | <span data-ttu-id="40785-167">\_luminance DXTKEY</span><span class="sxs-lookup"><span data-stu-id="40785-167">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="40785-168">Clé de luminance.</span><span class="sxs-lookup"><span data-stu-id="40785-168">Luminance key.</span></span>                                        |
| <span data-ttu-id="40785-169">3</span><span class="sxs-lookup"><span data-stu-id="40785-169">3</span></span>     | <span data-ttu-id="40785-170">DXTKEY \_ alpha</span><span class="sxs-lookup"><span data-stu-id="40785-170">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="40785-171">Clé par valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="40785-171">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="40785-172">4</span><span class="sxs-lookup"><span data-stu-id="40785-172">4</span></span>     | <span data-ttu-id="40785-173">DXTKEY \_ teinte</span><span class="sxs-lookup"><span data-stu-id="40785-173">DXTKEY\_HUE</span></span>       | <span data-ttu-id="40785-174">Clé par teinte.</span><span class="sxs-lookup"><span data-stu-id="40785-174">Key by hue.</span></span>                                           |



 

<span data-ttu-id="40785-175">Par défaut, le type de clé est DXTKEY \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="40785-175">The key type defaults to DXTKEY\_ALPHA.</span></span>

 

 



