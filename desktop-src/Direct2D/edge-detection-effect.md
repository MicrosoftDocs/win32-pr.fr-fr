---
title: Effet de détection de périphérie
description: Filtre le contenu d’une image, en laissant des lignes à la périphérie des sections contrastées de l’image.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47239bede77dc5d32582c6e83c8101e5c9bbf2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033261"
---
# <a name="edge-detection-effect"></a><span data-ttu-id="302d0-103">Effet de détection de périphérie</span><span class="sxs-lookup"><span data-stu-id="302d0-103">Edge-detection effect</span></span>

<span data-ttu-id="302d0-104">Filtre le contenu d’une image, en laissant des lignes à la périphérie des sections contrastées de l’image.</span><span class="sxs-lookup"><span data-stu-id="302d0-104">Filters out the content of an image, leaving lines at the edges of contrasting sections of the image.</span></span>

<span data-ttu-id="302d0-105">Le CLSID de cet effet est CLSID \_ D2D1EdgeDetection.</span><span class="sxs-lookup"><span data-stu-id="302d0-105">The CLSID for this effect is CLSID\_D2D1EdgeDetection.</span></span>

-   [<span data-ttu-id="302d0-106">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="302d0-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="302d0-107">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="302d0-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="302d0-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="302d0-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="302d0-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="302d0-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="302d0-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="302d0-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="302d0-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="302d0-111">Example image</span></span>

![exemple de sortie d’effet](images/edge-detection-effect.png)

## <a name="sample-code"></a><span data-ttu-id="302d0-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="302d0-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="302d0-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="302d0-114">Effect properties</span></span>

<span data-ttu-id="302d0-115">Les propriétés de l’effet de détection Edge sont définies par l’énumération [**d2d1 \_ EDGEDETECTION \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) .</span><span class="sxs-lookup"><span data-stu-id="302d0-115">The properties for the edge detection effect are defined by the [**D2D1\_EDGEDETECTION\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="302d0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="302d0-116">Requirements</span></span>



| <span data-ttu-id="302d0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="302d0-117">Requirement</span></span> | <span data-ttu-id="302d0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="302d0-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="302d0-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="302d0-119">Minimum supported client</span></span> | <span data-ttu-id="302d0-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="302d0-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="302d0-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="302d0-121">Minimum supported server</span></span> | <span data-ttu-id="302d0-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="302d0-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="302d0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="302d0-123">Header</span></span>                   | <span data-ttu-id="302d0-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="302d0-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="302d0-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="302d0-125">Library</span></span>                  | <span data-ttu-id="302d0-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="302d0-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="302d0-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="302d0-127">Related topics</span></span>

* [<span data-ttu-id="302d0-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="302d0-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
