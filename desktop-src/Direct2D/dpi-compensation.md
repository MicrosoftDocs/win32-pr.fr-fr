---
title: Effet de compensation DPI
description: Utilisez l’effet compensation DPI pour ajuster automatiquement une image bitmap d’entrée afin qu’elle corresponde à la valeur PPP du contexte. Cela est utile dans les situations où une image bitmap est créée ou chargée à une résolution différente de celle de l’écran.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844422"
---
# <a name="dpi-compensation-effect"></a><span data-ttu-id="d60b8-104">Effet de compensation DPI</span><span class="sxs-lookup"><span data-stu-id="d60b8-104">DPI compensation effect</span></span>

<span data-ttu-id="d60b8-105">Utilisez l’effet compensation DPI pour ajuster automatiquement une image bitmap d’entrée afin qu’elle corresponde à la valeur PPP du contexte.</span><span class="sxs-lookup"><span data-stu-id="d60b8-105">Use the DPI compensation effect to automatically adjust an input bitmap to match the DPI of the context.</span></span> <span data-ttu-id="d60b8-106">Cela est utile dans les situations où une image bitmap est créée ou chargée à une résolution différente de celle de l’écran.</span><span class="sxs-lookup"><span data-stu-id="d60b8-106">This is useful for situations where a bitmap is created or loaded at a different DPI than the screen.</span></span>

<span data-ttu-id="d60b8-107">Le CLSID de cet effet est CLSID \_ D2D1DpiCompensation.</span><span class="sxs-lookup"><span data-stu-id="d60b8-107">The CLSID for this effect is CLSID\_D2D1DpiCompensation.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="d60b8-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="d60b8-108">Effect properties</span></span>



