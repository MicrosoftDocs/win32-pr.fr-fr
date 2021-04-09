---
title: Effet morphologique
description: Utilisez l’effet morphologique pour les limites d’arête fine ou Epaissir dans une image.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- effets morphologiques
- effet d’Universion
- effet d’érosion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104728"
---
# <a name="morphology-effect"></a><span data-ttu-id="7a9ff-106">Effet morphologique</span><span class="sxs-lookup"><span data-stu-id="7a9ff-106">Morphology effect</span></span>

<span data-ttu-id="7a9ff-107">Utilisez l’effet morphologique pour les limites d’arête fine ou Epaissir dans une image.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-107">Use the morphology effect to thin or thicken edge boundaries in an image.</span></span> <span data-ttu-id="7a9ff-108">Cet effet crée un noyau qui est de 2 fois la largeur et la hauteur que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-108">This effect creates a kernel that is 2 times the Width and Height values you specify.</span></span> <span data-ttu-id="7a9ff-109">Cet effet centre le noyau sur le pixel qu’il calcule et retourne la valeur maximale dans le noyau (en cas de dilatation) ou la valeur minimale dans le noyau (en cas d’érosion).</span><span class="sxs-lookup"><span data-stu-id="7a9ff-109">This effect centers the kernel on the pixel it is calculating and returns the maximum value in the kernel (if dilating) or minimum value in the kernel (if eroding).</span></span>

<span data-ttu-id="7a9ff-110">Le CLSID de cet effet est CLSID \_ D2D1Morphology.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-110">The CLSID for this effect is CLSID\_D2D1Morphology.</span></span>

## <a name="example-images"></a><span data-ttu-id="7a9ff-111">Exemples d’images</span><span class="sxs-lookup"><span data-stu-id="7a9ff-111">Example images</span></span>

<span data-ttu-id="7a9ff-112">Cet exemple montre la sortie de l’effet lors de l’utilisation du mode ÉROD.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-112">This example shows the output of the effect when using the erode mode.</span></span>



