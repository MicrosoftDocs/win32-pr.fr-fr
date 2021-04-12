---
title: Effet de vignette
description: Utilisez l’effet de vignette pour répéter la région spécifiée de l’image.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- effet de vignette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032940"
---
# <a name="tile-effect"></a><span data-ttu-id="da812-104">Effet de vignette</span><span class="sxs-lookup"><span data-stu-id="da812-104">Tile effect</span></span>

<span data-ttu-id="da812-105">Utilisez l’effet de vignette pour répéter la région spécifiée de l’image.</span><span class="sxs-lookup"><span data-stu-id="da812-105">Use the tile effect to repeat the specified region of the image.</span></span>

<span data-ttu-id="da812-106">Le CLSID de cet effet est CLSID \_ D2D1Tile.</span><span class="sxs-lookup"><span data-stu-id="da812-106">The CLSID for this effect is CLSID\_D2D1Tile.</span></span>

## <a name="example-image"></a><span data-ttu-id="da812-107">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="da812-107">Example image</span></span>



| <span data-ttu-id="da812-108">Avant</span><span class="sxs-lookup"><span data-stu-id="da812-108">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| <span data-ttu-id="da812-110">After</span><span class="sxs-lookup"><span data-stu-id="da812-110">After</span></span>                                                      |
| ![image après la transformation.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="da812-112">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="da812-112">Effect properties</span></span>



| <span data-ttu-id="da812-113">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="da812-113">Display name and index enumeration</span></span>                | <span data-ttu-id="da812-114">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="da812-114">Type and default value</span></span>                                              | <span data-ttu-id="da812-115">Description</span><span class="sxs-lookup"><span data-stu-id="da812-115">Description</span></span>                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da812-116">Rect</span><span class="sxs-lookup"><span data-stu-id="da812-116">Rect</span></span><br/> <span data-ttu-id="da812-117">D2D1 de \_ vignette \_ prop \_ Rect</span><span class="sxs-lookup"><span data-stu-id="da812-117">D2D1\_TILE\_PROP\_RECT</span></span><br/> | <span data-ttu-id="da812-118">D2D1 \_ vecteur \_ 4F</span><span class="sxs-lookup"><span data-stu-id="da812-118">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="da812-119">{0.0 f, 0.0 f, 100,0 f, 100,0 f}</span><span class="sxs-lookup"><span data-stu-id="da812-119">{0.0f, 0.0f, 100.0f, 100.0f}</span></span><br/> | <span data-ttu-id="da812-120">Zone de l’image à présenter en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="da812-120">The region of the image to be tiled.</span></span> <span data-ttu-id="da812-121">Cette propriété est un \_ vecteur d2d1 \_ 4F défini comme suit : (gauche, haut, droite, bas).</span><span class="sxs-lookup"><span data-stu-id="da812-121">This property is a D2D1\_VECTOR\_4F defined as: (left, top, right, bottom).</span></span> <span data-ttu-id="da812-122">Les unités sont en DIP.</span><span class="sxs-lookup"><span data-stu-id="da812-122">The units are in DIPs.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="da812-123">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="da812-123">Output bitmap</span></span>

<span data-ttu-id="da812-124">Cet effet génère une image bitmap de taille infinie logiquement.</span><span class="sxs-lookup"><span data-stu-id="da812-124">This effect generates a logically infinite sized bitmap.</span></span>

<span data-ttu-id="da812-125">Vous pouvez juxtaposer une image et générer une certaine taille sans effets supplémentaires en définissant la taille quand vous appelez [**ID2D1DeviceContext ::D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span><span class="sxs-lookup"><span data-stu-id="da812-125">You can tile an image and output a certain size without any additional effects by setting the size when you call [**ID2D1DeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span></span>

## <a name="requirements"></a><span data-ttu-id="da812-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da812-126">Requirements</span></span>



| <span data-ttu-id="da812-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da812-127">Requirement</span></span> | <span data-ttu-id="da812-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="da812-128">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da812-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da812-129">Minimum supported client</span></span> | <span data-ttu-id="da812-130">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="da812-130">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="da812-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da812-131">Minimum supported server</span></span> | <span data-ttu-id="da812-132">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="da812-132">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="da812-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="da812-133">Header</span></span>                   | <span data-ttu-id="da812-134">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="da812-134">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="da812-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da812-135">Library</span></span>                  | <span data-ttu-id="da812-136">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="da812-136">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="da812-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da812-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da812-138">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="da812-138">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

