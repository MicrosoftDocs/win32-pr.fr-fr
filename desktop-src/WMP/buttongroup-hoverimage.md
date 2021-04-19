---
title: BUTTONGROUP. hoverImage
description: L’attribut hoverImage spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le BUTTONGROUP. L’état de survol se produit lorsque le bouton est à l’État haut et que l’utilisateur pointe dessus avec la souris.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- Lecteur Windows Media BUTTONGROUP. hoverImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537313"
---
# <a name="buttongrouphoverimage"></a><span data-ttu-id="85824-105">BUTTONGROUP. hoverImage</span><span class="sxs-lookup"><span data-stu-id="85824-105">BUTTONGROUP.hoverImage</span></span>

<span data-ttu-id="85824-106">L’attribut **hoverImage** spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="85824-106">The **hoverImage** attribute specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="85824-107">L’état de survol se produit lorsque le bouton est à l’État haut et que l’utilisateur pointe dessus avec la souris.</span><span class="sxs-lookup"><span data-stu-id="85824-107">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="85824-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="85824-108">Possible Values</span></span>

<span data-ttu-id="85824-109">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="85824-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="85824-110">Notes</span><span class="sxs-lookup"><span data-stu-id="85824-110">Remarks</span></span>

<span data-ttu-id="85824-111">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.</span><span class="sxs-lookup"><span data-stu-id="85824-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="85824-112">Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .</span><span class="sxs-lookup"><span data-stu-id="85824-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="85824-113">L’image par défaut est celle spécifiée dans l’attribut **image** ou sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="85824-113">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="85824-114">Si l’image de survol est plus grande que la région définie, l’image de survol est rognée.</span><span class="sxs-lookup"><span data-stu-id="85824-114">If the hover image is larger than the defined region, the hover image will be cropped.</span></span>

<span data-ttu-id="85824-115">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="85824-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="85824-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="85824-116">Examples</span></span>

<span data-ttu-id="85824-117">Consultez *BUTTONELEMENT*. attribut [mappingColor](buttonelement-mappingcolor.md) pour un exemple illustrant l’utilisation de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="85824-117">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="85824-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85824-118">Requirements</span></span>



| <span data-ttu-id="85824-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85824-119">Requirement</span></span> | <span data-ttu-id="85824-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="85824-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="85824-121">Version</span><span class="sxs-lookup"><span data-stu-id="85824-121">Version</span></span><br/> | <span data-ttu-id="85824-122">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="85824-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85824-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85824-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85824-124">**Élément BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="85824-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="85824-125">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="85824-125">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="85824-126">**BUTTONGROUP. image**</span><span class="sxs-lookup"><span data-stu-id="85824-126">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="85824-127">**BUTTONGROUP. saturation**</span><span class="sxs-lookup"><span data-stu-id="85824-127">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





