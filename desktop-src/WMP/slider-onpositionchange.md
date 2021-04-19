---
title: Slider. onPositionChange
description: Le gestionnaire d’événements onPositionChange gère un événement qui se produit lorsque la position du curseur change suite à un clic ou un glissement de l’utilisateur. | Slider. onPositionChange
ms.assetid: c18e9a49-9576-42ae-9f30-249c44d40f41
keywords:
- Slider. onPositionChange lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68faa9e7addd85b9b5f02b8a6c445e7ddf54e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529934"
---
# <a name="slideronpositionchange"></a><span data-ttu-id="0e175-105">Slider. onPositionChange</span><span class="sxs-lookup"><span data-stu-id="0e175-105">SLIDER.onPositionChange</span></span>

<span data-ttu-id="0e175-106">Le gestionnaire d’événements **onPositionChange** gère un événement qui se produit lorsque la position du curseur change suite à un clic ou un glissement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e175-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="0e175-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0e175-107">Remarks</span></span>

<span data-ttu-id="0e175-108">Si la position du curseur change à la suite de la modification de l’attribut de **valeur** dans le script, cet événement n’est pas déclenché.</span><span class="sxs-lookup"><span data-stu-id="0e175-108">If the position of the slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="0e175-109">Pour tenir compte de cette possibilité, implémentez plutôt le gestionnaire d’événements **\_ OnChange value** .</span><span class="sxs-lookup"><span data-stu-id="0e175-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e175-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e175-110">Requirements</span></span>



| <span data-ttu-id="0e175-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e175-111">Requirement</span></span> | <span data-ttu-id="0e175-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e175-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0e175-113">Version</span><span class="sxs-lookup"><span data-stu-id="0e175-113">Version</span></span><br/> | <span data-ttu-id="0e175-114">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="0e175-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e175-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e175-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e175-116">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="0e175-116">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





