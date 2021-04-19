---
title: Slider. Slide
description: L’attribut Slide spécifie ou récupère une valeur indiquant si l’image de premier plan glisse sur l’image d’arrière-plan ou est progressivement révélée dans une position statique sur l’image d’arrière-plan.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Slider. glissement du lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535007"
---
# <a name="sliderslide"></a><span data-ttu-id="743ac-104">Slider. Slide</span><span class="sxs-lookup"><span data-stu-id="743ac-104">SLIDER.slide</span></span>

<span data-ttu-id="743ac-105">L’attribut **Slide** spécifie ou récupère une valeur indiquant si l’image de premier plan glisse sur l’image d’arrière-plan ou est progressivement révélée dans une position statique sur l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="743ac-105">The **slide** attribute specifies or retrieves a value indicating whether the foreground image slides over the background image or is gradually revealed in a static position over the background image.</span></span>

``` syntax
        elementID.slide
```

## <a name="possible-values"></a><span data-ttu-id="743ac-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="743ac-106">Possible Values</span></span>

<span data-ttu-id="743ac-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="743ac-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="743ac-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="743ac-108">Value</span></span> | <span data-ttu-id="743ac-109">Description</span><span class="sxs-lookup"><span data-stu-id="743ac-109">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="743ac-110">true</span><span class="sxs-lookup"><span data-stu-id="743ac-110">true</span></span>  | <span data-ttu-id="743ac-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="743ac-111">Default.</span></span> <span data-ttu-id="743ac-112">L’image de premier plan glisse sur l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="743ac-112">The foreground image slides over the background image.</span></span>      |
| <span data-ttu-id="743ac-113">false</span><span class="sxs-lookup"><span data-stu-id="743ac-113">false</span></span> | <span data-ttu-id="743ac-114">L’image de premier plan est révélée sur l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="743ac-114">The foreground image is revealed in place over the background image.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="743ac-115">Notes</span><span class="sxs-lookup"><span data-stu-id="743ac-115">Remarks</span></span>

<span data-ttu-id="743ac-116">Lorsque le curseur **thumbImage** est déplacé à l’aide de la souris, si la **diapositive** est définie sur true, l’image de premier plan glisse comme si elle était extraite par le curseur pour couvrir l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="743ac-116">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="743ac-117">Si la **diapositive** est définie sur false, l’image de premier plan ne se déplace pas, mais elle est révélée en place, comme si le curseur déplace l’image d’arrière-plan hors de l’image de premier plan.</span><span class="sxs-lookup"><span data-stu-id="743ac-117">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

## <a name="requirements"></a><span data-ttu-id="743ac-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="743ac-118">Requirements</span></span>



| <span data-ttu-id="743ac-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="743ac-119">Requirement</span></span> | <span data-ttu-id="743ac-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="743ac-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="743ac-121">Version</span><span class="sxs-lookup"><span data-stu-id="743ac-121">Version</span></span><br/> | <span data-ttu-id="743ac-122">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="743ac-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="743ac-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="743ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="743ac-124">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="743ac-124">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="743ac-125">**Slider. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="743ac-125">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="743ac-126">**Slider. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="743ac-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





