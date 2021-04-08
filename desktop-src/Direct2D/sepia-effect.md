---
title: Effet sépia
description: convertit une image en tons sépia.
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6ead1d439e86cbd35be14d1f0ae32923de408d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942010"
---
# <a name="sepia-effect"></a><span data-ttu-id="e520f-103">Effet sépia</span><span class="sxs-lookup"><span data-stu-id="e520f-103">Sepia effect</span></span>

<span data-ttu-id="e520f-104">convertit une image en tons sépia.</span><span class="sxs-lookup"><span data-stu-id="e520f-104">Converts an image to sepia tones.</span></span>

<span data-ttu-id="e520f-105">Le CLSID de cet effet est CLSID \_ D2D1Sepia.</span><span class="sxs-lookup"><span data-stu-id="e520f-105">The CLSID for this effect is CLSID\_D2D1Sepia.</span></span>

-   [<span data-ttu-id="e520f-106">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="e520f-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="e520f-107">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e520f-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="e520f-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="e520f-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e520f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e520f-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e520f-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e520f-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="e520f-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="e520f-111">Example image</span></span>

![exemple de sortie d’effet](images/sepia-effect.png)

## <a name="sample-code"></a><span data-ttu-id="e520f-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="e520f-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="e520f-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="e520f-114">Effect properties</span></span>

<span data-ttu-id="e520f-115">Les propriétés de l’effet sépia sont définies par l’énumération [**d2d1 \_ sépia \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) .</span><span class="sxs-lookup"><span data-stu-id="e520f-115">The properties for the sepia effect are defined by the [**D2D1\_SEPIA\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e520f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e520f-116">Requirements</span></span>



| <span data-ttu-id="e520f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e520f-117">Requirement</span></span> | <span data-ttu-id="e520f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e520f-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="e520f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e520f-119">Minimum supported client</span></span> | <span data-ttu-id="e520f-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e520f-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e520f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e520f-121">Minimum supported server</span></span> | <span data-ttu-id="e520f-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e520f-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e520f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e520f-123">Header</span></span>                   | <span data-ttu-id="e520f-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="e520f-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="e520f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e520f-125">Library</span></span>                  | <span data-ttu-id="e520f-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e520f-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="e520f-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e520f-127">Related topics</span></span>

* [<span data-ttu-id="e520f-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="e520f-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




