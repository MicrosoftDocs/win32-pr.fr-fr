---
title: Effet de flux
description: Utilisez l’effet de flux pour générer une image bitmap basée sur la couleur spécifiée et la valeur alpha. Vous pouvez utiliser cet effet lorsque vous souhaitez qu’une couleur spécifique soit une entrée pour un effet, comme une couleur d’arrière-plan.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- effet de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942511"
---
# <a name="flood-effect"></a><span data-ttu-id="c2a5c-105">Effet de flux</span><span class="sxs-lookup"><span data-stu-id="c2a5c-105">Flood effect</span></span>

<span data-ttu-id="c2a5c-106">Utilisez l’effet de flux pour générer une image bitmap basée sur la couleur spécifiée et la valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-106">Use the flood effect to generate a bitmap based on the specified color and alpha value.</span></span> <span data-ttu-id="c2a5c-107">Vous pouvez utiliser cet effet lorsque vous souhaitez qu’une couleur spécifique soit une entrée pour un effet, comme une couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-107">You can use this effect when you want a specific color as an input for an effect, like a background color.</span></span>

> [!Note]  
> <span data-ttu-id="c2a5c-108">L’effet passe le long de la valeur de couleur spécifiée comme spécifié.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-108">The effect passes along the specified color value as specified.</span></span> <span data-ttu-id="c2a5c-109">Vous devez prémultiplier manuellement les valeurs si vous envisagez de passer la sortie aux effets qui attendent une entrée prémultipliée.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-109">You must manually pre-multiply the values if you plan to pass the output to effects that expect a pre-multiplied input.</span></span>

 

<span data-ttu-id="c2a5c-110">Le CLSID de cet effet est CLSID \_ D2D1Flood.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-110">The CLSID for this effect is CLSID\_D2D1Flood.</span></span>

<span data-ttu-id="c2a5c-111">L’effet de flux n’a aucune image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-111">The flood effect has no input image.</span></span>

-   [<span data-ttu-id="c2a5c-112">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="c2a5c-112">Example image</span></span>](#example-image)
-   [<span data-ttu-id="c2a5c-113">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="c2a5c-113">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c2a5c-114">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="c2a5c-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="c2a5c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2a5c-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c2a5c-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2a5c-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c2a5c-117">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="c2a5c-117">Example image</span></span>

![exemple d’image de l’effet de saturation en vert.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="c2a5c-119">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="c2a5c-119">Effect properties</span></span>



| <span data-ttu-id="c2a5c-120">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="c2a5c-120">Display name and index enumeration</span></span>                   | <span data-ttu-id="c2a5c-121">Description</span><span class="sxs-lookup"><span data-stu-id="c2a5c-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a5c-122">Couleur</span><span class="sxs-lookup"><span data-stu-id="c2a5c-122">Color</span></span><br/> <span data-ttu-id="c2a5c-123">Couleur de la \_ prop d2d1 Flood \_ \_</span><span class="sxs-lookup"><span data-stu-id="c2a5c-123">D2D1\_FLOOD\_PROP\_COLOR</span></span><br/> | <span data-ttu-id="c2a5c-124">Couleur et opacité de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-124">The color and opacity of the bitmap.</span></span> <span data-ttu-id="c2a5c-125">Cette propriété est un \_ vecteur d2d1 \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-125">This property is a D2D1\_VECTOR\_4F.</span></span> <span data-ttu-id="c2a5c-126">Les valeurs individuelles de chaque canal sont de type flottant, illimité et sans unité.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-126">The individual values for each channel are of type FLOAT, unbounded and unitless.</span></span> <span data-ttu-id="c2a5c-127">L’effet ne modifie pas les valeurs des canaux.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-127">The effect doesn't modify the values for the channels.</span></span><br/> <span data-ttu-id="c2a5c-128">Les valeurs RVBA pour chaque canal sont comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-128">The RGBA values for each channel range from 0 to 1.</span></span><br/> <span data-ttu-id="c2a5c-129">Le type est D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-129">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="c2a5c-130">La valeur par défaut est {0.0 f, 0.0 f, 0.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-130">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="c2a5c-131">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="c2a5c-131">Output bitmap</span></span>

<span data-ttu-id="c2a5c-132">Cet effet génère une image bitmap de taille infinie logiquement.</span><span class="sxs-lookup"><span data-stu-id="c2a5c-132">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a5c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2a5c-133">Requirements</span></span>



| <span data-ttu-id="c2a5c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2a5c-134">Requirement</span></span> | <span data-ttu-id="c2a5c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2a5c-135">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a5c-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2a5c-136">Minimum supported client</span></span> | <span data-ttu-id="c2a5c-137">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c2a5c-137">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c2a5c-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2a5c-138">Minimum supported server</span></span> | <span data-ttu-id="c2a5c-139">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c2a5c-139">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c2a5c-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2a5c-140">Header</span></span>                   | <span data-ttu-id="c2a5c-141">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="c2a5c-141">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c2a5c-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2a5c-142">Library</span></span>                  | <span data-ttu-id="c2a5c-143">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c2a5c-143">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c2a5c-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2a5c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2a5c-145">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c2a5c-145">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

