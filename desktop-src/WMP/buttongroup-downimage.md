---
title: BUTTONGROUP. downImage
description: L’attribut downImage spécifie ou récupère le nom de l’image représentant l’état inactif du BUTTONGROUP.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- Lecteur Windows Media BUTTONGROUP. downImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528722"
---
# <a name="buttongroupdownimage"></a><span data-ttu-id="1f274-104">BUTTONGROUP. downImage</span><span class="sxs-lookup"><span data-stu-id="1f274-104">BUTTONGROUP.downImage</span></span>

<span data-ttu-id="1f274-105">L’attribut **downImage** spécifie ou récupère le nom de l’image représentant l’état inactif du **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="1f274-105">The **downImage** attribute specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="1f274-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="1f274-106">Possible Values</span></span>

<span data-ttu-id="1f274-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1f274-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f274-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1f274-108">Remarks</span></span>

<span data-ttu-id="1f274-109">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.</span><span class="sxs-lookup"><span data-stu-id="1f274-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="1f274-110">Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .</span><span class="sxs-lookup"><span data-stu-id="1f274-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="1f274-111">L’image par défaut est celle spécifiée dans l’attribut **image** .</span><span class="sxs-lookup"><span data-stu-id="1f274-111">The default image is the one specified in the **image** attribute.</span></span>

<span data-ttu-id="1f274-112">Si l’image inférieure est plus grande que la région définie, l’image descendante est rognée.</span><span class="sxs-lookup"><span data-stu-id="1f274-112">If the down image is larger than the defined region, the down image will be cropped.</span></span>

<span data-ttu-id="1f274-113">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1f274-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f274-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f274-114">Requirements</span></span>



| <span data-ttu-id="1f274-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f274-115">Requirement</span></span> | <span data-ttu-id="1f274-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f274-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1f274-117">Version</span><span class="sxs-lookup"><span data-stu-id="1f274-117">Version</span></span><br/> | <span data-ttu-id="1f274-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="1f274-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f274-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f274-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f274-120">**Élément BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="1f274-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="1f274-121">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="1f274-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="1f274-122">**BUTTONGROUP. image**</span><span class="sxs-lookup"><span data-stu-id="1f274-122">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="1f274-123">**BUTTONGROUP. saturation**</span><span class="sxs-lookup"><span data-stu-id="1f274-123">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





