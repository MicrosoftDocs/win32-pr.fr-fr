---
title: Effet de relief
description: Crée une version en nuances de gris de l’image qui apparaît comme si elle était marquée sur papier.
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dde087eb7f85fcd68615c39730bf6208024fc43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741533"
---
# <a name="emboss-effect"></a><span data-ttu-id="b5ef2-103">Effet de relief</span><span class="sxs-lookup"><span data-stu-id="b5ef2-103">Emboss effect</span></span>

<span data-ttu-id="b5ef2-104">Crée une version en nuances de gris de l’image qui apparaît comme si elle était marquée sur papier.</span><span class="sxs-lookup"><span data-stu-id="b5ef2-104">Creates a grayscale version of the image that appears as though it has been stamped into paper.</span></span>

<span data-ttu-id="b5ef2-105">Le CLSID de cet effet est CLSID \_ D2D1Emboss.</span><span class="sxs-lookup"><span data-stu-id="b5ef2-105">The CLSID for this effect is CLSID\_D2D1Emboss.</span></span>

-   [<span data-ttu-id="b5ef2-106">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="b5ef2-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="b5ef2-107">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="b5ef2-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="b5ef2-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="b5ef2-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b5ef2-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5ef2-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b5ef2-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5ef2-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="b5ef2-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="b5ef2-111">Example image</span></span>

![exemple de sortie d’effet](images/emboss-effect.png)

## <a name="sample-code"></a><span data-ttu-id="b5ef2-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="b5ef2-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="b5ef2-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="b5ef2-114">Effect properties</span></span>

<span data-ttu-id="b5ef2-115">Les propriétés de l’effet de relief sont définies par l’énumération [**d2d1 \_ emboss \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) .</span><span class="sxs-lookup"><span data-stu-id="b5ef2-115">The properties for the emboss effect are defined by the [**D2D1\_EMBOSS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ef2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5ef2-116">Requirements</span></span>



| <span data-ttu-id="b5ef2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5ef2-117">Requirement</span></span> | <span data-ttu-id="b5ef2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5ef2-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="b5ef2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ef2-119">Minimum supported client</span></span> | <span data-ttu-id="b5ef2-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b5ef2-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b5ef2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ef2-121">Minimum supported server</span></span> | <span data-ttu-id="b5ef2-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b5ef2-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b5ef2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5ef2-123">Header</span></span>                   | <span data-ttu-id="b5ef2-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="b5ef2-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="b5ef2-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5ef2-125">Library</span></span>                  | <span data-ttu-id="b5ef2-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b5ef2-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="b5ef2-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5ef2-127">Related topics</span></span>

* [<span data-ttu-id="b5ef2-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="b5ef2-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
