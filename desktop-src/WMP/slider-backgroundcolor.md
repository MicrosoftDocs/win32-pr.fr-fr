---
title: Slider. backgroundColor
description: L’attribut backgroundColor spécifie ou récupère la couleur d’arrière-plan du contrôle Slider.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- Slider. backgroundColor lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542226"
---
# <a name="sliderbackgroundcolor"></a><span data-ttu-id="33816-104">Slider. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="33816-104">SLIDER.backgroundColor</span></span>

<span data-ttu-id="33816-105">L’attribut **backgroundColor** spécifie ou récupère la couleur d’arrière-plan du contrôle Slider.</span><span class="sxs-lookup"><span data-stu-id="33816-105">The **backgroundColor** attribute specifies or retrieves the background color of the slider control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="33816-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="33816-106">Possible Values</span></span>

<span data-ttu-id="33816-107">Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="33816-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="33816-108">Il n'a aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="33816-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33816-109">Notes</span><span class="sxs-lookup"><span data-stu-id="33816-109">Remarks</span></span>

<span data-ttu-id="33816-110">Un contrôle Slider de base peut être construit en spécifiant **backgroundColor** ou **BackgroundImage**, et **foregroundColor** ou **foregroundImage**.</span><span class="sxs-lookup"><span data-stu-id="33816-110">A basic slider control can be constructed by specifying **backgroundColor** or **backgroundImage**, and **foregroundColor** or **foregroundImage**.</span></span>

<span data-ttu-id="33816-111">Lorsque vous utilisez les couleurs, les dimensions du contrôle Slider définissent la zone remplie par la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="33816-111">When using the colors, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="33816-112">La couleur de premier plan couvre la couleur d’arrière-plan lorsque la position du curseur augmente.</span><span class="sxs-lookup"><span data-stu-id="33816-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="33816-113">Pour créer un remplissage dégradé de la zone occupée par la couleur d’arrière-plan ou de premier plan, spécifiez les attributs **backgroundEndColor** ou **foregroundEndColor** .</span><span class="sxs-lookup"><span data-stu-id="33816-113">To make a gradient fill of the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="33816-114">Consultez *CUSTOMSLIDER*. attribut [positionImage](customslider-positionimage.md) pour un exemple illustrant l’utilisation des attributs de l’élément **Slider** .</span><span class="sxs-lookup"><span data-stu-id="33816-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="33816-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33816-115">Requirements</span></span>



| <span data-ttu-id="33816-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33816-116">Requirement</span></span> | <span data-ttu-id="33816-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="33816-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="33816-118">Version</span><span class="sxs-lookup"><span data-stu-id="33816-118">Version</span></span><br/> | <span data-ttu-id="33816-119">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="33816-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33816-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33816-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33816-121">**Référence de couleur**</span><span class="sxs-lookup"><span data-stu-id="33816-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="33816-122">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="33816-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="33816-123">**Slider. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="33816-123">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="33816-124">**Slider. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="33816-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="33816-125">**Slider. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="33816-125">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="33816-126">**Slider. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="33816-126">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="33816-127">**Slider. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="33816-127">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





