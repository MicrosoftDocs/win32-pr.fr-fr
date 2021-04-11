---
title: Effet de mappage de déplacement
description: Utilisez l’effet de mappage de déplacement pour déplacer les pixels de l’image d’entrée selon les valeurs d’intensité d’une deuxième image d’entrée.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- effet de mappage de déplacement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102952"
---
# <a name="displacement-map-effect"></a><span data-ttu-id="bf3b7-104">Effet de mappage de déplacement</span><span class="sxs-lookup"><span data-stu-id="bf3b7-104">Displacement map effect</span></span>

<span data-ttu-id="bf3b7-105">Utilisez l’effet de mappage de déplacement pour déplacer les pixels de l’image d’entrée selon les valeurs d’intensité d’une deuxième image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-105">Use the displacement map effect to displace the pixels of the input image by the intensity values of a second input image.</span></span>

<span data-ttu-id="bf3b7-106">Le CLSID de cet effet est CLSID \_ D2D1DisplacementMap.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-106">The CLSID for this effect is CLSID\_D2D1DisplacementMap.</span></span>

-   [<span data-ttu-id="bf3b7-107">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="bf3b7-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="bf3b7-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="bf3b7-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="bf3b7-109">Canaux de couleur</span><span class="sxs-lookup"><span data-stu-id="bf3b7-109">Color channels</span></span>](#color-channels)
-   [<span data-ttu-id="bf3b7-110">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="bf3b7-110">Output Bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="bf3b7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf3b7-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bf3b7-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf3b7-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="bf3b7-113">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="bf3b7-113">Example image</span></span>



| <span data-ttu-id="bf3b7-114">Avant</span><span class="sxs-lookup"><span data-stu-id="bf3b7-114">Before</span></span>                                                           |
|------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)       |
| <span data-ttu-id="bf3b7-116">After</span><span class="sxs-lookup"><span data-stu-id="bf3b7-116">After</span></span>                                                            |
| ![image après la transformation.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="bf3b7-118">Les emplacements des pixels de la sortie sont déterminés à l’aide de la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="bf3b7-118">The locations of the pixels in the output are determined using this formula:</span></span>

<span data-ttu-id="bf3b7-119">C' (x, y) = C (x + Scale \* (XChannelSelector (bitmap de déplacement (x, y))-0.5), o + Scale \* (YChannelSelector (bitmap de déplacement (x, y))-0,5))</span><span class="sxs-lookup"><span data-stu-id="bf3b7-119">C' (x,y)=C(x+ scale\*(XChannelSelector(Displacement Bitmap (x,y))-0.5),y+ scale\*(YChannelSelector(Displacement Bitmap (x,y))-0.5))</span></span>

<span data-ttu-id="bf3b7-120">Où :</span><span class="sxs-lookup"><span data-stu-id="bf3b7-120">Where:</span></span><dl> <span data-ttu-id="bf3b7-121">*C (x, y)* est le pixel de sortie à (x, y).</span><span class="sxs-lookup"><span data-stu-id="bf3b7-121">*C  (x, y)* is the output pixel at (x, y).</span></span>  
<span data-ttu-id="bf3b7-122">*C (x, y)* est le pixel d’entrée à (x, y).</span><span class="sxs-lookup"><span data-stu-id="bf3b7-122">*C (x, y)* is the input pixel at (x, y).</span></span>  
<span data-ttu-id="bf3b7-123">*Bitmap de déplacement (x, y)* est l’intensité de pixel de déplacement aux coordonnées spécifiées</span><span class="sxs-lookup"><span data-stu-id="bf3b7-123">*Displacement Bitmap (x, y)* is the displacement pixel intensity at the specified coordinates</span></span>  
<span data-ttu-id="bf3b7-124">*XChannelSelector* l’intensité du canal RVBA sélectionné à partir de l’image bitmap de déplacement qui place l’image d’entrée dans l’axe X.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-124">*XChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the X direction.</span></span>  
<span data-ttu-id="bf3b7-125">*YChannelSelector* l’intensité du canal RVBA sélectionné à partir de l’image bitmap de déplacement qui place l’image d’entrée dans l’axe Y.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-125">*YChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the Y direction.</span></span>  
</dl>

<span data-ttu-id="bf3b7-126">L’effet rééchantillonne l’image d’entrée en fonction de la propriété Scale et de l’intensité de l’image de déplacement.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-126">The effect resamples the input image according to the scale property and the intensity of the displacement image.</span></span> <span data-ttu-id="bf3b7-127">Il utilise l’interpolation bilinéaire en cas d’échantillonnage entre les pixels de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-127">It uses bilinear interpolation if sampling from between pixels in the input image.</span></span>

<span data-ttu-id="bf3b7-128">Cet effet fonctionne sur les images alpha directes et prémultipliées.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-128">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="bf3b7-129">Le format alpha de sortie est le même que le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-129">The output alpha format is the same as the input format.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="bf3b7-130">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="bf3b7-130">Effect properties</span></span>



| <span data-ttu-id="bf3b7-131">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="bf3b7-131">Display name and index enumeration</span></span>                                                   | <span data-ttu-id="bf3b7-132">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="bf3b7-132">Type and default value</span></span>                                                   | <span data-ttu-id="bf3b7-133">Description</span><span class="sxs-lookup"><span data-stu-id="bf3b7-133">Description</span></span>                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf3b7-134">Scale</span><span class="sxs-lookup"><span data-stu-id="bf3b7-134">Scale</span></span><br/> <span data-ttu-id="bf3b7-135">\_Échelle d2d1 DISPLACEMENTMAP \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="bf3b7-135">D2D1\_DISPLACEMENTMAP\_PROP\_SCALE</span></span><br/>                       | <span data-ttu-id="bf3b7-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bf3b7-136">FLOAT</span></span><br/> <span data-ttu-id="bf3b7-137">0.0f</span><span class="sxs-lookup"><span data-stu-id="bf3b7-137">0.0f</span></span><br/>                                         | <span data-ttu-id="bf3b7-138">Multiplie l’intensité du canal sélectionné à partir de l’image de déplacement.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-138">Multiplies the intensity of the selected channel from the displacement image.</span></span> <span data-ttu-id="bf3b7-139">Plus vous définissez cette propriété, plus l’effet déplace les pixels</span><span class="sxs-lookup"><span data-stu-id="bf3b7-139">The higher you set this property, the more the effect displaces the pixels</span></span><br/>                       |
| <span data-ttu-id="bf3b7-140">XChannelSelect</span><span class="sxs-lookup"><span data-stu-id="bf3b7-140">XChannelSelect</span></span><br/> <span data-ttu-id="bf3b7-141">D2D1 \_ DISPLACEMENTMAP \_ prop \_ X \_ canal \_ Select</span><span class="sxs-lookup"><span data-stu-id="bf3b7-141">D2D1\_DISPLACEMENTMAP\_PROP\_X\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="bf3b7-142">\_Sélecteur de canal d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="bf3b7-142">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="bf3b7-143">\_ \_ Sélecteur de canal d2d1 \_ A</span><span class="sxs-lookup"><span data-stu-id="bf3b7-143">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="bf3b7-144">L’effet extrait l’intensité de ce canal de couleur et l’utilise pour déplacer spatialement l’image dans la direction X.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-144">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the X direction.</span></span> <span data-ttu-id="bf3b7-145">Pour plus d’informations, consultez [canaux de couleurs](#color-channels) .</span><span class="sxs-lookup"><span data-stu-id="bf3b7-145">See [Color channels](#color-channels) for more info.</span></span><br/> |
| <span data-ttu-id="bf3b7-146">YChannelSelect</span><span class="sxs-lookup"><span data-stu-id="bf3b7-146">YChannelSelect</span></span><br/> <span data-ttu-id="bf3b7-147">D2D1 \_ DISPLACEMENTMAP \_ prop \_ Y \_ canal \_ Select</span><span class="sxs-lookup"><span data-stu-id="bf3b7-147">D2D1\_DISPLACEMENTMAP\_PROP\_Y\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="bf3b7-148">\_Sélecteur de canal d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="bf3b7-148">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="bf3b7-149">\_ \_ Sélecteur de canal d2d1 \_ A</span><span class="sxs-lookup"><span data-stu-id="bf3b7-149">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="bf3b7-150">L’effet extrait l’intensité de ce canal de couleur et l’utilise pour déplacer spatialement l’image dans la direction Y.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-150">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the Y direction.</span></span> <span data-ttu-id="bf3b7-151">Pour plus d’informations, consultez [canaux de couleurs](#color-channels) .</span><span class="sxs-lookup"><span data-stu-id="bf3b7-151">See [Color channels](#color-channels) for more info.</span></span><br/> |



 

## <a name="color-channels"></a><span data-ttu-id="bf3b7-152">Canaux de couleur</span><span class="sxs-lookup"><span data-stu-id="bf3b7-152">Color channels</span></span>



| <span data-ttu-id="bf3b7-153">Énumération</span><span class="sxs-lookup"><span data-stu-id="bf3b7-153">Enumeration</span></span>                | <span data-ttu-id="bf3b7-154">Description</span><span class="sxs-lookup"><span data-stu-id="bf3b7-154">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bf3b7-155">\_Sélecteur de canal d2d1 \_ \_ R</span><span class="sxs-lookup"><span data-stu-id="bf3b7-155">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="bf3b7-156">L’effet extrait la sortie d’intensité à partir du canal rouge.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-156">The effect extracts the intensity output from the red channel.</span></span>   |
| <span data-ttu-id="bf3b7-157">\_Sélecteur de canal d2d1 \_ \_ G</span><span class="sxs-lookup"><span data-stu-id="bf3b7-157">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="bf3b7-158">L’effet extrait la sortie d’intensité à partir du canal vert.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-158">The effect extracts the intensity output from the green channel.</span></span> |
| <span data-ttu-id="bf3b7-159">\_Sélecteur de canal d2d1 \_ \_ B</span><span class="sxs-lookup"><span data-stu-id="bf3b7-159">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="bf3b7-160">L’effet extrait la sortie d’intensité à partir du canal bleu.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-160">The effect extracts the intensity output from the blue channel.</span></span>  |
| <span data-ttu-id="bf3b7-161">\_ \_ Sélecteur de canal d2d1 \_ A</span><span class="sxs-lookup"><span data-stu-id="bf3b7-161">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="bf3b7-162">L’effet extrait la sortie d’intensité à partir du canal alpha.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-162">The effect extracts the intensity output from the alpha channel.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="bf3b7-163">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="bf3b7-163">Output Bitmap</span></span>

<span data-ttu-id="bf3b7-164">Vous pouvez déterminer la taille maximale de l’image bitmap de sortie avec les équations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf3b7-164">You can determine the maximum size of the output bitmap with these equations:</span></span>

<span data-ttu-id="bf3b7-165">Bitmap de sortie ?</span><span class="sxs-lookup"><span data-stu-id="bf3b7-165">Output Bitmap?</span></span> <span data-ttu-id="bf3b7-166">Pixels = (taille de l’image bitmap en entrée ? ( DIP) + échelle) \* (dpi utilisateur/96)</span><span class="sxs-lookup"><span data-stu-id="bf3b7-166">Pixels=(Input Bitmap Size?(DIPs)+Scale)\*(User DPI/96)</span></span>

<span data-ttu-id="bf3b7-167">Bitmap de sortie<sub>y</sub> pixels = (taille de la bitmap d’entrée<sub>y</sub>(DIP) + échelle) \* (dpi utilisateur/96)</span><span class="sxs-lookup"><span data-stu-id="bf3b7-167">Output Bitmap<sub>y</sub> Pixels=(Input Bitmap Size<sub>y</sub>(DIPs) + Scale)\*(User DPI/96)</span></span>

## <a name="requirements"></a><span data-ttu-id="bf3b7-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf3b7-168">Requirements</span></span>



| <span data-ttu-id="bf3b7-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf3b7-169">Requirement</span></span> | <span data-ttu-id="bf3b7-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf3b7-170">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf3b7-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf3b7-171">Minimum supported client</span></span> | <span data-ttu-id="bf3b7-172">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="bf3b7-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bf3b7-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf3b7-173">Minimum supported server</span></span> | <span data-ttu-id="bf3b7-174">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="bf3b7-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bf3b7-175">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf3b7-175">Header</span></span>                   | <span data-ttu-id="bf3b7-176">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="bf3b7-176">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="bf3b7-177">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bf3b7-177">Library</span></span>                  | <span data-ttu-id="bf3b7-178">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="bf3b7-178">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="bf3b7-179">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf3b7-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf3b7-180">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="bf3b7-180">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

