---
title: Effet de la netteté
description: Rend l’image plus nette.
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54203cfeb786204500c905e2ff4cfc83bf9719e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741180"
---
# <a name="sharpen-effect"></a><span data-ttu-id="c0b6f-103">Effet de la netteté</span><span class="sxs-lookup"><span data-stu-id="c0b6f-103">Sharpen effect</span></span>

<span data-ttu-id="c0b6f-104">Rend l’image plus nette.</span><span class="sxs-lookup"><span data-stu-id="c0b6f-104">Sharpens the image.</span></span>

<span data-ttu-id="c0b6f-105">Le CLSID de cet effet est CLSID \_ D2D1Sharpen.</span><span class="sxs-lookup"><span data-stu-id="c0b6f-105">The CLSID for this effect is CLSID\_D2D1Sharpen.</span></span>

-   [<span data-ttu-id="c0b6f-106">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="c0b6f-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="c0b6f-107">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c0b6f-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="c0b6f-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="c0b6f-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c0b6f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0b6f-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c0b6f-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0b6f-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c0b6f-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="c0b6f-111">Example image</span></span>

![exemple de sortie d’effet](images/sharpen-effect.png)

## <a name="sample-code"></a><span data-ttu-id="c0b6f-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="c0b6f-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="c0b6f-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="c0b6f-114">Effect properties</span></span>

<span data-ttu-id="c0b6f-115">Les propriétés de l’effet de la netteté sont définies par l’énumération de la [**\_ \_ netteté d2d1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) .</span><span class="sxs-lookup"><span data-stu-id="c0b6f-115">The properties for the sharpen effect are defined by the [**D2D1\_SHARPEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b6f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0b6f-116">Requirements</span></span>



| <span data-ttu-id="c0b6f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0b6f-117">Requirement</span></span> | <span data-ttu-id="c0b6f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0b6f-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="c0b6f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0b6f-119">Minimum supported client</span></span> | <span data-ttu-id="c0b6f-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c0b6f-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c0b6f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0b6f-121">Minimum supported server</span></span> | <span data-ttu-id="c0b6f-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c0b6f-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c0b6f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0b6f-123">Header</span></span>                   | <span data-ttu-id="c0b6f-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="c0b6f-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="c0b6f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0b6f-125">Library</span></span>                  | <span data-ttu-id="c0b6f-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c0b6f-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="c0b6f-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0b6f-127">Related topics</span></span>

* [<span data-ttu-id="c0b6f-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="c0b6f-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



