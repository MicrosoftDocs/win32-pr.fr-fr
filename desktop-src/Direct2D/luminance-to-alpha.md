---
title: Effet luminance vers alpha
description: Utilisez l’effet luminance pour Alpha pour définir le canal alpha sur la luminance de l’image et définir les canaux de couleur sur 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- effet luminance vers alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104553248"
---
# <a name="luminance-to-alpha-effect"></a><span data-ttu-id="7c417-104">Effet luminance vers alpha</span><span class="sxs-lookup"><span data-stu-id="7c417-104">Luminance to alpha effect</span></span>

<span data-ttu-id="7c417-105">Utilisez l’effet luminance pour Alpha pour définir le canal alpha sur la luminance de l’image et définir les canaux de couleur sur 0.</span><span class="sxs-lookup"><span data-stu-id="7c417-105">Use the luminance to alpha effect to set the alpha channel to the luminance of the image and sets the color channels to 0.</span></span> <span data-ttu-id="7c417-106">Vous pouvez utiliser la sortie de cet effet pour créer une superposition translucide en fonction de la luminosité de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7c417-106">You can use the output of this effect to make a semitransparent overlay based on the brightness of the input image.</span></span> <span data-ttu-id="7c417-107">Ou vous pouvez l’utiliser pour créer un masque d’image.</span><span class="sxs-lookup"><span data-stu-id="7c417-107">Or you can use it to make an image mask.</span></span>

> [!Note]  
> <span data-ttu-id="7c417-108">Cet effet n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7c417-108">This effect has no properties.</span></span>

 

<span data-ttu-id="7c417-109">Le CLSID de cet effet est CLSID \_ D2D1LuminanceToAlpha.</span><span class="sxs-lookup"><span data-stu-id="7c417-109">The CLSID for this effect is CLSID\_D2D1LuminanceToAlpha.</span></span>

## <a name="example-image"></a><span data-ttu-id="7c417-110">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="7c417-110">Example image</span></span>

<span data-ttu-id="7c417-111">Cet exemple montre la sortie de l’effet luminance vers alpha composite sur une surface blanche pour afficher l’opacité.</span><span class="sxs-lookup"><span data-stu-id="7c417-111">This example shows the output of the luminance to alpha effect composited over a white surface to show opacity.</span></span>



| <span data-ttu-id="7c417-112">Avant</span><span class="sxs-lookup"><span data-stu-id="7c417-112">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)        |
| <span data-ttu-id="7c417-114">After</span><span class="sxs-lookup"><span data-stu-id="7c417-114">After</span></span>                                                             |
| ![image après la transformation.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="7c417-116">Cet effet définit le canal alpha de la sortie sur la luminance de l’image d’entrée à l’aide de cette matrice de couleurs.</span><span class="sxs-lookup"><span data-stu-id="7c417-116">This effect sets the alpha channel of the output to the luminance of the input image using this color matrix.</span></span>

![matrice de couleurs utilisée par l’effet pour définir le canal alpha.](images/luminance-to-alpha-math1.png)

<span data-ttu-id="7c417-118">Cet effet consomme et génère des images alpha prémultipliées.</span><span class="sxs-lookup"><span data-stu-id="7c417-118">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="7c417-119">L’effet ne fonctionne pas sur les images alpha directes, sauf si elles sont entièrement opaques.</span><span class="sxs-lookup"><span data-stu-id="7c417-119">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

> [!Note]
>
> <span data-ttu-id="7c417-120">Étant donné que les images sont stockées dans un format compensé gamma, avant de calculer la luminance pour une image, vous devez d’abord effectuer une correction gamma inverse pour obtenir les valeurs de couleur vraies pour l’image.</span><span class="sxs-lookup"><span data-stu-id="7c417-120">Because images are stored in a gamma-compensated format, before you calculate the luminance for an image you should first perform inverse gamma correction to get the true color values for the image.</span></span> <span data-ttu-id="7c417-121">Étant donné que les images sont normalement stockées à 2,2 de gamma, vous pouvez utiliser l’effet de transfert gamma avec un exposant de (1/2.2), puis utiliser la sortie de cet effet.</span><span class="sxs-lookup"><span data-stu-id="7c417-121">Since images are normally stored at 2.2 gamma, you can use the Gamma transfer effect with an exponent of (1/2.2) and then use the output of that effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7c417-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c417-122">Requirements</span></span>



| <span data-ttu-id="7c417-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c417-123">Requirement</span></span> | <span data-ttu-id="7c417-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c417-124">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c417-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c417-125">Minimum supported client</span></span> | <span data-ttu-id="7c417-126">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="7c417-126">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7c417-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c417-127">Minimum supported server</span></span> | <span data-ttu-id="7c417-128">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="7c417-128">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7c417-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c417-129">Header</span></span>                   | <span data-ttu-id="7c417-130">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="7c417-130">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="7c417-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c417-131">Library</span></span>                  | <span data-ttu-id="7c417-132">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7c417-132">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="output-bitmap"></a><span data-ttu-id="7c417-133">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="7c417-133">Output bitmap</span></span>

<span data-ttu-id="7c417-134">La sortie a la même taille que l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7c417-134">The output is the same size as the input image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c417-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c417-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c417-136">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="7c417-136">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
