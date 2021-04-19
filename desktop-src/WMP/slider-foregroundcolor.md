---
title: Slider. foregroundColor
description: L’attribut foregroundColor spécifie ou récupère la couleur de premier plan du contrôle Slider.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- Slider. foregroundColor lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534866"
---
# <a name="sliderforegroundcolor"></a><span data-ttu-id="5fd58-104">Slider. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="5fd58-104">SLIDER.foregroundColor</span></span>

<span data-ttu-id="5fd58-105">L’attribut **foregroundColor** spécifie ou récupère la couleur de premier plan du contrôle Slider.</span><span class="sxs-lookup"><span data-stu-id="5fd58-105">The **foregroundColor** attribute specifies or retrieves the foreground color of the slider control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="5fd58-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="5fd58-106">Possible Values</span></span>

<span data-ttu-id="5fd58-107">Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5fd58-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="5fd58-108">La valeur par défaut est « White ».</span><span class="sxs-lookup"><span data-stu-id="5fd58-108">The default value is "white".</span></span>

## <a name="remarks"></a><span data-ttu-id="5fd58-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5fd58-109">Remarks</span></span>

<span data-ttu-id="5fd58-110">Un contrôle Slider de base peut être construit en spécifiant l’une des deux paires d’attributs : **backgroundColor** et **ForegroundColor**, ou **BackgroundImage** et **foregroundImage**.</span><span class="sxs-lookup"><span data-stu-id="5fd58-110">A basic slider control can be constructed by specifying one of two pairs of attributes: the **backgroundColor** and **foregroundColor**, or the **backgroundImage** and **foregroundImage**.</span></span>

<span data-ttu-id="5fd58-111">Quand vous construisez un contrôle Slider à l’aide des attributs Color, les dimensions du contrôle Slider définissent la zone remplie par la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="5fd58-111">When you construct a slider control using the color attributes, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="5fd58-112">La couleur de premier plan couvre la couleur d’arrière-plan lorsque la position du curseur augmente.</span><span class="sxs-lookup"><span data-stu-id="5fd58-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="5fd58-113">Pour créer un remplissage dégradé dans la zone occupée par la couleur d’arrière-plan ou de premier plan, spécifiez les attributs **backgroundEndColor** ou **foregroundEndColor** .</span><span class="sxs-lookup"><span data-stu-id="5fd58-113">To make a gradient fill in the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="5fd58-114">Consultez *CUSTOMSLIDER*. attribut [positionImage](customslider-positionimage.md) pour un exemple illustrant l’utilisation des attributs de l’élément **Slider** .</span><span class="sxs-lookup"><span data-stu-id="5fd58-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd58-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fd58-115">Requirements</span></span>



| <span data-ttu-id="5fd58-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fd58-116">Requirement</span></span> | <span data-ttu-id="5fd58-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fd58-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5fd58-118">Version</span><span class="sxs-lookup"><span data-stu-id="5fd58-118">Version</span></span><br/> | <span data-ttu-id="5fd58-119">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="5fd58-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fd58-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fd58-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd58-121">**Référence de couleur**</span><span class="sxs-lookup"><span data-stu-id="5fd58-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="5fd58-122">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="5fd58-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="5fd58-123">**Slider. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="5fd58-123">**SLIDER.backgroundColor**</span></span>](slider-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="5fd58-124">**Slider. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="5fd58-124">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="5fd58-125">**Slider. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="5fd58-125">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="5fd58-126">**Slider. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="5fd58-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





