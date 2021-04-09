---
title: Effet vignette
description: Atténue l’image d’entrée des bords en couleur définie par l’utilisateur.
ms.assetid: 34da221f-44a2-1d01-d88d-d7846b9770b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fe9302a86a49b060aa05ecb856ce43122d946d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104935"
---
# <a name="vignette-effect"></a><span data-ttu-id="12d4e-103">Effet vignette</span><span class="sxs-lookup"><span data-stu-id="12d4e-103">Vignette effect</span></span>

<span data-ttu-id="12d4e-104">Atténue l’image d’entrée des bords en couleur définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12d4e-104">Fades the input image at the edges to a user-set color.</span></span>

<span data-ttu-id="12d4e-105">Le CLSID de cet effet est CLSID \_ D2D1Vignette.</span><span class="sxs-lookup"><span data-stu-id="12d4e-105">The CLSID for this effect is CLSID\_D2D1Vignette.</span></span>

-   [<span data-ttu-id="12d4e-106">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="12d4e-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="12d4e-107">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="12d4e-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="12d4e-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="12d4e-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="12d4e-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12d4e-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="12d4e-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12d4e-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="12d4e-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="12d4e-111">Example image</span></span>

![exemple de sortie d’effet](images/vignette-effect.png)

## <a name="sample-code"></a><span data-ttu-id="12d4e-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="12d4e-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> vignetteEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Vignette, &vignetteEffect);
 
vignetteEffect->SetInput(0, bitmap);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_COLOR, );
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_TRANSITION_SIZE, 0.1f);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_STRENGTH, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(vignetteEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="12d4e-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="12d4e-114">Effect properties</span></span>

<span data-ttu-id="12d4e-115">Les propriétés de l’effet vignette sont définies par l’énumération [**d2d1 \_ vignette \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) .</span><span class="sxs-lookup"><span data-stu-id="12d4e-115">The properties for the vignette effect are defined by the [**D2D1\_VIGNETTE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d4e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12d4e-116">Requirements</span></span>

| <span data-ttu-id="12d4e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12d4e-117">Requirement</span></span> | <span data-ttu-id="12d4e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="12d4e-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="12d4e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12d4e-119">Minimum supported client</span></span> | <span data-ttu-id="12d4e-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="12d4e-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="12d4e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12d4e-121">Minimum supported server</span></span> | <span data-ttu-id="12d4e-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="12d4e-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="12d4e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="12d4e-123">Header</span></span>                   | <span data-ttu-id="12d4e-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="12d4e-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="12d4e-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12d4e-125">Library</span></span>                  | <span data-ttu-id="12d4e-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="12d4e-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="12d4e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12d4e-127">Related topics</span></span>

* [<span data-ttu-id="12d4e-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="12d4e-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
