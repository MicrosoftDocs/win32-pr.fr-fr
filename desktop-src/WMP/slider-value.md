---
title: Slider. Value
description: L’attribut value spécifie ou récupère la position actuelle du curseur. | Slider. Value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Slider. Value lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540443"
---
# <a name="slidervalue"></a><span data-ttu-id="00198-105">Slider. Value</span><span class="sxs-lookup"><span data-stu-id="00198-105">SLIDER.value</span></span>

<span data-ttu-id="00198-106">L’attribut **value** spécifie ou récupère la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="00198-106">The **value** attribute specifies or retrieves the current position of the slider.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="00198-107">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="00198-107">Possible Values</span></span>

<span data-ttu-id="00198-108">Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur par défaut est **min**.</span><span class="sxs-lookup"><span data-stu-id="00198-108">This attribute is a read/write **Number** (**float**) with a default value of **min**.</span></span>

## <a name="remarks"></a><span data-ttu-id="00198-109">Notes</span><span class="sxs-lookup"><span data-stu-id="00198-109">Remarks</span></span>

<span data-ttu-id="00198-110">La **valeur** doit toujours être supérieure ou égale à **min** et inférieure ou égale à **Max**. Si vous spécifiez une valeur en dehors de cette plage, la **valeur** et la position du curseur ne sont pas modifiées.</span><span class="sxs-lookup"><span data-stu-id="00198-110">The **value** should always be greater than or equal to **min** and less than or equal to **max**. If you specify a value outside this range, **value** and the position of the slider are not changed.</span></span>

<span data-ttu-id="00198-111">Consultez **CUSTOMSLIDER**. attribut [positionImage](customslider-positionimage.md) pour un exemple illustrant l’utilisation des attributs de l’élément **Slider** .</span><span class="sxs-lookup"><span data-stu-id="00198-111">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="00198-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00198-112">Requirements</span></span>



| <span data-ttu-id="00198-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00198-113">Requirement</span></span> | <span data-ttu-id="00198-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="00198-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="00198-115">Version</span><span class="sxs-lookup"><span data-stu-id="00198-115">Version</span></span><br/> | <span data-ttu-id="00198-116">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="00198-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="00198-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00198-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00198-118">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="00198-118">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="00198-119">**Slider. min.**</span><span class="sxs-lookup"><span data-stu-id="00198-119">**SLIDER.min**</span></span>](slider-min.md)
</dt> </dl>

 

 





