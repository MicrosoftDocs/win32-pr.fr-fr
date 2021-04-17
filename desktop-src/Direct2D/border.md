---
title: Effet de bordure
description: Utilisez l’effet de bordure pour étendre une image à partir des bords.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- effet de bordure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104530412"
---
# <a name="border-effect"></a><span data-ttu-id="35fec-104">Effet de bordure</span><span class="sxs-lookup"><span data-stu-id="35fec-104">Border effect</span></span>

<span data-ttu-id="35fec-105">Utilisez l’effet de bordure pour étendre une image à partir des bords.</span><span class="sxs-lookup"><span data-stu-id="35fec-105">Use the border effect to extend an image from the edges.</span></span> <span data-ttu-id="35fec-106">Vous pouvez utiliser cet effet pour répéter les pixels à partir des bords de l’image, habiller les pixels de l’extrémité opposée de l’image ou mettre en miroir les pixels sur la bordure de l’image bitmap pour étendre la région de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="35fec-106">You can use this effect to repeat the pixels from the edges of the image, wrap the pixels from the opposite end of the image, or mirror the pixels across the bitmap border to extend the bitmap region.</span></span>

<span data-ttu-id="35fec-107">Le CLSID de cet effet est CLSID \_ D2D1Border.</span><span class="sxs-lookup"><span data-stu-id="35fec-107">The CLSID for this effect is CLSID\_D2D1Border.</span></span>

## <a name="example-images"></a><span data-ttu-id="35fec-108">Exemples d’images</span><span class="sxs-lookup"><span data-stu-id="35fec-108">Example images</span></span>

<span data-ttu-id="35fec-109">Les exemples ci-dessous illustrent la sortie de l’effet de bordure à l’aide de chaque mode.</span><span class="sxs-lookup"><span data-stu-id="35fec-109">The examples here show the output of the border effect using each mode.</span></span> <span data-ttu-id="35fec-110">La taille de sortie est infinie, mais ces exemples d’images sont rognés à deux fois la taille.</span><span class="sxs-lookup"><span data-stu-id="35fec-110">The output size is infinite, but these example images are cropped to twice the size.</span></span>

### <a name="mirror"></a><span data-ttu-id="35fec-111">Miroir</span><span class="sxs-lookup"><span data-stu-id="35fec-111">Mirror</span></span>



| <span data-ttu-id="35fec-112">Avant</span><span class="sxs-lookup"><span data-stu-id="35fec-112">Before</span></span>                                                    |
|-----------------------------------------------------------|
| ![Capture d’écran qui affiche l’image avant l’effet.](images/border-before.jpg) |
| <span data-ttu-id="35fec-114">After</span><span class="sxs-lookup"><span data-stu-id="35fec-114">After</span></span>                                                     |
| ![Capture d’écran qui montre l’image après la transformation.](images/10-border.png)   |



 

### <a name="clamp"></a><span data-ttu-id="35fec-116">Clamp</span><span class="sxs-lookup"><span data-stu-id="35fec-116">Clamp</span></span>



| <span data-ttu-id="35fec-117">Avant</span><span class="sxs-lookup"><span data-stu-id="35fec-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![Capture d’écran qui montre l’image avant l’effet d’une bride.](images/border-before.jpg)     |
| <span data-ttu-id="35fec-119">After</span><span class="sxs-lookup"><span data-stu-id="35fec-119">After</span></span>                                                         |
| ![Capture d’écran qui montre l’image après la transformation d’une bride.](images/10-border-clamp.png) |



 

### <a name="wrap"></a><span data-ttu-id="35fec-121">Encapsuler</span><span class="sxs-lookup"><span data-stu-id="35fec-121">Wrap</span></span>



