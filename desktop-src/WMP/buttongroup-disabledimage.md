---
title: BUTTONGROUP. disabledImage
description: L’attribut disabledImage spécifie ou récupère le nom de l’image représentant l’état désactivé des boutons dans le BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- Lecteur Windows Media BUTTONGROUP. disabledImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525968"
---
# <a name="buttongroupdisabledimage"></a><span data-ttu-id="c2f74-104">BUTTONGROUP. disabledImage</span><span class="sxs-lookup"><span data-stu-id="c2f74-104">BUTTONGROUP.disabledImage</span></span>

<span data-ttu-id="c2f74-105">L’attribut **disabledImage** spécifie ou récupère le nom de l’image représentant l’état désactivé des boutons dans le **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="c2f74-105">The **disabledImage** attribute specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="c2f74-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c2f74-106">Possible Values</span></span>

<span data-ttu-id="c2f74-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c2f74-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2f74-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c2f74-108">Remarks</span></span>

<span data-ttu-id="c2f74-109">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.</span><span class="sxs-lookup"><span data-stu-id="c2f74-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="c2f74-110">Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .</span><span class="sxs-lookup"><span data-stu-id="c2f74-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="c2f74-111">Lorsque l’attribut **Disabled** d’un élément **BUTTONELEMENT** a la valeur true, la région correspondante de **disabledImage** pour le **BUTTONGROUP** est affichée.</span><span class="sxs-lookup"><span data-stu-id="c2f74-111">When the **disabled** attribute of a **BUTTONELEMENT** element is set to true, the corresponding region of the **disabledImage** for the **BUTTONGROUP** is displayed.</span></span> <span data-ttu-id="c2f74-112">Si la taille de l’image désactivée est supérieure à celle de la région définie, l’image désactivée est rognée.</span><span class="sxs-lookup"><span data-stu-id="c2f74-112">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="c2f74-113">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c2f74-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2f74-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2f74-114">Requirements</span></span>



| <span data-ttu-id="c2f74-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2f74-115">Requirement</span></span> | <span data-ttu-id="c2f74-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2f74-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c2f74-117">Version</span><span class="sxs-lookup"><span data-stu-id="c2f74-117">Version</span></span><br/> | <span data-ttu-id="c2f74-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c2f74-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2f74-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2f74-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2f74-120">**Élément BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="c2f74-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="c2f74-121">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="c2f74-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="c2f74-122">**BUTTONGROUP. saturation**</span><span class="sxs-lookup"><span data-stu-id="c2f74-122">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





