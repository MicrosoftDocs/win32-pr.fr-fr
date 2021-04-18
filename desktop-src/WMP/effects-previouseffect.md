---
title: EFFECTs. previousEffect
description: La méthode previousEffect affiche la visualisation précédente, en ignorant les présélections.
ms.assetid: f1cfef29-0241-4028-b047-4f17bf0e9250
keywords:
- EFFECTs. previousEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.previousEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5482e7c202d6d35f3a833b5bafc8a41dca38956
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543192"
---
# <a name="effectspreviouseffect"></a><span data-ttu-id="52205-104">EFFECTs. previousEffect</span><span class="sxs-lookup"><span data-stu-id="52205-104">EFFECTS.previousEffect</span></span>

<span data-ttu-id="52205-105">La méthode **previousEffect** affiche la visualisation précédente, en ignorant les présélections.</span><span class="sxs-lookup"><span data-stu-id="52205-105">The **previousEffect** method displays the previous visualization, skipping presets.</span></span>

``` syntax
        elementID.previousEffect()
```

## <a name="parameters"></a><span data-ttu-id="52205-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52205-106">Parameters</span></span>

<span data-ttu-id="52205-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="52205-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52205-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="52205-108">Return Value</span></span>

<span data-ttu-id="52205-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="52205-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52205-110">Notes</span><span class="sxs-lookup"><span data-stu-id="52205-110">Remarks</span></span>

<span data-ttu-id="52205-111">Cette méthode affiche la visualisation précédente dans l’ordre de création.</span><span class="sxs-lookup"><span data-stu-id="52205-111">This method displays the previous visualization in the authoring order.</span></span> <span data-ttu-id="52205-112">Si la visualisation actuelle est la première dans l’ordre de création et si **AutoriserTout** a la valeur false, la dernière visualisation est rendue active.</span><span class="sxs-lookup"><span data-stu-id="52205-112">If the current visualization is the first in the authoring order, and if **allowAll** is false, the last visualization is made current.</span></span>

## <a name="requirements"></a><span data-ttu-id="52205-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52205-113">Requirements</span></span>



| <span data-ttu-id="52205-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52205-114">Requirement</span></span> | <span data-ttu-id="52205-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="52205-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="52205-116">Version</span><span class="sxs-lookup"><span data-stu-id="52205-116">Version</span></span><br/> | <span data-ttu-id="52205-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="52205-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52205-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52205-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52205-119">**Élément EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="52205-119">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="52205-120">**EFFECTs. nextEffect**</span><span class="sxs-lookup"><span data-stu-id="52205-120">**EFFECTS.nextEffect**</span></span>](effects-nexteffect.md)
</dt> <dt>

[<span data-ttu-id="52205-121">**EFFECTs. AutoriserTout**</span><span class="sxs-lookup"><span data-stu-id="52205-121">**EFFECTS.allowAll**</span></span>](effects-allowall.md)
</dt> </dl>

 

 





