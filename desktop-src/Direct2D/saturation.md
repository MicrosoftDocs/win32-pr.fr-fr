---
title: Effet de saturation
description: Utilisez cet effet pour modifier la saturation d’une image.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- effet de saturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032734"
---
# <a name="saturation-effect"></a><span data-ttu-id="60027-104">Effet de saturation</span><span class="sxs-lookup"><span data-stu-id="60027-104">Saturation effect</span></span>

<span data-ttu-id="60027-105">Utilisez cet effet pour modifier la saturation d’une image.</span><span class="sxs-lookup"><span data-stu-id="60027-105">Use this effect to alter the saturation of an image.</span></span> <span data-ttu-id="60027-106">L’effet de saturation est une spécialisation de l’effet de [matrice de couleurs](color-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="60027-106">The saturation effect is a specialization of the [color matrix](color-matrix.md) effect.</span></span>

<span data-ttu-id="60027-107">Le CLSID de cet effet est CLSID \_ D2D1Saturation.</span><span class="sxs-lookup"><span data-stu-id="60027-107">The CLSID for this effect is CLSID\_D2D1Saturation.</span></span>

-   [<span data-ttu-id="60027-108">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="60027-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="60027-109">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="60027-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="60027-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60027-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="60027-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60027-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="60027-112">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="60027-112">Example image</span></span>

<span data-ttu-id="60027-113">L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet de saturation avec une saturation de 0%.</span><span class="sxs-lookup"><span data-stu-id="60027-113">The example here shows the input and output images of the saturation effect with a saturation of 0%.</span></span>



| <span data-ttu-id="60027-114">Avant</span><span class="sxs-lookup"><span data-stu-id="60027-114">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)  |
| <span data-ttu-id="60027-116">After</span><span class="sxs-lookup"><span data-stu-id="60027-116">After</span></span>                                                       |
| ![image après la transformation.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="60027-118">L’effet calcule une *matrice de couleurs* en fonction de la valeur de saturation (dans l’équation ici) que vous spécifiez avec la propriété saturation d2d1 \_ saturation \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="60027-118">The effect calculates a color matrix based on the saturation value (*s* in the equation here) you specify with the D2D1\_SATURATION\_PROP\_SATURATION property.</span></span> <span data-ttu-id="60027-119">L’équation de matrice est présentée ici.</span><span class="sxs-lookup"><span data-stu-id="60027-119">The matrix equation is shown here.</span></span>

![formule permettant de calculer une matrice de saturation.](images/saturation-formula.png)

<span data-ttu-id="60027-121">La matrice créée dépend uniquement de la valeur de saturation.</span><span class="sxs-lookup"><span data-stu-id="60027-121">The matrix created depends only on the saturation value.</span></span> <span data-ttu-id="60027-122">Vous pouvez utiliser l’effet [matrice de couleurs](color-matrix.md) si vous avez besoin d’une matrice spécifique.</span><span class="sxs-lookup"><span data-stu-id="60027-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

<span data-ttu-id="60027-123">Cet effet consomme et génère des images alpha prémultipliées.</span><span class="sxs-lookup"><span data-stu-id="60027-123">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="60027-124">L’effet ne fonctionne pas sur les images alpha directes, sauf si elles sont entièrement opaques.</span><span class="sxs-lookup"><span data-stu-id="60027-124">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="60027-125">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="60027-125">Effect properties</span></span>



| <span data-ttu-id="60027-126">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="60027-126">Display name and index enumeration</span></span>                                  | <span data-ttu-id="60027-127">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="60027-127">Type and default value</span></span>           | <span data-ttu-id="60027-128">Description</span><span class="sxs-lookup"><span data-stu-id="60027-128">Description</span></span>                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60027-129">Saturation</span><span class="sxs-lookup"><span data-stu-id="60027-129">Saturation</span></span><br/> <span data-ttu-id="60027-130">Saturation de la \_ saturation d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="60027-130">D2D1\_SATURATION\_PROP\_SATURATION</span></span><br/> | <span data-ttu-id="60027-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="60027-131">FLOAT</span></span><br/> <span data-ttu-id="60027-132">0,5 f</span><span class="sxs-lookup"><span data-stu-id="60027-132">0.5f</span></span><br/> | <span data-ttu-id="60027-133">Saturation de l’image.</span><span class="sxs-lookup"><span data-stu-id="60027-133">The saturation of the image.</span></span> <span data-ttu-id="60027-134">Vous pouvez définir la saturation sur une valeur comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="60027-134">You can set the saturation to a value between 0 and 1.</span></span> <span data-ttu-id="60027-135">Si vous lui affectez la valeur 1, l’image de sortie est entièrement saturée.</span><span class="sxs-lookup"><span data-stu-id="60027-135">If you set it to 1 the output image is fully saturated.</span></span> <span data-ttu-id="60027-136">Si vous lui affectez la valeur 0, l’image de sortie est monochrome.</span><span class="sxs-lookup"><span data-stu-id="60027-136">If you set it to 0 the output image is monochrome.</span></span> <span data-ttu-id="60027-137">La valeur de saturation est sans unité.</span><span class="sxs-lookup"><span data-stu-id="60027-137">The saturation value is unitless.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="60027-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60027-138">Requirements</span></span>



| <span data-ttu-id="60027-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60027-139">Requirement</span></span> | <span data-ttu-id="60027-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="60027-140">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60027-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60027-141">Minimum supported client</span></span> | <span data-ttu-id="60027-142">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="60027-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="60027-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60027-143">Minimum supported server</span></span> | <span data-ttu-id="60027-144">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="60027-144">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="60027-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="60027-145">Header</span></span>                   | <span data-ttu-id="60027-146">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="60027-146">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="60027-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60027-147">Library</span></span>                  | <span data-ttu-id="60027-148">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="60027-148">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="60027-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60027-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60027-150">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="60027-150">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

