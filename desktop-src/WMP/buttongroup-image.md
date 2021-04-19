---
title: BUTTONGROUP. image
description: L’attribut image spécifie ou récupère le nom de l’image représentant les boutons d’un BUTTONGROUP.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- Lecteur Windows Media BUTTONGROUP. image
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545637"
---
# <a name="buttongroupimage"></a><span data-ttu-id="2b825-104">BUTTONGROUP. image</span><span class="sxs-lookup"><span data-stu-id="2b825-104">BUTTONGROUP.image</span></span>

<span data-ttu-id="2b825-105">L’attribut **image** spécifie ou récupère le nom de l’image représentant les boutons d’un **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="2b825-105">The **image** attribute specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="2b825-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="2b825-106">Possible Values</span></span>

<span data-ttu-id="2b825-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2b825-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b825-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2b825-108">Remarks</span></span>

<span data-ttu-id="2b825-109">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.</span><span class="sxs-lookup"><span data-stu-id="2b825-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="2b825-110">Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .</span><span class="sxs-lookup"><span data-stu-id="2b825-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="2b825-111">Si l’image du contrôle est plus grande que la région définie, l’image est rognée.</span><span class="sxs-lookup"><span data-stu-id="2b825-111">If the image of the control is larger than the defined region, the image will be cropped.</span></span>

<span data-ttu-id="2b825-112">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2b825-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b825-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b825-113">Requirements</span></span>



| <span data-ttu-id="2b825-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b825-114">Requirement</span></span> | <span data-ttu-id="2b825-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b825-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2b825-116">Version</span><span class="sxs-lookup"><span data-stu-id="2b825-116">Version</span></span><br/> | <span data-ttu-id="2b825-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="2b825-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b825-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b825-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b825-119">**Élément BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="2b825-119">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="2b825-120">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="2b825-120">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="2b825-121">**BUTTONGROUP. saturation**</span><span class="sxs-lookup"><span data-stu-id="2b825-121">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





