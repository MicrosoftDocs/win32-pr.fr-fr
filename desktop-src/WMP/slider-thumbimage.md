---
title: Slider. thumbImage
description: L’attribut thumbImage spécifie ou récupère l’image qui sera utilisée pour représenter la position actuelle du curseur.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- Slider. thumbImage lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541598"
---
# <a name="sliderthumbimage"></a><span data-ttu-id="d94aa-104">Slider. thumbImage</span><span class="sxs-lookup"><span data-stu-id="d94aa-104">SLIDER.thumbImage</span></span>

<span data-ttu-id="d94aa-105">L’attribut **thumbImage** spécifie ou récupère l’image qui sera utilisée pour représenter la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="d94aa-105">The **thumbImage** attribute specifies or retrieves the image that will be used to represent the current position of the slider.</span></span>

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a><span data-ttu-id="d94aa-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d94aa-106">Possible Values</span></span>

<span data-ttu-id="d94aa-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="d94aa-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="d94aa-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d94aa-108">Remarks</span></span>

<span data-ttu-id="d94aa-109">Le **thumbImage** spécifie l’image qui sera utilisée pour représenter la position actuelle, ainsi que pour indiquer que l’utilisateur peut agir avec le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d94aa-109">The **thumbImage** specifies the image that will be used to represent current position, as well as indicate that the user can take action with the control.</span></span> <span data-ttu-id="d94aa-110">Si aucune image Thumb n’est spécifiée, le curseur est non interactif.</span><span class="sxs-lookup"><span data-stu-id="d94aa-110">If no thumb image is specified, the slider is non-interactive.</span></span>

<span data-ttu-id="d94aa-111">L’image Thumb est centrée dans la dimension étroite du contrôle Slider.</span><span class="sxs-lookup"><span data-stu-id="d94aa-111">The thumb image is centered in the narrow dimension of the slider control.</span></span> <span data-ttu-id="d94aa-112">Si l’image Thumb est plus étroite que le contrôle, l’image apparaît au milieu de l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="d94aa-112">If the thumb image is narrower than the control, the image appears in the middle of the background.</span></span> <span data-ttu-id="d94aa-113">Si l’image Thumb est plus grande que le contrôle, les extrémités de l’image sont coupées.</span><span class="sxs-lookup"><span data-stu-id="d94aa-113">If the thumb image is larger than the control, the ends of the image are cut off.</span></span>

<span data-ttu-id="d94aa-114">La position du curseur est spécifiée par le centre de l’image Thumb.</span><span class="sxs-lookup"><span data-stu-id="d94aa-114">The position of the slider is specified by the center of the thumb image.</span></span> <span data-ttu-id="d94aa-115">Si la **bordure** est égale à zéro, seule la moitié de l’image Thumb sera visible aux positions des curseurs de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="d94aa-115">If **borderSize** is zero, only half the thumb image will be visible at the beginning and end slider positions.</span></span> <span data-ttu-id="d94aa-116">Pour éviter cela, définissez la **bordure** sur une valeur supérieure ou égale à la moitié de la largeur de l’image Thumb (ou de la moitié de la hauteur si la **direction** est définie sur « vertical »).</span><span class="sxs-lookup"><span data-stu-id="d94aa-116">To prevent this, set **borderSize** to a value greater than or equal to half the width of the thumb image (or half the height if **direction** is set to "vertical").</span></span>

<span data-ttu-id="d94aa-117">Les formats pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).</span><span class="sxs-lookup"><span data-stu-id="d94aa-117">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

<span data-ttu-id="d94aa-118">Consultez **CUSTOMSLIDER**. attribut [positionImage](customslider-positionimage.md) pour un exemple illustrant l’utilisation des attributs de l’élément **Slider** .</span><span class="sxs-lookup"><span data-stu-id="d94aa-118">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d94aa-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d94aa-119">Requirements</span></span>



| <span data-ttu-id="d94aa-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d94aa-120">Requirement</span></span> | <span data-ttu-id="d94aa-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d94aa-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d94aa-122">Version</span><span class="sxs-lookup"><span data-stu-id="d94aa-122">Version</span></span><br/> | <span data-ttu-id="d94aa-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="d94aa-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d94aa-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d94aa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94aa-125">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="d94aa-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="d94aa-126">**Slider. bordure**</span><span class="sxs-lookup"><span data-stu-id="d94aa-126">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="d94aa-127">**Slider. direction**</span><span class="sxs-lookup"><span data-stu-id="d94aa-127">**SLIDER.direction**</span></span>](slider-direction.md)
</dt> </dl>

 

 





