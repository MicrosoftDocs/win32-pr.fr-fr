---
title: Effet RGB-à-teinte
description: Convertit une image RVB en espaces de couleurs TSL (teinte, saturation, luminosité) ou HSV (teinte, saturation, valeur).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384491"
---
# <a name="rgb-to-hue-effect"></a><span data-ttu-id="880ee-103">Effet RGB-à-teinte</span><span class="sxs-lookup"><span data-stu-id="880ee-103">RGB-to-hue effect</span></span>

<span data-ttu-id="880ee-104">Convertit une image RVB en espaces de couleurs TSL (teinte, saturation, luminosité) ou HSV (teinte, saturation, valeur).</span><span class="sxs-lookup"><span data-stu-id="880ee-104">Converts an RGB image to either the HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) color spaces.</span></span>

<span data-ttu-id="880ee-105">TSL et HSV sont deux modèles différents pour représenter une couleur RVB dans un espace colorimétrique cylindrique.</span><span class="sxs-lookup"><span data-stu-id="880ee-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="880ee-106">Ils sont utiles car ils vous permettent d’obtenir des informations sur une couleur à l’aide de concepts plus intuitifs, tels que la teinte et l’intensité, et la combinaison de valeurs rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="880ee-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="880ee-107">Cet effet normalise les données de sortie (valeur de teinte, de saturation pour HSV ou teinte, saturation, luminosité pour TSL) à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="880ee-107">This effect normalizes the output data (hue, saturation value for HSV or hue, saturation, lightness for HSL) to the range \[0, 1\].</span></span>

<span data-ttu-id="880ee-108">Le CLSID de cet effet est CLSID \_ D2D1RgbToHue.</span><span class="sxs-lookup"><span data-stu-id="880ee-108">The CLSID for this effect is CLSID\_D2D1RgbToHue.</span></span>

<span data-ttu-id="880ee-109">Pour inverser le comportement de cet effet, utilisez l' [effet teinter au RVB](hue-to-rgb-effect.md).</span><span class="sxs-lookup"><span data-stu-id="880ee-109">To reverse the behavior of this effect, use the [Hue to RGB effect](hue-to-rgb-effect.md).</span></span>

-   [<span data-ttu-id="880ee-110">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="880ee-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="880ee-111">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="880ee-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="880ee-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="880ee-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="880ee-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="880ee-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="880ee-114">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="880ee-114">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a><span data-ttu-id="880ee-115">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="880ee-115">Effect properties</span></span>

<span data-ttu-id="880ee-116">Les propriétés de l’effet de contraste sont définies par l’énumération [**d2d1 \_ RGBTOHUE \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) .</span><span class="sxs-lookup"><span data-stu-id="880ee-116">The properties for the contrast effect are defined by the [**D2D1\_RGBTOHUE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="880ee-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="880ee-117">Requirements</span></span>



| <span data-ttu-id="880ee-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="880ee-118">Requirement</span></span> | <span data-ttu-id="880ee-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="880ee-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="880ee-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="880ee-120">Minimum supported client</span></span> | <span data-ttu-id="880ee-121">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="880ee-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="880ee-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="880ee-122">Minimum supported server</span></span> | <span data-ttu-id="880ee-123">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="880ee-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="880ee-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="880ee-124">Header</span></span>                   | <span data-ttu-id="880ee-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="880ee-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="880ee-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="880ee-126">Library</span></span>                  | <span data-ttu-id="880ee-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="880ee-127">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="880ee-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="880ee-128">Related topics</span></span>

* [<span data-ttu-id="880ee-129">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="880ee-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
