---
title: Slider. backgroundImage
description: L’attribut backgroundImage spécifie ou récupère l’image d’arrière-plan du curseur.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- Slider. backgroundImage lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535872"
---
# <a name="sliderbackgroundimage"></a><span data-ttu-id="7b79b-104">Slider. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="7b79b-104">SLIDER.backgroundImage</span></span>

<span data-ttu-id="7b79b-105">L’attribut **BackgroundImage** spécifie ou récupère l’image d’arrière-plan du curseur.</span><span class="sxs-lookup"><span data-stu-id="7b79b-105">The **backgroundImage** attribute specifies or retrieves the background image of the slider.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="7b79b-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7b79b-106">Possible Values</span></span>

<span data-ttu-id="7b79b-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="7b79b-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b79b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7b79b-108">Remarks</span></span>

<span data-ttu-id="7b79b-109">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7b79b-109">This attribute is optional.</span></span> <span data-ttu-id="7b79b-110">Lorsque vous utilisez des images pour construire un curseur, l' **BackgroundImage** est utilisé pour l’image de curseur principale.</span><span class="sxs-lookup"><span data-stu-id="7b79b-110">When using images to construct a slider, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="7b79b-111">Le **thumbImage** représente le curseur réel et peut être déplacé à l’aide de la souris.</span><span class="sxs-lookup"><span data-stu-id="7b79b-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="7b79b-112">Au niveau du curseur **thumbImage** se trouve une ligne invisible dans laquelle l’image d’arrière-plan est affichée d’un côté de la ligne, et l’image de premier plan s’affiche de l’autre côté.</span><span class="sxs-lookup"><span data-stu-id="7b79b-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="7b79b-113">Lorsque le curseur **thumbImage** est déplacé à l’aide de la souris, si la **diapositive** est définie sur true, l’image de premier plan glisse comme si elle était extraite par le curseur pour couvrir l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="7b79b-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="7b79b-114">Si la **diapositive** est définie sur false, l’image de premier plan ne se déplace pas, mais elle est révélée en place, comme si le curseur déplace l’image d’arrière-plan hors de l’image de premier plan.</span><span class="sxs-lookup"><span data-stu-id="7b79b-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="7b79b-115">Si l’attribut **tileed** a la valeur true et que l’image d’arrière-plan est plus petite que le contrôle Slider, l’image est affichée en mosaïque horizontale ou verticale en fonction de l’attribut **direction** .</span><span class="sxs-lookup"><span data-stu-id="7b79b-115">If the **tiled** attribute is set to true and the background image is smaller than the slider control, the image will be tiled either horizontally or vertically depending on the **direction** attribute.</span></span> <span data-ttu-id="7b79b-116">Si l’attribut de **bordure** est défini sur une valeur supérieure à zéro, le nombre spécifié est le nombre de pixels à partir de la gauche et de la droite ou du haut et du bas de l’image (là encore, en fonction de l’attribut de **direction** ) qui sera réservé pour les bordures du contrôle Slider.</span><span class="sxs-lookup"><span data-stu-id="7b79b-116">If the **borderSize** attribute is set to a value greater than zero, the number specified will be the number of pixels from the left and right or top and bottom of the image (again, depending on the **direction** attribute) that will be reserved for the borders of the slider control.</span></span> <span data-ttu-id="7b79b-117">Dans ce cas, seule la partie centrale de l’image est utilisée pour la mosaïque du reste du contrôle.</span><span class="sxs-lookup"><span data-stu-id="7b79b-117">In this case, only the central portion of the image is used for tiling the remainder of the control.</span></span>

<span data-ttu-id="7b79b-118">Les formats pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).</span><span class="sxs-lookup"><span data-stu-id="7b79b-118">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b79b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b79b-119">Requirements</span></span>



| <span data-ttu-id="7b79b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b79b-120">Requirement</span></span> | <span data-ttu-id="7b79b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b79b-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7b79b-122">Version</span><span class="sxs-lookup"><span data-stu-id="7b79b-122">Version</span></span><br/> | <span data-ttu-id="7b79b-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="7b79b-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b79b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b79b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b79b-125">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="7b79b-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="7b79b-126">**Slider. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="7b79b-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="7b79b-127">**Slider. Slide**</span><span class="sxs-lookup"><span data-stu-id="7b79b-127">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="7b79b-128">**Slider. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="7b79b-128">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> </dl>

 

 





