---
title: PLAYLIST. hueShift
description: L’attribut hueShift spécifie ou récupère la quantité de décalage de la teinte des images de la liste déroulante.
ms.assetid: 9d4d8b73-527e-43f3-a921-0576b8897918
keywords:
- Lecteur Windows Media PLAYLIST. hueShift
topic_type:
- apiref
api_name:
- PLAYLIST.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e9dbe89989ddd8f02d67ac8f14532b9b1fbf15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545900"
---
# <a name="playlisthueshift"></a><span data-ttu-id="4bce6-104">PLAYLIST. hueShift</span><span class="sxs-lookup"><span data-stu-id="4bce6-104">PLAYLIST.hueShift</span></span>

<span data-ttu-id="4bce6-105">L’attribut **hueShift** spécifie ou récupère la quantité de décalage de la teinte des images de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="4bce6-105">The **hueShift** attribute specifies or retrieves the amount by which the hue of the drop-down images is shifted.</span></span>

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a><span data-ttu-id="4bce6-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="4bce6-106">Possible Values</span></span>

<span data-ttu-id="4bce6-107">Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est comprise entre 0,0 et 360,0, avec une valeur par défaut de 0,0.</span><span class="sxs-lookup"><span data-stu-id="4bce6-107">This attribute is a read/write **Number** (**float**) with a value ranging from 0.0 to 360.0 with a default value of 0.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bce6-108">Notes</span><span class="sxs-lookup"><span data-stu-id="4bce6-108">Remarks</span></span>

<span data-ttu-id="4bce6-109">Cet attribut modifie la valeur de teinte des images spécifiées par les attributs **dropDownBackgroundImage** et **dropDownImage** si elles ont été spécifiées et s’ils font référence à des images BMP 8 bits.</span><span class="sxs-lookup"><span data-stu-id="4bce6-109">This attribute changes the hue value of the images specified by the **dropDownBackgroundImage** and **dropDownImage** attributes if they have been specified and they refer to 8-bit BMP images.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bce6-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bce6-110">Requirements</span></span>



| <span data-ttu-id="4bce6-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bce6-111">Requirement</span></span> | <span data-ttu-id="4bce6-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bce6-112">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="4bce6-113">Version</span><span class="sxs-lookup"><span data-stu-id="4bce6-113">Version</span></span><br/> | <span data-ttu-id="4bce6-114">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4bce6-114">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bce6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bce6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bce6-116">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="4bce6-116">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="4bce6-117">**PLAYLIST. dropDownBackgroundImage**</span><span class="sxs-lookup"><span data-stu-id="4bce6-117">**PLAYLIST.dropDownBackgroundImage**</span></span>](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[<span data-ttu-id="4bce6-118">**PLAYLIST. dropDownImage**</span><span class="sxs-lookup"><span data-stu-id="4bce6-118">**PLAYLIST.dropDownImage**</span></span>](playlist-dropdownimage.md)
</dt> <dt>

[<span data-ttu-id="4bce6-119">**PLAYLIST. saturation**</span><span class="sxs-lookup"><span data-stu-id="4bce6-119">**PLAYLIST.saturation**</span></span>](playlist-saturation.md)
</dt> </dl>

 

 





