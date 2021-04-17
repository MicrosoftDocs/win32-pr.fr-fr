---
title: Effets des tons clairs et des ombres
description: Ajuste les clairs et les ombres de l’image.
ms.assetid: ebbb7d99-9144-ffff-af73-d89e7d269924
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d595a5b82a2df0b0b0bab14c03e6a807511ed61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104559429"
---
# <a name="highlights-and-shadows-effect"></a><span data-ttu-id="590ef-103">Effets des tons clairs et des ombres</span><span class="sxs-lookup"><span data-stu-id="590ef-103">Highlights and shadows effect</span></span>

<span data-ttu-id="590ef-104">Ajuste les clairs et les ombres de l’image.</span><span class="sxs-lookup"><span data-stu-id="590ef-104">Adjusts the highlights and shadows of the image.</span></span>

<span data-ttu-id="590ef-105">Le CLSID de cet effet est CLSID \_ D2D1HighlightsShadows.</span><span class="sxs-lookup"><span data-stu-id="590ef-105">The CLSID for this effect is CLSID\_D2D1HighlightsShadows.</span></span>

-   [<span data-ttu-id="590ef-106">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="590ef-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="590ef-107">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="590ef-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="590ef-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="590ef-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="590ef-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="590ef-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="590ef-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="590ef-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="590ef-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="590ef-111">Example image</span></span>

![exemple de sortie d’effet](images/highlights-and-shadows-effect.png)

## <a name="sample-code"></a><span data-ttu-id="590ef-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="590ef-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> highlightsAndShadowsEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HighlightsShadows, &highlightsAndShadowsEffect);
 
highlightsAndShadowsEffect->SetInput(0, bitmap);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, 0.0f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, 0.5f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, 0.2f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="590ef-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="590ef-114">Effect properties</span></span>

<span data-ttu-id="590ef-115">Les propriétés de l’effet des tons clairs et des tons foncés sont définies par l’énumération [**d2d1 \_ HIGHLIGHTSANDSHADOWS \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) .</span><span class="sxs-lookup"><span data-stu-id="590ef-115">The properties for the highlights and shadows effect are defined by the [**D2D1\_HIGHLIGHTSANDSHADOWS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="590ef-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="590ef-116">Requirements</span></span>

| <span data-ttu-id="590ef-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="590ef-117">Requirement</span></span> | <span data-ttu-id="590ef-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="590ef-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="590ef-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="590ef-119">Minimum supported client</span></span> | <span data-ttu-id="590ef-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="590ef-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="590ef-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="590ef-121">Minimum supported server</span></span> | <span data-ttu-id="590ef-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="590ef-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="590ef-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="590ef-123">Header</span></span>                   | <span data-ttu-id="590ef-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="590ef-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="590ef-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="590ef-125">Library</span></span>                  | <span data-ttu-id="590ef-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="590ef-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="590ef-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="590ef-127">Related topics</span></span>

* [<span data-ttu-id="590ef-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="590ef-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