| <span data-ttu-id="35fec-122">Avant</span><span class="sxs-lookup"><span data-stu-id="35fec-122">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![Capture d’écran qui montre l’image avant l’effet d’un retour à la ligne.](images/border-before.jpg)    |
| <span data-ttu-id="35fec-124">After</span><span class="sxs-lookup"><span data-stu-id="35fec-124">After</span></span>                                                        |
| ![Capture d’écran qui montre l’image après la transformation d’un retour à la ligne.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="35fec-126">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="35fec-126">Effect properties</span></span>



| <span data-ttu-id="35fec-127">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="35fec-127">Display name and index enumeration</span></span>                                  | <span data-ttu-id="35fec-128">Description</span><span class="sxs-lookup"><span data-stu-id="35fec-128">Description</span></span>                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fec-129">Mode bord X</span><span class="sxs-lookup"><span data-stu-id="35fec-129">Edge Mode X</span></span><br/> <span data-ttu-id="35fec-130">D2D1 \_ bordure \_ prop \_ \_ en mode Edge \_ X</span><span class="sxs-lookup"><span data-stu-id="35fec-130">D2D1\_BORDER\_PROP\_EDGE\_MODE\_X</span></span><br/> | <span data-ttu-id="35fec-131">Mode de bord dans la direction X de l’effet.</span><span class="sxs-lookup"><span data-stu-id="35fec-131">The edge mode in the X direction for the effect.</span></span> <span data-ttu-id="35fec-132">Vous pouvez définir cette valeur sur clamp, Wrap ou Mirror.</span><span class="sxs-lookup"><span data-stu-id="35fec-132">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="35fec-133">Pour plus d’informations, consultez [modes de bord](#edge-modes) .</span><span class="sxs-lookup"><span data-stu-id="35fec-133">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="35fec-134">Le type est D2D1 \_ \_ Edge bord \_ mode.</span><span class="sxs-lookup"><span data-stu-id="35fec-134">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="35fec-135">La valeur par défaut est \_ d2d1 \_ en mode bord de bordure \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="35fec-135">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |
| <span data-ttu-id="35fec-136">Mode bord Y</span><span class="sxs-lookup"><span data-stu-id="35fec-136">Edge Mode Y</span></span><br/> <span data-ttu-id="35fec-137">D2D1 \_ frontière \_ prop \_ \_ en mode Edge \_ Y</span><span class="sxs-lookup"><span data-stu-id="35fec-137">D2D1\_BORDER\_PROP\_EDGE\_MODE\_Y</span></span><br/> | <span data-ttu-id="35fec-138">Mode de bord dans l’axe Y de l’effet.</span><span class="sxs-lookup"><span data-stu-id="35fec-138">The edge mode in the Y direction for the effect.</span></span> <span data-ttu-id="35fec-139">Vous pouvez définir cette valeur sur clamp, Wrap ou Mirror.</span><span class="sxs-lookup"><span data-stu-id="35fec-139">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="35fec-140">Pour plus d’informations, consultez [modes de bord](#edge-modes) .</span><span class="sxs-lookup"><span data-stu-id="35fec-140">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="35fec-141">Le type est D2D1 \_ \_ Edge bord \_ mode.</span><span class="sxs-lookup"><span data-stu-id="35fec-141">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="35fec-142">La valeur par défaut est \_ d2d1 \_ en mode bord de bordure \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="35fec-142">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |



 

## <a name="edge-modes"></a><span data-ttu-id="35fec-143">Modes de bord</span><span class="sxs-lookup"><span data-stu-id="35fec-143">Edge modes</span></span>



| <span data-ttu-id="35fec-144">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="35fec-144">Display name and index enumeration</span></span>                            | <span data-ttu-id="35fec-145">Description</span><span class="sxs-lookup"><span data-stu-id="35fec-145">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35fec-146">Clamp</span><span class="sxs-lookup"><span data-stu-id="35fec-146">Clamp</span></span><br/> <span data-ttu-id="35fec-147">D2D1 de \_ mode de bordure de \_ bord \_ \_</span><span class="sxs-lookup"><span data-stu-id="35fec-147">D2D1\_BORDER\_EDGE\_MODE\_CLAMP</span></span><br/>   | <span data-ttu-id="35fec-148">Répète les pixels à partir des bords de l’image.</span><span class="sxs-lookup"><span data-stu-id="35fec-148">Repeats the pixels from the edges of the image.</span></span>      |
| <span data-ttu-id="35fec-149">Encapsuler</span><span class="sxs-lookup"><span data-stu-id="35fec-149">Wrap</span></span><br/> <span data-ttu-id="35fec-150">D2D1 le \_ mode de bordure de \_ bord \_ \_</span><span class="sxs-lookup"><span data-stu-id="35fec-150">D2D1\_BORDER\_EDGE\_MODE\_WRAP</span></span><br/>     | <span data-ttu-id="35fec-151">Utilise des pixels du bord de fin opposé de l’image.</span><span class="sxs-lookup"><span data-stu-id="35fec-151">Uses pixels from the opposite end edge of the image.</span></span> |
| <span data-ttu-id="35fec-152">Miroir</span><span class="sxs-lookup"><span data-stu-id="35fec-152">Mirror</span></span><br/> <span data-ttu-id="35fec-153">D2D1 \_ en \_ mode Edge frontière \_ \_</span><span class="sxs-lookup"><span data-stu-id="35fec-153">D2D1\_BORDER\_EDGE\_MODE\_MIRROR</span></span><br/> | <span data-ttu-id="35fec-154">Reflète les pixels sur le bord de l’image.</span><span class="sxs-lookup"><span data-stu-id="35fec-154">Reflects pixels about the edge of the image.</span></span>         |



 

## <a name="output-bitmap"></a><span data-ttu-id="35fec-155">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="35fec-155">Output bitmap</span></span>

<span data-ttu-id="35fec-156">La taille de la bitmap de sortie est infinie pour toutes les entrées, à l’exception d’une image d’entrée de 0 taille.</span><span class="sxs-lookup"><span data-stu-id="35fec-156">The output bitmap size is infinite for all inputs, except a 0 sized input image.</span></span> <span data-ttu-id="35fec-157">Si la hauteur ou la largeur d’une image d’entrée est égale à 0, la taille de sortie est 0.</span><span class="sxs-lookup"><span data-stu-id="35fec-157">If the height or the width of an input image is 0, the output size is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fec-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35fec-158">Requirements</span></span>



| <span data-ttu-id="35fec-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35fec-159">Requirement</span></span> | <span data-ttu-id="35fec-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="35fec-160">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35fec-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35fec-161">Minimum supported client</span></span> | <span data-ttu-id="35fec-162">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="35fec-162">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="35fec-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35fec-163">Minimum supported server</span></span> | <span data-ttu-id="35fec-164">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="35fec-164">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="35fec-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="35fec-165">Header</span></span>                   | <span data-ttu-id="35fec-166">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="35fec-166">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="35fec-167">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35fec-167">Library</span></span>                  | <span data-ttu-id="35fec-168">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="35fec-168">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="35fec-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35fec-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35fec-170">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="35fec-170">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

