---
title: Effet de température et de teinte
description: Effet de température et de teinte
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c3628e1fdcb1c72a84a9e08736e4215d55514
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096637"
---
# <a name="temperature-and-tint-effect"></a><span data-ttu-id="9a078-103">Effet de température et de teinte</span><span class="sxs-lookup"><span data-stu-id="9a078-103">Temperature and tint effect</span></span>

<span data-ttu-id="9a078-104">Le CLSID de cet effet est CLSID \_ D2D1TemperatureTint.</span><span class="sxs-lookup"><span data-stu-id="9a078-104">The CLSID for this effect is CLSID\_D2D1TemperatureTint.</span></span>

## <a name="sample-code"></a><span data-ttu-id="9a078-105">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="9a078-105">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="9a078-106">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="9a078-106">Effect properties</span></span>

<span data-ttu-id="9a078-107">Les propriétés de l’effet température et teinte sont définies par l’énumération [**d2d1 \_ TEMPERATUREANDTINT \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) .</span><span class="sxs-lookup"><span data-stu-id="9a078-107">The properties for the temperature and tint effect are defined by the [**D2D1\_TEMPERATUREANDTINT\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a078-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a078-108">Requirements</span></span>



| <span data-ttu-id="9a078-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a078-109">Requirement</span></span> | <span data-ttu-id="9a078-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a078-110">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="9a078-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a078-111">Minimum supported client</span></span> | <span data-ttu-id="9a078-112">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9a078-112">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9a078-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a078-113">Minimum supported server</span></span> | <span data-ttu-id="9a078-114">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9a078-114">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9a078-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a078-115">Header</span></span>                   | <span data-ttu-id="9a078-116">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="9a078-116">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="9a078-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9a078-117">Library</span></span>                  | <span data-ttu-id="9a078-118">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="9a078-118">d2d1.lib, dxguid.lib</span></span>                              |



 

## <a name="related-topics"></a><span data-ttu-id="9a078-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a078-119">Related topics</span></span>

* [<span data-ttu-id="9a078-120">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="9a078-120">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
