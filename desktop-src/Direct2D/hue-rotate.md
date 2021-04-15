---
title: Effet de rotation de la teinte
description: Utilisez l’effet rotation de la teinte pour modifier la teinte d’une image en appliquant une matrice de couleurs en fonction de l’angle de rotation.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- effet de rotation de la teinte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104554878"
---
# <a name="hue-rotatation-effect"></a><span data-ttu-id="f0332-104">Effet de rotation de la teinte</span><span class="sxs-lookup"><span data-stu-id="f0332-104">Hue rotatation effect</span></span>

<span data-ttu-id="f0332-105">Utilisez l’effet rotation de la teinte pour modifier la teinte d’une image en appliquant une matrice de couleurs en fonction de l’angle de rotation.</span><span class="sxs-lookup"><span data-stu-id="f0332-105">Use the hue rotate effect to alter the hue of an image by applying a color matrix based on the rotation angle.</span></span>

<span data-ttu-id="f0332-106">Le CLSID de cet effet est CLSID \_ D2D1HueRotation.</span><span class="sxs-lookup"><span data-stu-id="f0332-106">The CLSID for this effect is CLSID\_D2D1HueRotation.</span></span>

-   [<span data-ttu-id="f0332-107">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="f0332-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="f0332-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="f0332-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="f0332-109">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="f0332-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="f0332-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0332-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f0332-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0332-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="f0332-112">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="f0332-112">Example image</span></span>

<span data-ttu-id="f0332-113">L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet de rotation de la teinte avec un angle de rotation de 270 degrés.</span><span class="sxs-lookup"><span data-stu-id="f0332-113">The example here shows the input and output images of the hue rotate effect with a rotation angle of 270 degrees.</span></span>



| <span data-ttu-id="f0332-114">Avant</span><span class="sxs-lookup"><span data-stu-id="f0332-114">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)   |
| <span data-ttu-id="f0332-116">After</span><span class="sxs-lookup"><span data-stu-id="f0332-116">After</span></span>                                                        |
| ![image après la transformation.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="f0332-118">L’effet calcule une matrice de couleurs en fonction de l’angle de rotation (*?*) que vous spécifiez avec la \_ propriété d2d1 HUEROTATION \_ prop \_ angle.</span><span class="sxs-lookup"><span data-stu-id="f0332-118">The effect calculates a color matrix based on the rotation angle (*?*) you specify with the D2D1\_HUEROTATION\_PROP\_ANGLE property.</span></span> <span data-ttu-id="f0332-119">Voici les équations de matrice.</span><span class="sxs-lookup"><span data-stu-id="f0332-119">Here are the matrix equations.</span></span>

![calculs de rotation de teinte](images/hue-formula.png)

<span data-ttu-id="f0332-121">La matrice créée dépend uniquement de l’angle de rotation.</span><span class="sxs-lookup"><span data-stu-id="f0332-121">The matrix created depends only on the rotation angle.</span></span> <span data-ttu-id="f0332-122">Vous pouvez utiliser l’effet [matrice de couleurs](color-matrix.md) si vous avez besoin d’une matrice spécifique.</span><span class="sxs-lookup"><span data-stu-id="f0332-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="f0332-123">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="f0332-123">Effect properties</span></span>



| <span data-ttu-id="f0332-124">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="f0332-124">Display name and index enumeration</span></span>                         | <span data-ttu-id="f0332-125">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f0332-125">Type and default value</span></span>           | <span data-ttu-id="f0332-126">Description</span><span class="sxs-lookup"><span data-stu-id="f0332-126">Description</span></span>                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| <span data-ttu-id="f0332-127">Angle</span><span class="sxs-lookup"><span data-stu-id="f0332-127">Angle</span></span><br/> <span data-ttu-id="f0332-128">\_Angle d2d1 HUEROTATION \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="f0332-128">D2D1\_HUEROTATION\_PROP\_ANGLE</span></span><br/> | <span data-ttu-id="f0332-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f0332-129">FLOAT</span></span><br/> <span data-ttu-id="f0332-130">0.0f</span><span class="sxs-lookup"><span data-stu-id="f0332-130">0.0f</span></span><br/> | <span data-ttu-id="f0332-131">Angle de rotation de la teinte, en degrés.</span><span class="sxs-lookup"><span data-stu-id="f0332-131">The angle to rotate the hue, in degrees.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="f0332-132">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="f0332-132">Output bitmap</span></span>

<span data-ttu-id="f0332-133">La taille de la bitmap de sortie est la même que la taille de la bitmap d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f0332-133">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0332-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0332-134">Requirements</span></span>



| <span data-ttu-id="f0332-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0332-135">Requirement</span></span> | <span data-ttu-id="f0332-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0332-136">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0332-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0332-137">Minimum supported client</span></span> | <span data-ttu-id="f0332-138">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="f0332-138">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f0332-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0332-139">Minimum supported server</span></span> | <span data-ttu-id="f0332-140">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="f0332-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f0332-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0332-141">Header</span></span>                   | <span data-ttu-id="f0332-142">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="f0332-142">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="f0332-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0332-143">Library</span></span>                  | <span data-ttu-id="f0332-144">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="f0332-144">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="f0332-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0332-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0332-146">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="f0332-146">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

