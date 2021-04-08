---
title: Effet de rognage
description: Utilisez l’effet rognage pour sortir une région spécifiée d’une image.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- effet de rognage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843533"
---
# <a name="crop-effect"></a><span data-ttu-id="439a6-104">Effet de rognage</span><span class="sxs-lookup"><span data-stu-id="439a6-104">Crop effect</span></span>

<span data-ttu-id="439a6-105">Utilisez l’effet rognage pour sortir une région spécifiée d’une image.</span><span class="sxs-lookup"><span data-stu-id="439a6-105">Use the crop effect to output a specified region of an image.</span></span>

<span data-ttu-id="439a6-106">Le CLSID de cet effet est CLSID \_ D2D1Crop.</span><span class="sxs-lookup"><span data-stu-id="439a6-106">The CLSID for this effect is CLSID\_D2D1Crop.</span></span>

-   [<span data-ttu-id="439a6-107">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="439a6-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="439a6-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="439a6-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="439a6-109">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="439a6-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="439a6-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="439a6-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="439a6-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="439a6-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="439a6-112">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="439a6-112">Example image</span></span>



| <span data-ttu-id="439a6-113">Avant</span><span class="sxs-lookup"><span data-stu-id="439a6-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| <span data-ttu-id="439a6-115">After</span><span class="sxs-lookup"><span data-stu-id="439a6-115">After</span></span>                                                      |
| ![image après la transformation.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="439a6-117">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="439a6-117">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="439a6-118">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="439a6-118">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="439a6-119">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="439a6-119">Type and default value</span></span></th>
<th><span data-ttu-id="439a6-120">Description</span><span class="sxs-lookup"><span data-stu-id="439a6-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="439a6-121">Rect</span><span class="sxs-lookup"><span data-stu-id="439a6-121">Rect</span></span><br/></td>
<td><span data-ttu-id="439a6-122">D2D1_VECTOR_4F</span><span class="sxs-lookup"><span data-stu-id="439a6-122">D2D1_VECTOR_4F</span></span><br/></td>
<td><span data-ttu-id="439a6-123">Région à rogner spécifiée comme vecteur au format (gauche, haut, largeur, hauteur).</span><span class="sxs-lookup"><span data-stu-id="439a6-123">The region to be cropped specified as a vector in the form (left, top, width, height).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="439a6-124">D2D1_CROP_PROP_RECT</span><span class="sxs-lookup"><span data-stu-id="439a6-124">D2D1_CROP_PROP_RECT</span></span><br/></td>
<td><span data-ttu-id="439a6-125">{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}</span><span class="sxs-lookup"><span data-stu-id="439a6-125">{-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}</span></span><br/></td>
<td><span data-ttu-id="439a6-126">Les unités sont en DIP.</span><span class="sxs-lookup"><span data-stu-id="439a6-126">The units are in DIPs.</span></span> <br/>
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="439a6-127">Le Rect sera tronqué s’il chevauche les limites de bord de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="439a6-127">The Rect will be truncated if it overlaps the edge boundaries of the input image.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="439a6-128">D2D1_CROP_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="439a6-128">D2D1_CROP_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="439a6-129">D2D1_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="439a6-129">D2D1_BORDER_MODE</span></span> <br/> <span data-ttu-id="439a6-130">D2D1_BORDER_MODE_SOFT</span><span class="sxs-lookup"><span data-stu-id="439a6-130">D2D1_BORDER_MODE_SOFT</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="439a6-131">D2D1_BORDER_MODE_SOFT : si le rectangle de rognage tombe sur des coordonnées de pixels fractionnaires, l’effet applique l’anticrénelage qui produit une bordure douce.</span><span class="sxs-lookup"><span data-stu-id="439a6-131">D2D1_BORDER_MODE_SOFT : If the crop rectangle falls on fractional pixel coordinates, the effect applies antialiasing which results in a soft edge.</span></span></li>
<li><span data-ttu-id="439a6-132">D2D1_BORDER_MODE_HARD : si le rectangle de rognage se trouve sur des coordonnées de pixels fractionnaires, il s’agit d’un effet de serre qui produit un bord dur.</span><span class="sxs-lookup"><span data-stu-id="439a6-132">D2D1_BORDER_MODE_HARD : If the crop rectangle falls on fractional pixel coordinates, the effect clamps which results in a hard edge.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a><span data-ttu-id="439a6-133">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="439a6-133">Output bitmap</span></span>

<span data-ttu-id="439a6-134">La sortie de cet effet est la taille de la propriété Rect.</span><span class="sxs-lookup"><span data-stu-id="439a6-134">The output of this effect is the size of the Rect property.</span></span> <span data-ttu-id="439a6-135">La longueur et la largeur sont calculées</span><span class="sxs-lookup"><span data-stu-id="439a6-135">The length and width are calc</span></span>

<span data-ttu-id="439a6-136">ulated à l’aide des équations ici :</span><span class="sxs-lookup"><span data-stu-id="439a6-136">ulated using the equations here:</span></span> <dl> <span data-ttu-id="439a6-137">Longueur de sortie en pixels = (Rect. Right-Rect. Left) \* (dpi/96 de l’utilisateur)</span><span class="sxs-lookup"><span data-stu-id="439a6-137">Output length in Pixels=(Rect.Right-Rect.Left)\*(User's DPI/96)</span></span>  
<span data-ttu-id="439a6-138">Hauteur de sortie en pixels = (Rect. Bottom-Rect.Top) \* (dpi/96 de l’utilisateur)</span><span class="sxs-lookup"><span data-stu-id="439a6-138">Output height in pixels=(Rect.Bottom-Rect.Top)\*(User's DPI/96)</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="439a6-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="439a6-139">Requirements</span></span>



| <span data-ttu-id="439a6-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="439a6-140">Requirement</span></span> | <span data-ttu-id="439a6-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="439a6-141">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="439a6-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="439a6-142">Minimum supported client</span></span> | <span data-ttu-id="439a6-143">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="439a6-143">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="439a6-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="439a6-144">Minimum supported server</span></span> | <span data-ttu-id="439a6-145">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="439a6-145">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="439a6-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="439a6-146">Header</span></span>                   | <span data-ttu-id="439a6-147">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="439a6-147">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="439a6-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="439a6-148">Library</span></span>                  | <span data-ttu-id="439a6-149">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="439a6-149">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="439a6-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="439a6-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439a6-151">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="439a6-151">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

