---
title: Slider. bordure
description: L’attribut de bordure spécifie ou récupère la largeur de la bordure en pixels.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Slider. bordure du lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539286"
---
# <a name="sliderbordersize"></a><span data-ttu-id="06acb-104">Slider. bordure</span><span class="sxs-lookup"><span data-stu-id="06acb-104">SLIDER.borderSize</span></span>

<span data-ttu-id="06acb-105">L’attribut de **bordure** spécifie ou récupère la largeur de la bordure en pixels.</span><span class="sxs-lookup"><span data-stu-id="06acb-105">The **borderSize** attribute specifies or retrieves the border width in pixels.</span></span>

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a><span data-ttu-id="06acb-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="06acb-106">Possible Values</span></span>

<span data-ttu-id="06acb-107">Cet attribut est un **nombre** en lecture/écriture (**long**) représentant la largeur de la bordure en pixels.</span><span class="sxs-lookup"><span data-stu-id="06acb-107">This attribute is a read/write **Number** (**long**) representing the border width in pixels.</span></span> <span data-ttu-id="06acb-108">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="06acb-108">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="06acb-109">Notes</span><span class="sxs-lookup"><span data-stu-id="06acb-109">Remarks</span></span>

<span data-ttu-id="06acb-110">Cet attribut définit un décalage à partir du début et de la fin du contrôle Slider, de gauche à droite si l’attribut **direction** est défini sur « horizontal », et du haut et du bas s’il est défini sur « vertical ».</span><span class="sxs-lookup"><span data-stu-id="06acb-110">This attribute defines an offset from the beginning and end of the slider control that is, from the left and right if the **direction** attribute is set to "horizontal", and from the top and bottom if it is set to "vertical".</span></span> <span data-ttu-id="06acb-111">Ces positions de décalage déterminent les positions minimale et maximale du curseur de défilement, au-delà duquel la couleur ou l’image de premier plan ne sera pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="06acb-111">These offset positions dictate the minimum and maximum positions of the slider thumb, beyond which the foreground color or image will not be applied.</span></span>

<span data-ttu-id="06acb-112">Si une image d’arrière-plan est utilisée avec l’attribut **tileed** défini sur true, le décalage est appliqué à l’image, en dictant la quantité d’image (à partir de la gauche et de la droite ou du haut et du bas) à utiliser pour les bordures de début et de fin du contrôle Slider, avec la partie centrale de l’image en mosaïque dans le reste.</span><span class="sxs-lookup"><span data-stu-id="06acb-112">If a background image is used with the **tiled** attribute set to true, the offset is applied to the image, dictating the amount of the image (either from the left and right or from the top and bottom) to be used for the beginning and end borders of the slider control, with the central portion of the image being tiled throughout the remainder.</span></span> <span data-ttu-id="06acb-113">De cette façon, une petite image d’arrière-plan peut être utilisée pour couvrir la longueur totale d’un contrôle Slider plus grand.</span><span class="sxs-lookup"><span data-stu-id="06acb-113">In this way, a small background image can be used to cover the full length of a larger slider control.</span></span>

## <a name="requirements"></a><span data-ttu-id="06acb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06acb-114">Requirements</span></span>



| <span data-ttu-id="06acb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06acb-115">Requirement</span></span> | <span data-ttu-id="06acb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="06acb-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="06acb-117">Version</span><span class="sxs-lookup"><span data-stu-id="06acb-117">Version</span></span><br/> | <span data-ttu-id="06acb-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="06acb-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06acb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06acb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06acb-120">**Slider (élément)**</span><span class="sxs-lookup"><span data-stu-id="06acb-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="06acb-121">**Slider. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="06acb-121">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="06acb-122">**Slider. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="06acb-122">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="06acb-123">**Slider. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="06acb-123">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="06acb-124">**Slider. en mosaïque**</span><span class="sxs-lookup"><span data-stu-id="06acb-124">**SLIDER.tiled**</span></span>](slider-tiled.md)
</dt> </dl>

 

 





