---
title: Effet Postérisation
description: L’effet Postérisation réduit le nombre de couleurs uniques dans une image.
ms.assetid: e6686998-1246-b3b7-6f4f-212568c3191c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c98c55154300f7b29c23c24e97570335c6e930f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033033"
---
# <a name="posterize-effect"></a><span data-ttu-id="e7ebe-103">Effet Postérisation</span><span class="sxs-lookup"><span data-stu-id="e7ebe-103">Posterize effect</span></span>

<span data-ttu-id="e7ebe-104">L’effet Postérisation réduit le nombre de couleurs uniques dans une image.</span><span class="sxs-lookup"><span data-stu-id="e7ebe-104">The posterize effect reduces the number of unique colors in an image.</span></span>

<span data-ttu-id="e7ebe-105">Le CLSID de cet effet est CLSID \_ D2D1Posterize.</span><span class="sxs-lookup"><span data-stu-id="e7ebe-105">The CLSID for this effect is CLSID\_D2D1Posterize.</span></span>

-   [<span data-ttu-id="e7ebe-106">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="e7ebe-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="e7ebe-107">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e7ebe-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="e7ebe-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="e7ebe-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e7ebe-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7ebe-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e7ebe-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7ebe-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="e7ebe-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="e7ebe-111">Example image</span></span>

![exemple de sortie d’effet](images/posterize-effect.png)

## <a name="sample-code"></a><span data-ttu-id="e7ebe-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="e7ebe-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> posterizeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Posterize, &posterizeEffect);
 
posterizeEffect->SetInput(0, bitmap);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, 4);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(posterizeEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="e7ebe-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="e7ebe-114">Effect properties</span></span>

<span data-ttu-id="e7ebe-115">Les propriétés de l’effet Postérisation sont définies par l’énumération [**\_ \_ props d2d1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) .</span><span class="sxs-lookup"><span data-stu-id="e7ebe-115">The properties for the posterize effect are defined by the [**D2D1\_POSTERIZE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ebe-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7ebe-116">Requirements</span></span>



| <span data-ttu-id="e7ebe-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7ebe-117">Requirement</span></span> | <span data-ttu-id="e7ebe-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7ebe-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="e7ebe-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7ebe-119">Minimum supported client</span></span> | <span data-ttu-id="e7ebe-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e7ebe-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e7ebe-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7ebe-121">Minimum supported server</span></span> | <span data-ttu-id="e7ebe-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e7ebe-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e7ebe-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7ebe-123">Header</span></span>                   | <span data-ttu-id="e7ebe-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="e7ebe-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="e7ebe-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7ebe-125">Library</span></span>                  | <span data-ttu-id="e7ebe-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e7ebe-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="e7ebe-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7ebe-127">Related topics</span></span>

* [<span data-ttu-id="e7ebe-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="e7ebe-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