| <span data-ttu-id="7a9ff-113">Avant</span><span class="sxs-lookup"><span data-stu-id="7a9ff-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| <span data-ttu-id="7a9ff-115">After</span><span class="sxs-lookup"><span data-stu-id="7a9ff-115">After</span></span>                                                      |
| ![image après la transformation.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="7a9ff-117">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="7a9ff-117">Effect properties</span></span>



| <span data-ttu-id="7a9ff-118">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="7a9ff-118">Display name and index enumeration</span></span>                          | <span data-ttu-id="7a9ff-119">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="7a9ff-119">Type and default value</span></span>                                                     | <span data-ttu-id="7a9ff-120">Description</span><span class="sxs-lookup"><span data-stu-id="7a9ff-120">Description</span></span>                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a9ff-121">Mode</span><span class="sxs-lookup"><span data-stu-id="7a9ff-121">Mode</span></span><br/> <span data-ttu-id="7a9ff-122">\_Mode d2d1 morphologique \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="7a9ff-122">D2D1\_MORPHOLOGY\_PROP\_MODE</span></span><br/>     | <span data-ttu-id="7a9ff-123">\_Mode morphologique \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="7a9ff-123">D2D1\_MORPHOLOGY\_MODE</span></span><br/> <span data-ttu-id="7a9ff-124">\_Mode morphologique \_ d2d1 \_ ÉROD</span><span class="sxs-lookup"><span data-stu-id="7a9ff-124">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span><br/> | <span data-ttu-id="7a9ff-125">Mode morphologique.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-125">The morphology mode.</span></span> <span data-ttu-id="7a9ff-126">Les modes disponibles sont ÉROD (aplatir) et dilate (Epaissir).</span><span class="sxs-lookup"><span data-stu-id="7a9ff-126">The available modes are erode (flatten) and dilate (thicken).</span></span><br/> <span data-ttu-id="7a9ff-127">Pour plus d’informations, consultez [modes morphologique](#morphology-modes) .</span><span class="sxs-lookup"><span data-stu-id="7a9ff-127">See [Morphology modes](#morphology-modes) for more info.</span></span><br/> |
| <span data-ttu-id="7a9ff-128">Largeur</span><span class="sxs-lookup"><span data-stu-id="7a9ff-128">Width</span></span><br/> <span data-ttu-id="7a9ff-129">Largeur de la D2D1 de la \_ morphologie \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a9ff-129">D2D1\_MORPHOLOGY\_PROP\_WIDTH</span></span><br/>   | <span data-ttu-id="7a9ff-130">UINT</span><span class="sxs-lookup"><span data-stu-id="7a9ff-130">UINT</span></span><br/> <span data-ttu-id="7a9ff-131">1</span><span class="sxs-lookup"><span data-stu-id="7a9ff-131">1</span></span><br/>                                               | <span data-ttu-id="7a9ff-132">Taille du noyau sur l’axe X.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-132">Size of the kernel in the X direction.</span></span> <span data-ttu-id="7a9ff-133">Les unités sont en DIP.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-133">The units are in DIPs.</span></span> <span data-ttu-id="7a9ff-134">Les valeurs doivent être comprises entre 1 et 100 inclus.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-134">Values must be between 1 and 100 inclusive.</span></span>                                                         |
| <span data-ttu-id="7a9ff-135">Hauteur</span><span class="sxs-lookup"><span data-stu-id="7a9ff-135">Height</span></span><br/> <span data-ttu-id="7a9ff-136">Hauteur de la D2D1 de la \_ morphologie \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a9ff-136">D2D1\_MORPHOLOGY\_PROP\_HEIGHT</span></span><br/> | <span data-ttu-id="7a9ff-137">UINT</span><span class="sxs-lookup"><span data-stu-id="7a9ff-137">UINT</span></span><br/> <span data-ttu-id="7a9ff-138">1</span><span class="sxs-lookup"><span data-stu-id="7a9ff-138">1</span></span><br/>                                               | <span data-ttu-id="7a9ff-139">Taille du noyau sur l’axe Y.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-139">Size of the kernel in the Y direction.</span></span> <span data-ttu-id="7a9ff-140">Les unités sont en DIP.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-140">The units are in DIPs.</span></span> <span data-ttu-id="7a9ff-141">Les valeurs doivent être comprises entre 1 et 100 inclus.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-141">Values must be between 1 and 100 inclusive.</span></span>                                                         |



 

## <a name="morphology-modes"></a><span data-ttu-id="7a9ff-142">Modes morphologiques</span><span class="sxs-lookup"><span data-stu-id="7a9ff-142">Morphology modes</span></span>



| <span data-ttu-id="7a9ff-143">Nom</span><span class="sxs-lookup"><span data-stu-id="7a9ff-143">Name</span></span>                           | <span data-ttu-id="7a9ff-144">Description</span><span class="sxs-lookup"><span data-stu-id="7a9ff-144">Description</span></span>                                                    |
|--------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7a9ff-145">\_Mode morphologique \_ d2d1 \_ ÉROD</span><span class="sxs-lookup"><span data-stu-id="7a9ff-145">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span>  | <span data-ttu-id="7a9ff-146">La valeur maximale de chaque canal RVB dans le noyau est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-146">The maximum value from each RGB channel in the kernel is used.</span></span> |
| <span data-ttu-id="7a9ff-147">\_Mode morphologique d2d1 \_ en \_ retard</span><span class="sxs-lookup"><span data-stu-id="7a9ff-147">D2D1\_MORPHOLOGY\_MODE\_DILATE</span></span> | <span data-ttu-id="7a9ff-148">La valeur minimale de chaque canal RVB dans le noyau est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7a9ff-148">The minimum value from each RGB channel in the kernel is used.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="7a9ff-149">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="7a9ff-149">Output bitmap</span></span>

<span data-ttu-id="7a9ff-150">Pour le mode de sortie, la taille de la bitmap de sortie augmente :</span><span class="sxs-lookup"><span data-stu-id="7a9ff-150">For DILATE mode, the Output Bitmap size grows:</span></span> 

| <span data-ttu-id="7a9ff-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a9ff-151">Requirement</span></span> | <span data-ttu-id="7a9ff-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a9ff-152">Value</span></span> |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="7a9ff-153">Croissance des bitmaps de sortie X =</span><span class="sxs-lookup"><span data-stu-id="7a9ff-153">Output Bitmap Growth X =</span></span> | <span data-ttu-id="7a9ff-154">INT (FLOAT (Width) \* ((dpi utilisateur)/96))</span><span class="sxs-lookup"><span data-stu-id="7a9ff-154">INT(FLOAT(Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="7a9ff-155">Croissance de la bitmap de sortie Y =</span><span class="sxs-lookup"><span data-stu-id="7a9ff-155">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="7a9ff-156">INT (FLOAT (hauteur) \* ((dpi utilisateur)/96))</span><span class="sxs-lookup"><span data-stu-id="7a9ff-156">INT(FLOAT(Height) \* ((User DPI) / 96))</span></span> |



 

<span data-ttu-id="7a9ff-157">Pour le mode ÉROD, la taille de la bitmap de sortie diminue :</span><span class="sxs-lookup"><span data-stu-id="7a9ff-157">For ERODE mode, the Output Bitmap size shrinks:</span></span>

| <span data-ttu-id="7a9ff-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a9ff-158">Requirement</span></span> | <span data-ttu-id="7a9ff-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a9ff-159">Value</span></span> |
|--------------------------|------------------------------------------|
| <span data-ttu-id="7a9ff-160">Croissance des bitmaps de sortie X =</span><span class="sxs-lookup"><span data-stu-id="7a9ff-160">Output Bitmap Growth X =</span></span> | <span data-ttu-id="7a9ff-161">INT (FLOAT (-Width) \* ((dpi utilisateur)/96))</span><span class="sxs-lookup"><span data-stu-id="7a9ff-161">INT(FLOAT(-Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="7a9ff-162">Croissance de la bitmap de sortie Y =</span><span class="sxs-lookup"><span data-stu-id="7a9ff-162">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="7a9ff-163">INT (FLOAT (-Height) \* ((dpi utilisateur)/96))</span><span class="sxs-lookup"><span data-stu-id="7a9ff-163">INT(FLOAT(-Height) \* ((User DPI) / 96))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7a9ff-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a9ff-164">Requirements</span></span>



| <span data-ttu-id="7a9ff-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a9ff-165">Requirement</span></span> | <span data-ttu-id="7a9ff-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a9ff-166">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a9ff-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a9ff-167">Minimum supported client</span></span> | <span data-ttu-id="7a9ff-168">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="7a9ff-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7a9ff-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a9ff-169">Minimum supported server</span></span> | <span data-ttu-id="7a9ff-170">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="7a9ff-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7a9ff-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a9ff-171">Header</span></span>                   | <span data-ttu-id="7a9ff-172">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="7a9ff-172">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="7a9ff-173">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a9ff-173">Library</span></span>                  | <span data-ttu-id="7a9ff-174">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7a9ff-174">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="7a9ff-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a9ff-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a9ff-176">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="7a9ff-176">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

