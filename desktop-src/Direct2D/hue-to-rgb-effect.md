---
title: Effet teinte-à-RGB
description: Convertit une image TSL (teinte, saturation, luminosité) ou HSV (teinte, saturation, valeur) en un espace de couleurs RVB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942058"
---
# <a name="hue-to-rgb-effect"></a><span data-ttu-id="774a1-103">Effet teinte-à-RGB</span><span class="sxs-lookup"><span data-stu-id="774a1-103">Hue-to-RGB effect</span></span>

<span data-ttu-id="774a1-104">Convertit une image TSL (teinte, saturation, luminosité) ou HSV (teinte, saturation, valeur) en un espace de couleurs RVB.</span><span class="sxs-lookup"><span data-stu-id="774a1-104">Converts an HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) image to the RGB color space.</span></span>

<span data-ttu-id="774a1-105">TSL et HSV sont deux modèles différents pour représenter une couleur RVB dans un espace colorimétrique cylindrique.</span><span class="sxs-lookup"><span data-stu-id="774a1-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="774a1-106">Ils sont utiles car ils vous permettent d’obtenir des informations sur une couleur à l’aide de concepts plus intuitifs, tels que la teinte et l’intensité, et la combinaison de valeurs rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="774a1-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="774a1-107">Cet effet passe par toutes les valeurs alpha d’entrée.</span><span class="sxs-lookup"><span data-stu-id="774a1-107">This effect passes through any input alpha values.</span></span>

<span data-ttu-id="774a1-108">Le CLSID de cet effet est CLSID \_ D2D1HueToRgb.</span><span class="sxs-lookup"><span data-stu-id="774a1-108">The CLSID for this effect is CLSID\_D2D1HueToRgb.</span></span>

<span data-ttu-id="774a1-109">Pour inverser le comportement de cet effet, utilisez l' [effet RVB pour teinte](rgb-to-hue-effect.md).</span><span class="sxs-lookup"><span data-stu-id="774a1-109">To reverse the behavior of this effect, use the [RGB to Hue effect](rgb-to-hue-effect.md).</span></span>

-   [<span data-ttu-id="774a1-110">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="774a1-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="774a1-111">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="774a1-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="774a1-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="774a1-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="774a1-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="774a1-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="774a1-114">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="774a1-114">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="774a1-115">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="774a1-115">Effect properties</span></span>

<span data-ttu-id="774a1-116">Les propriétés de l’effet de contraste sont définies par l’énumération [**d2d1 \_ HUETORGB \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) .</span><span class="sxs-lookup"><span data-stu-id="774a1-116">The properties for the contrast effect are defined by the [**D2D1\_HUETORGB\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="774a1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="774a1-117">Requirements</span></span>



| <span data-ttu-id="774a1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="774a1-118">Requirement</span></span> | <span data-ttu-id="774a1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="774a1-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="774a1-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="774a1-120">Minimum supported client</span></span> | <span data-ttu-id="774a1-121">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="774a1-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="774a1-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="774a1-122">Minimum supported server</span></span> | <span data-ttu-id="774a1-123">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="774a1-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="774a1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="774a1-124">Header</span></span>                   | <span data-ttu-id="774a1-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="774a1-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="774a1-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="774a1-126">Library</span></span>                  | <span data-ttu-id="774a1-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="774a1-127">d2d1.lib, dxguid.lib</span></span>                              |



## <a name="related-topics"></a><span data-ttu-id="774a1-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="774a1-128">Related topics</span></span>

* [<span data-ttu-id="774a1-129">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="774a1-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
