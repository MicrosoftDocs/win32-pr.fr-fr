---
title: Effet d’exposition
description: Augmentez ou diminuez l’exposition de l’image.
ms.assetid: d384f539-5c19-53c7-e52b-bf833e221449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6f5bda52fecc0b5e3896515b04a6560f17da49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942513"
---
# <a name="exposure-effect"></a><span data-ttu-id="4f9b2-103">Effet d’exposition</span><span class="sxs-lookup"><span data-stu-id="4f9b2-103">Exposure effect</span></span>

<span data-ttu-id="4f9b2-104">Augmentez ou diminuez l’exposition de l’image.</span><span class="sxs-lookup"><span data-stu-id="4f9b2-104">Increase or decreases the exposure of the image.</span></span>

<span data-ttu-id="4f9b2-105">Le CLSID de cet effet est CLSID \_ D2D1Exposure.</span><span class="sxs-lookup"><span data-stu-id="4f9b2-105">The CLSID for this effect is CLSID\_D2D1Exposure.</span></span>

-   [<span data-ttu-id="4f9b2-106">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="4f9b2-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="4f9b2-107">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="4f9b2-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="4f9b2-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="4f9b2-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="4f9b2-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f9b2-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4f9b2-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f9b2-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="4f9b2-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="4f9b2-111">Example image</span></span>

![exemple de sortie d’effet](images/exposure-effect.png)

## <a name="sample-code"></a><span data-ttu-id="4f9b2-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="4f9b2-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> exposureEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Exposure, &exposureEffect);
 
exposureEffect->SetInput(0, bitmap);
exposureEffect->SetValue(D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(exposureEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="4f9b2-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="4f9b2-114">Effect properties</span></span>

<span data-ttu-id="4f9b2-115">Les propriétés de l’effet d’exposition sont définies par l’énumération [**d2d1 \_ Exposure \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) .</span><span class="sxs-lookup"><span data-stu-id="4f9b2-115">The properties for the exposure effect are defined by the [**D2D1\_EXPOSURE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f9b2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f9b2-116">Requirements</span></span>



| <span data-ttu-id="4f9b2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f9b2-117">Requirement</span></span> | <span data-ttu-id="4f9b2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f9b2-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="4f9b2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f9b2-119">Minimum supported client</span></span> | <span data-ttu-id="4f9b2-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="4f9b2-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4f9b2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f9b2-121">Minimum supported server</span></span> | <span data-ttu-id="4f9b2-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="4f9b2-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4f9b2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f9b2-123">Header</span></span>                   | <span data-ttu-id="4f9b2-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="4f9b2-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="4f9b2-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f9b2-125">Library</span></span>                  | <span data-ttu-id="4f9b2-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="4f9b2-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="4f9b2-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f9b2-127">Related topics</span></span>

* [<span data-ttu-id="4f9b2-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="4f9b2-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




