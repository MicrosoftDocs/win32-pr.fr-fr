---
title: Effet de redresser
description: Pivote et ajuste éventuellement une image.
ms.assetid: aa37cdf1-bbb6-db4e-45a7-67c7cc16b7b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8e521ca4c0c452301c0f8031c94ba8c22efe80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104551086"
---
# <a name="straighten-effect"></a><span data-ttu-id="e2f1b-103">Effet de redresser</span><span class="sxs-lookup"><span data-stu-id="e2f1b-103">Straighten effect</span></span>

<span data-ttu-id="e2f1b-104">Pivote et ajuste éventuellement une image.</span><span class="sxs-lookup"><span data-stu-id="e2f1b-104">Rotates and optionally scales an image.</span></span>

<span data-ttu-id="e2f1b-105">Le CLSID de cet effet est CLSID \_ D2D1Straighten.</span><span class="sxs-lookup"><span data-stu-id="e2f1b-105">The CLSID for this effect is CLSID\_D2D1Straighten.</span></span>

-   [<span data-ttu-id="e2f1b-106">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="e2f1b-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="e2f1b-107">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e2f1b-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="e2f1b-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="e2f1b-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e2f1b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2f1b-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e2f1b-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2f1b-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="e2f1b-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="e2f1b-111">Example image</span></span>

![exemple de sortie d’effet](images/straighten-effect.png)

## <a name="sample-code"></a><span data-ttu-id="e2f1b-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="e2f1b-113">Sample code</span></span>


```cpp
ComPtr<ID2D1Effect> straightenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Straighten, &straightenEffect);
 
straightenEffect->SetInput(0, bitmap);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_ANGLE, 12.0f);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, true);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_SCALE_MODE, D2D1_STRAIGHTEN_SCALE_MODE_LINEAR);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(straightenEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="e2f1b-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="e2f1b-114">Effect properties</span></span>

<span data-ttu-id="e2f1b-115">Les propriétés de l’effet redresser sont définies par l’énumération [**d2d1 \_ redresse \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) .</span><span class="sxs-lookup"><span data-stu-id="e2f1b-115">The properties for the straighten effect are defined by the [**D2D1\_STRAIGHTEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f1b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2f1b-116">Requirements</span></span>



| <span data-ttu-id="e2f1b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2f1b-117">Requirement</span></span> | <span data-ttu-id="e2f1b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2f1b-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="e2f1b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2f1b-119">Minimum supported client</span></span> | <span data-ttu-id="e2f1b-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e2f1b-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e2f1b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2f1b-121">Minimum supported server</span></span> | <span data-ttu-id="e2f1b-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e2f1b-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e2f1b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2f1b-123">Header</span></span>                   | <span data-ttu-id="e2f1b-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="e2f1b-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="e2f1b-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2f1b-125">Library</span></span>                  | <span data-ttu-id="e2f1b-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e2f1b-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="e2f1b-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2f1b-127">Related topics</span></span>

* [<span data-ttu-id="e2f1b-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="e2f1b-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

