---
title: Effet clé Chroma
description: Convertit une couleur donnée plus ou moins une tolérance en alpha. Par exemple, la touche chroma peut supprimer l’arrière-plan d’une image pour un effet de recouvrement en vert à l’écran.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843409"
---
# <a name="chroma-key-effect"></a><span data-ttu-id="eaaba-104">Effet clé Chroma</span><span class="sxs-lookup"><span data-stu-id="eaaba-104">Chroma-key effect</span></span>

<span data-ttu-id="eaaba-105">Convertit une couleur donnée plus ou moins une tolérance en alpha.</span><span class="sxs-lookup"><span data-stu-id="eaaba-105">Converts a given color plus or minus a tolerance to alpha.</span></span> <span data-ttu-id="eaaba-106">Par exemple, la touche chroma peut supprimer l’arrière-plan d’une image pour un effet de recouvrement en vert à l’écran.</span><span class="sxs-lookup"><span data-stu-id="eaaba-106">For example, chroma-key can remove the background of an image for a green-screen overlay effect.</span></span>

<span data-ttu-id="eaaba-107">Le CLSID de cet effet est CLSID \_ D2D1ChromaKey.</span><span class="sxs-lookup"><span data-stu-id="eaaba-107">The CLSID for this effect is CLSID\_D2D1ChromaKey.</span></span>

-   [<span data-ttu-id="eaaba-108">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="eaaba-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="eaaba-109">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="eaaba-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="eaaba-110">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="eaaba-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="eaaba-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaaba-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="eaaba-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eaaba-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="eaaba-113">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="eaaba-113">Example image</span></span>

![exemple de sortie d’effet](images/chromakey-effect.png)

> [!Note]  
> <span data-ttu-id="eaaba-115">Dans cet exemple, la sortie de l’effet de clé Chroma est la deuxième image avec l’arrière-plan transparent de la damier.</span><span class="sxs-lookup"><span data-stu-id="eaaba-115">In this example, the output of the chroma-key effect is the second image with the checkerboard transparent background.</span></span> <span data-ttu-id="eaaba-116">La troisième image combine cela avec une image d’arrière-plan pour la superposition finale de l’écran vert.</span><span class="sxs-lookup"><span data-stu-id="eaaba-116">The third image combines this with a background image for the final green-screen overlay.</span></span>

## <a name="sample-code"></a><span data-ttu-id="eaaba-117">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="eaaba-117">Sample code</span></span>

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="eaaba-118">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="eaaba-118">Effect properties</span></span>

<span data-ttu-id="eaaba-119">Les propriétés de l’effet Chroma-Key sont définies par l’énumération [**d2d1 \_ CHROMAKEY \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) .</span><span class="sxs-lookup"><span data-stu-id="eaaba-119">The properties for the chroma-key effect are defined by the [**D2D1\_CHROMAKEY\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaaba-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaaba-120">Requirements</span></span>

| <span data-ttu-id="eaaba-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaaba-121">Requirement</span></span> | <span data-ttu-id="eaaba-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaaba-122">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="eaaba-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaaba-123">Minimum supported client</span></span> | <span data-ttu-id="eaaba-124">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="eaaba-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="eaaba-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaaba-125">Minimum supported server</span></span> | <span data-ttu-id="eaaba-126">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="eaaba-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="eaaba-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="eaaba-127">Header</span></span>                   | <span data-ttu-id="eaaba-128">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="eaaba-128">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="eaaba-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eaaba-129">Library</span></span>                  | <span data-ttu-id="eaaba-130">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="eaaba-130">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="eaaba-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eaaba-131">Related topics</span></span>

* [<span data-ttu-id="eaaba-132">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="eaaba-132">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
