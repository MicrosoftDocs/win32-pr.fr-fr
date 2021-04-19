---
title: CUSTOMSLIDER.onPositionChange
description: Le gestionnaire d’événements onPositionChange gère un événement qui se produit lorsque la position du curseur change suite à un clic ou un glissement de l’utilisateur. | CUSTOMSLIDER.onPositionChange
ms.assetid: d8fe99a2-69ff-4e75-8d7d-506bcb2f75bf
keywords:
- Lecteur Windows Media CUSTOMSLIDER. onPositionChange
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3d5547d66ca6dc1b770242301bd95ed010a8d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538111"
---
# <a name="customslideronpositionchange"></a><span data-ttu-id="c2189-105">CUSTOMSLIDER.onPositionChange</span><span class="sxs-lookup"><span data-stu-id="c2189-105">CUSTOMSLIDER.onPositionChange</span></span>

<span data-ttu-id="c2189-106">Le gestionnaire d’événements **onPositionChange** gère un événement qui se produit lorsque la position du curseur change suite à un clic ou un glissement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2189-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="c2189-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c2189-107">Remarks</span></span>

<span data-ttu-id="c2189-108">Si la position du curseur personnalisé change à la suite de la modification de l’attribut de **valeur** dans le script, cet événement n’est pas déclenché.</span><span class="sxs-lookup"><span data-stu-id="c2189-108">If the position of the custom slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="c2189-109">Pour tenir compte de cette possibilité, implémentez plutôt le gestionnaire d’événements **\_ OnChange value** .</span><span class="sxs-lookup"><span data-stu-id="c2189-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2189-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2189-110">Requirements</span></span>



| <span data-ttu-id="c2189-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2189-111">Requirement</span></span> | <span data-ttu-id="c2189-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2189-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c2189-113">Version</span><span class="sxs-lookup"><span data-stu-id="c2189-113">Version</span></span><br/> | <span data-ttu-id="c2189-114">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c2189-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2189-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2189-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2189-116">**Élément CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="c2189-116">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





