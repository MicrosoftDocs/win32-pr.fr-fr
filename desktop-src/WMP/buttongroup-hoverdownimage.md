---
title: BUTTONGROUP. hoverDownImage
description: L’attribut hoverDownImage spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le BUTTONGROUP. L’état Survol se produit lorsque le bouton est à l’état inactif et que l’utilisateur pointe dessus avec la souris.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- Lecteur Windows Media BUTTONGROUP. hoverDownImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532706"
---
# <a name="buttongrouphoverdownimage"></a><span data-ttu-id="b27db-105">BUTTONGROUP. hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="b27db-105">BUTTONGROUP.hoverDownImage</span></span>

<span data-ttu-id="b27db-106">L’attribut **hoverDownImage** spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="b27db-106">The **hoverDownImage** attribute specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="b27db-107">L’état Survol se produit lorsque le bouton est à l’état inactif et que l’utilisateur pointe dessus avec la souris.</span><span class="sxs-lookup"><span data-stu-id="b27db-107">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="b27db-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b27db-108">Possible Values</span></span>

<span data-ttu-id="b27db-109">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b27db-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b27db-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b27db-110">Remarks</span></span>

<span data-ttu-id="b27db-111">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.</span><span class="sxs-lookup"><span data-stu-id="b27db-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="b27db-112">Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .</span><span class="sxs-lookup"><span data-stu-id="b27db-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="b27db-113">L’image par défaut est celle spécifiée dans l’attribut **downImage** ou sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b27db-113">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="b27db-114">Si l’image de survol est plus grande que la région définie, l’image de survol est rognée.</span><span class="sxs-lookup"><span data-stu-id="b27db-114">If the hover-down image is larger than the defined region, the hover-down image will be cropped.</span></span>

<span data-ttu-id="b27db-115">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b27db-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b27db-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b27db-116">Requirements</span></span>



| <span data-ttu-id="b27db-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b27db-117">Requirement</span></span> | <span data-ttu-id="b27db-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b27db-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b27db-119">Version</span><span class="sxs-lookup"><span data-stu-id="b27db-119">Version</span></span><br/> | <span data-ttu-id="b27db-120">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="b27db-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b27db-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b27db-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27db-122">**Élément BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="b27db-122">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="b27db-123">**BUTTONGROUP. downImage**</span><span class="sxs-lookup"><span data-stu-id="b27db-123">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> <dt>

[<span data-ttu-id="b27db-124">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="b27db-124">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="b27db-125">**BUTTONGROUP. saturation**</span><span class="sxs-lookup"><span data-stu-id="b27db-125">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





