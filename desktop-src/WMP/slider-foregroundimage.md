---
title: Slider. foregroundImage
description: L’attribut foregroundImage spécifie ou récupère l’image de premier plan du curseur.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- Slider. foregroundImage lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525618"
---
# <a name="sliderforegroundimage"></a><span data-ttu-id="eacac-104">Slider. foregroundImage</span><span class="sxs-lookup"><span data-stu-id="eacac-104">SLIDER.foregroundImage</span></span>

<span data-ttu-id="eacac-105">L’attribut **foregroundImage** spécifie ou récupère l’image de premier plan du curseur.</span><span class="sxs-lookup"><span data-stu-id="eacac-105">The **foregroundImage** attribute specifies or retrieves the foreground image of the slider.</span></span>

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a><span data-ttu-id="eacac-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="eacac-106">Possible Values</span></span>

<span data-ttu-id="eacac-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="eacac-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="eacac-108">Notes</span><span class="sxs-lookup"><span data-stu-id="eacac-108">Remarks</span></span>

<span data-ttu-id="eacac-109">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="eacac-109">This attribute is optional.</span></span> <span data-ttu-id="eacac-110">Lorsque vous utilisez des images pour construire un contrôle Slider, l' **BackgroundImage** est utilisé pour l’image de curseur principale.</span><span class="sxs-lookup"><span data-stu-id="eacac-110">When using images to construct a slider control, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="eacac-111">Le **thumbImage** représente le curseur réel et peut être déplacé à l’aide de la souris.</span><span class="sxs-lookup"><span data-stu-id="eacac-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="eacac-112">Au niveau du curseur **thumbImage** se trouve une ligne invisible dans laquelle l’image d’arrière-plan est affichée d’un côté de la ligne, et l’image de premier plan s’affiche de l’autre côté.</span><span class="sxs-lookup"><span data-stu-id="eacac-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="eacac-113">Lorsque le curseur **thumbImage** est déplacé à l’aide de la souris, si la **diapositive** est définie sur true, l’image de premier plan glisse comme si elle était extraite par le curseur pour couvrir l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="eacac-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="eacac-114">Si la **diapositive** est définie sur false, l’image de premier plan ne se déplace pas, mais elle est révélée en place, comme si le curseur déplace l’image d’arrière-plan hors de l’image de premier plan.</span><span class="sxs-lookup"><span data-stu-id="eacac-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="eacac-115">Si l’attribut **tileed** a la valeur true et que l’image de premier plan est plus petite que la zone de premier plan du contrôle Slider, l’image est affichée en mosaïque horizontalement ou verticalement, selon l’attribut **direction** , pour occuper l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="eacac-115">If the **tiled** attribute is set to true and the foreground image is smaller than the foreground area of the slider control, the image will be tiled either horizontally or vertically, depending on the **direction** attribute, to fill the available space.</span></span>

<span data-ttu-id="eacac-116">Les formats pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).</span><span class="sxs-lookup"><span data-stu-id="eacac-116">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="eacac-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eacac-117">Requirements</span></span>



| <span data-ttu-id="eacac-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eacac-118">Requirement</span></span> | <span data-ttu-id="eacac-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="eacac-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="eacac-120">Version</span><span class="sxs-lookup"><span data-stu-id="eacac-120">Version</span></span><br/> | <span data-ttu-id="eacac-121">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="eacac-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eacac-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eacac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eacac-123">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="eacac-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="eacac-124">**Slider. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="eacac-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="eacac-125">**Slider. Slide**</span><span class="sxs-lookup"><span data-stu-id="eacac-125">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="eacac-126">**Slider. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="eacac-126">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="eacac-127">**Slider. Value**</span><span class="sxs-lookup"><span data-stu-id="eacac-127">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





