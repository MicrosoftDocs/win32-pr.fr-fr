---
title: VIEW. backgroundImage
description: L’attribut backgroundImage spécifie ou récupère l’image d’arrière-plan de la vue ou de la sous-vue.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- AFFICHER. backgroundImage lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523929"
---
# <a name="viewbackgroundimage"></a><span data-ttu-id="60cf1-104">VIEW. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="60cf1-104">VIEW.backgroundImage</span></span>

<span data-ttu-id="60cf1-105">L’attribut **BackgroundImage** spécifie ou récupère l’image d’arrière-plan de la **vue** ou de la sous- **vue**.</span><span class="sxs-lookup"><span data-stu-id="60cf1-105">The **backgroundImage** attribute specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="60cf1-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="60cf1-106">Possible Values</span></span>

<span data-ttu-id="60cf1-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="60cf1-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="60cf1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="60cf1-108">Remarks</span></span>

<span data-ttu-id="60cf1-109">Les formats pris en charge sont BMP, JPG, GIF et PNG.</span><span class="sxs-lookup"><span data-stu-id="60cf1-109">The supported formats are BMP, JPG, GIF, and PNG.</span></span> <span data-ttu-id="60cf1-110">Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **backgroundImageHueShift** et **backgroundImageSaturation** .</span><span class="sxs-lookup"><span data-stu-id="60cf1-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **backgroundImageHueShift** and **backgroundImageSaturation** attributes.</span></span>

<span data-ttu-id="60cf1-111">Dans un package de téléchargement Windows Media, si vous spécifiez l’attribut **BackgroundImage** pour un élément **View** , vous devez également spécifier l’attribut **backgroundColor** pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="60cf1-111">In a Windows Media Download package, if you specify the **backgroundImage** attribute for a **VIEW** element, then you must also specify the **backgroundColor** attribute for that element.</span></span>

## <a name="requirements"></a><span data-ttu-id="60cf1-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60cf1-112">Requirements</span></span>



| <span data-ttu-id="60cf1-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60cf1-113">Requirement</span></span> | <span data-ttu-id="60cf1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="60cf1-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="60cf1-115">Version</span><span class="sxs-lookup"><span data-stu-id="60cf1-115">Version</span></span><br/> | <span data-ttu-id="60cf1-116">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="60cf1-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60cf1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60cf1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60cf1-118">**Élément VIEW**</span><span class="sxs-lookup"><span data-stu-id="60cf1-118">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="60cf1-119">**VUE. backgroundImageHueShift**</span><span class="sxs-lookup"><span data-stu-id="60cf1-119">**VIEW.backgroundImageHueShift**</span></span>](view-backgroundimagehueshift.md)
</dt> <dt>

[<span data-ttu-id="60cf1-120">**VUE. backgroundImageSaturation**</span><span class="sxs-lookup"><span data-stu-id="60cf1-120">**VIEW.backgroundImageSaturation**</span></span>](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





