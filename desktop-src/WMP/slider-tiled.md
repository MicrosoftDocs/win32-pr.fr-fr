---
title: Slider. en mosaïque
description: L’attribut tileed spécifie ou récupère une valeur indiquant si l’image du curseur sera affichée en mosaïque.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Slider. lecteur Windows Media en mosaïque
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528739"
---
# <a name="slidertiled"></a><span data-ttu-id="c86e4-104">Slider. en mosaïque</span><span class="sxs-lookup"><span data-stu-id="c86e4-104">SLIDER.tiled</span></span>

<span data-ttu-id="c86e4-105">L’attribut **tileed** spécifie ou récupère une valeur indiquant si l’image du curseur sera affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="c86e4-105">The **tiled** attribute specifies or retrieves a value indicating whether the slider image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="c86e4-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c86e4-106">Possible Values</span></span>

<span data-ttu-id="c86e4-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c86e4-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="c86e4-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c86e4-108">Value</span></span> | <span data-ttu-id="c86e4-109">Description</span><span class="sxs-lookup"><span data-stu-id="c86e4-109">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c86e4-110">true</span><span class="sxs-lookup"><span data-stu-id="c86e4-110">true</span></span>  | <span data-ttu-id="c86e4-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="c86e4-111">Default.</span></span> <span data-ttu-id="c86e4-112">La bitmap de l’image est répétée jusqu’à ce qu’elle remplisse toute la région du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c86e4-112">The image bitmap will be repeated until it fills the entire region of the control.</span></span> |
| <span data-ttu-id="c86e4-113">false</span><span class="sxs-lookup"><span data-stu-id="c86e4-113">false</span></span> | <span data-ttu-id="c86e4-114">L’image ne sera pas affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="c86e4-114">The image will not be tiled.</span></span>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="c86e4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c86e4-115">Remarks</span></span>

<span data-ttu-id="c86e4-116">Cet attribut s’applique uniquement si vous utilisez des images de premier plan et d’arrière-plan pour définir un contrôle Slider.</span><span class="sxs-lookup"><span data-stu-id="c86e4-116">This attribute applies only if you are using foreground and background images to define a slider control.</span></span> <span data-ttu-id="c86e4-117">Si les images sont plus petites que la zone définie du curseur et que l’attribut **tileed** a la valeur true, les images sont répétées jusqu’à ce qu’elles remplissent la longueur totale du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c86e4-117">If the images are smaller than the defined area of the slider, and the **tiled** attribute is set to true, the images will be repeated until they fill the entire length of the control.</span></span>

<span data-ttu-id="c86e4-118">Vous pouvez utiliser cet attribut conjointement avec l’attribut de **bordure** .</span><span class="sxs-lookup"><span data-stu-id="c86e4-118">You may wish to use this attribute in conjunction with the **borderSize** attribute.</span></span> <span data-ttu-id="c86e4-119">L’attribut de **bordure** vous permet de définir une bordure qui n’est pas répétée pendant la mosaïque.</span><span class="sxs-lookup"><span data-stu-id="c86e4-119">The **borderSize** attribute allows you to define a border that is not repeated during tiling.</span></span>

## <a name="requirements"></a><span data-ttu-id="c86e4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c86e4-120">Requirements</span></span>



| <span data-ttu-id="c86e4-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c86e4-121">Requirement</span></span> | <span data-ttu-id="c86e4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c86e4-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c86e4-123">Version</span><span class="sxs-lookup"><span data-stu-id="c86e4-123">Version</span></span><br/> | <span data-ttu-id="c86e4-124">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c86e4-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c86e4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c86e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c86e4-126">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="c86e4-126">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="c86e4-127">**Slider. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="c86e4-127">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="c86e4-128">**Slider. bordure**</span><span class="sxs-lookup"><span data-stu-id="c86e4-128">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="c86e4-129">**Slider. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="c86e4-129">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





