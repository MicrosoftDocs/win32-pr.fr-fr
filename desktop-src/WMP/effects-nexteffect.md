---
title: EFFECTs. nextEffect
description: La méthode nextEffect affiche la première présélection de la visualisation suivante, en ignorant les présélections intermédiaires.
ms.assetid: dedd8e8b-2337-46f5-91a8-43ef54c86012
keywords:
- EFFECTs. nextEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.nextEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b84d7ec4d6095ffdac2a0f0592aa3f3e832e68e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543832"
---
# <a name="effectsnexteffect"></a><span data-ttu-id="8a669-104">EFFECTs. nextEffect</span><span class="sxs-lookup"><span data-stu-id="8a669-104">EFFECTS.nextEffect</span></span>

<span data-ttu-id="8a669-105">La méthode **nextEffect** affiche la première présélection de la visualisation suivante, en ignorant les présélections intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="8a669-105">The **nextEffect** method displays the first preset of the next visualization, skipping intervening presets.</span></span>

``` syntax
        elementID.nextEffect()
```

## <a name="parameters"></a><span data-ttu-id="8a669-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a669-106">Parameters</span></span>

<span data-ttu-id="8a669-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8a669-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a669-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8a669-108">Return Value</span></span>

<span data-ttu-id="8a669-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8a669-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a669-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8a669-110">Remarks</span></span>

<span data-ttu-id="8a669-111">Cette méthode affiche la première présélection de la visualisation suivante dans l’ordre de création.</span><span class="sxs-lookup"><span data-stu-id="8a669-111">This method displays the first preset of the next visualization in the authoring order.</span></span> <span data-ttu-id="8a669-112">Si la visualisation actuelle est la dernière dans l’ordre de création et si **AutoriserTout** a la valeur false, la première visualisation est rendue active.</span><span class="sxs-lookup"><span data-stu-id="8a669-112">If the current visualization is the last in the authoring order, and if **allowAll** is false, the first visualization is made current.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a669-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a669-113">Requirements</span></span>



| <span data-ttu-id="8a669-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a669-114">Requirement</span></span> | <span data-ttu-id="8a669-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a669-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8a669-116">Version</span><span class="sxs-lookup"><span data-stu-id="8a669-116">Version</span></span><br/> | <span data-ttu-id="8a669-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8a669-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a669-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a669-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a669-119">**Élément EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="8a669-119">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="8a669-120">**EFFECTs. AutoriserTout**</span><span class="sxs-lookup"><span data-stu-id="8a669-120">**EFFECTS.allowAll**</span></span>](effects-allowall.md)
</dt> <dt>

[<span data-ttu-id="8a669-121">**EFFECTs. previousEffect**</span><span class="sxs-lookup"><span data-stu-id="8a669-121">**EFFECTS.previousEffect**</span></span>](effects-previouseffect.md)
</dt> </dl>

 

 





