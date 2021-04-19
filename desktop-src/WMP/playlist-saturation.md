---
title: PLAYLIST. saturation
description: L’attribut saturation spécifie ou récupère la valeur de saturation des images de la liste déroulante.
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- PLAYLIST. saturation du lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eb53afeafb0754f0e754f68fd5ff785eaade8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520863"
---
# <a name="playlistsaturation"></a><span data-ttu-id="bf9bc-104">PLAYLIST. saturation</span><span class="sxs-lookup"><span data-stu-id="bf9bc-104">PLAYLIST.saturation</span></span>

<span data-ttu-id="bf9bc-105">L’attribut **saturation** spécifie ou récupère la valeur de saturation des images de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="bf9bc-105">The **saturation** attribute specifies or retrieves the saturation value of the drop-down images.</span></span>

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a><span data-ttu-id="bf9bc-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="bf9bc-106">Possible Values</span></span>

<span data-ttu-id="bf9bc-107">Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est comprise entre 0,0 et 2,0, avec une valeur par défaut de 1,0.</span><span class="sxs-lookup"><span data-stu-id="bf9bc-107">This attribute is a read/write **Number** (**float**) with a value ranging from 0.0 to 2.0 with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf9bc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="bf9bc-108">Remarks</span></span>

<span data-ttu-id="bf9bc-109">Cet attribut modifie la valeur de saturation des images spécifiées par les attributs **dropDownBackgroundImage** et **dropDownImage** si elles ont été spécifiées et s’ils font référence à des images BMP 8 bits.</span><span class="sxs-lookup"><span data-stu-id="bf9bc-109">This attribute changes the saturation value of the images specified by the **dropDownBackgroundImage** and **dropDownImage** attributes if they have been specified and they refer to 8-bit BMP images.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf9bc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf9bc-110">Requirements</span></span>



| <span data-ttu-id="bf9bc-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf9bc-111">Requirement</span></span> | <span data-ttu-id="bf9bc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf9bc-112">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="bf9bc-113">Version</span><span class="sxs-lookup"><span data-stu-id="bf9bc-113">Version</span></span><br/> | <span data-ttu-id="bf9bc-114">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bf9bc-114">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf9bc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf9bc-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf9bc-116">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="bf9bc-116">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="bf9bc-117">**PLAYLIST. dropDownBackgroundImage**</span><span class="sxs-lookup"><span data-stu-id="bf9bc-117">**PLAYLIST.dropDownBackgroundImage**</span></span>](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[<span data-ttu-id="bf9bc-118">**PLAYLIST. dropDownImage**</span><span class="sxs-lookup"><span data-stu-id="bf9bc-118">**PLAYLIST.dropDownImage**</span></span>](playlist-dropdownimage.md)
</dt> <dt>

[<span data-ttu-id="bf9bc-119">**PLAYLIST. hueShift**</span><span class="sxs-lookup"><span data-stu-id="bf9bc-119">**PLAYLIST.hueShift**</span></span>](playlist-hueshift.md)
</dt> </dl>

 

 