| <span data-ttu-id="d60b8-109">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="d60b8-109">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="d60b8-110">Description</span><span class="sxs-lookup"><span data-stu-id="d60b8-110">Description</span></span>                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d60b8-111">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="d60b8-111">InterpolationMode</span></span><br/> <span data-ttu-id="d60b8-112">\_Mode d’interpolation d2d1 DPICOMPENSATION \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="d60b8-112">D2D1\_DPICOMPENSATION\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="d60b8-113">Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="d60b8-113">The interpolation mode the effect uses to scale the image.</span></span><br/> <span data-ttu-id="d60b8-114">Le type est D2D1 \_ DPICOMPENSATION \_ interpolation \_ mode.</span><span class="sxs-lookup"><span data-stu-id="d60b8-114">The type is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="d60b8-115">La valeur par défaut est D2D1 \_ DPICOMPENSATION \_ interpolation \_ mode \_ Linear.</span><span class="sxs-lookup"><span data-stu-id="d60b8-115">The default value is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR .</span></span><br/>                  |
| <span data-ttu-id="d60b8-116">BorderMode</span><span class="sxs-lookup"><span data-stu-id="d60b8-116">BorderMode</span></span><br/> <span data-ttu-id="d60b8-117">\_Mode de bordure d2d1 DPICOMPENSATION \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="d60b8-117">D2D1\_DPICOMPENSATION\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="d60b8-118">Le mode utilisé pour calculer la bordure de l’image, soft ou Hard.</span><span class="sxs-lookup"><span data-stu-id="d60b8-118">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="d60b8-119">Pour plus d’informations, consultez [modes de bordure](https://www.bing.com/search?q=Border+modes) .</span><span class="sxs-lookup"><span data-stu-id="d60b8-119">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span> <br/> <span data-ttu-id="d60b8-120">Le type est D2D1 \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="d60b8-120">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="d60b8-121">La valeur par défaut est \_ d2d1 \_ en mode bordure \_ souple.</span><span class="sxs-lookup"><span data-stu-id="d60b8-121">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/> |
| <span data-ttu-id="d60b8-122">InputDpi</span><span class="sxs-lookup"><span data-stu-id="d60b8-122">InputDpi</span></span><br/> <span data-ttu-id="d60b8-123">D2D1 \_ DPICOMPENSATION \_ prop \_ entrée \_ PPP</span><span class="sxs-lookup"><span data-stu-id="d60b8-123">D2D1\_DPICOMPENSATION\_PROP\_INPUT\_DPI</span></span><br/>                   | <span data-ttu-id="d60b8-124">PPP de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d60b8-124">The DPI of the input image.</span></span><br/> <span data-ttu-id="d60b8-125">Le type est FLOAT.</span><span class="sxs-lookup"><span data-stu-id="d60b8-125">The type is FLOAT.</span></span><br/> <span data-ttu-id="d60b8-126">La valeur par défaut est 96.0 f.</span><span class="sxs-lookup"><span data-stu-id="d60b8-126">The default value is 96.0f.</span></span><br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a><span data-ttu-id="d60b8-127">Modes d’interpolation</span><span class="sxs-lookup"><span data-stu-id="d60b8-127">Interpolation modes</span></span>



| <span data-ttu-id="d60b8-128">Énumération</span><span class="sxs-lookup"><span data-stu-id="d60b8-128">Enumeration</span></span>                                                       | <span data-ttu-id="d60b8-129">Description</span><span class="sxs-lookup"><span data-stu-id="d60b8-129">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d60b8-130">\_Mode d’interpolation d2d1 DPICOMPENSATION \_ \_ \_ le plus proche \_ voisin</span><span class="sxs-lookup"><span data-stu-id="d60b8-130">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="d60b8-131">Échantillonne le point unique le plus proche et l’utilise.</span><span class="sxs-lookup"><span data-stu-id="d60b8-131">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="d60b8-132">Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.</span><span class="sxs-lookup"><span data-stu-id="d60b8-132">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="d60b8-133">D2D1 \_ \_ mode d’interpolation \_ DPICOMPENSATION \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="d60b8-133">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="d60b8-134">Utilise un échantillon à quatre points et une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="d60b8-134">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="d60b8-135">Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="d60b8-135">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="d60b8-136">D2D1 \_ DPICOMPENSATION \_ mode d' \_ interpolation \_ cubique</span><span class="sxs-lookup"><span data-stu-id="d60b8-136">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="d60b8-137">Utilise un exemple de noyau cubique 16 pour l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="d60b8-137">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="d60b8-138">Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="d60b8-138">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="d60b8-139">\_Mode d’interpolation d2d1 DPICOMPENSATION multi- \_ \_ \_ \_ exemple \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="d60b8-139">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="d60b8-140">Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="d60b8-140">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="d60b8-141">Ce mode est adapté à la réduction de la taille des images avec quelques pixels.</span><span class="sxs-lookup"><span data-stu-id="d60b8-141">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="d60b8-142">D2D1 \_ \_ mode d’interpolation \_ DPICOMPENSATION \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="d60b8-142">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="d60b8-143">Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="d60b8-143">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="d60b8-144">D2D1 \_ DPICOMPENSATION \_ mode d’interpolation de \_ \_ haute \_ qualité \_ cubique</span><span class="sxs-lookup"><span data-stu-id="d60b8-144">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="d60b8-145">Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="d60b8-145">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="d60b8-146">Utilise ensuite le mode d’interpolation cubique pour la sortie finale.</span><span class="sxs-lookup"><span data-stu-id="d60b8-146">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="d60b8-147">Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ DPICOMPENSTION \_ interpolation \_ mode \_ Linear.</span><span class="sxs-lookup"><span data-stu-id="d60b8-147">If you don't select a mode, the effect defaults to D2D1\_DPICOMPENSTION\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="d60b8-148">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="d60b8-148">Border modes</span></span>



| <span data-ttu-id="d60b8-149">Nom</span><span class="sxs-lookup"><span data-stu-id="d60b8-149">Name</span></span>                     | <span data-ttu-id="d60b8-150">Description</span><span class="sxs-lookup"><span data-stu-id="d60b8-150">Description</span></span>                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d60b8-151">\_Mode de bordure d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d60b8-151">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="d60b8-152">Les pixels en dehors des limites d’entrée sont générés par l' [effet de bordure de miroir](border.md).</span><span class="sxs-lookup"><span data-stu-id="d60b8-152">Pixels outside of the input boundaries are generated by the [mirror border effect](border.md).</span></span> <br/> |
| <span data-ttu-id="d60b8-153">D2D1 \_ mode de bordure \_ \_ difficile</span><span class="sxs-lookup"><span data-stu-id="d60b8-153">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="d60b8-154">Les pixels en dehors des limites d’entrée sont des noirs transparents.</span><span class="sxs-lookup"><span data-stu-id="d60b8-154">Pixels outside of the input boundaries are transparent black.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="d60b8-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d60b8-155">Requirements</span></span>



| <span data-ttu-id="d60b8-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d60b8-156">Requirement</span></span> | <span data-ttu-id="d60b8-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="d60b8-157">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d60b8-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d60b8-158">Minimum supported client</span></span> | <span data-ttu-id="d60b8-159">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d60b8-159">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d60b8-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d60b8-160">Minimum supported server</span></span> | <span data-ttu-id="d60b8-161">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d60b8-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d60b8-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="d60b8-162">Header</span></span>                   | <span data-ttu-id="d60b8-163">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="d60b8-163">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="d60b8-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d60b8-164">Library</span></span>                  | <span data-ttu-id="d60b8-165">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d60b8-165">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="d60b8-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d60b8-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d60b8-167">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="d60b8-167">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

