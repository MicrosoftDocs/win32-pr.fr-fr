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
# <a name="playlisthueshift"></a>PLAYLIST. hueShift

L’attribut **hueShift** spécifie ou récupère la quantité de décalage de la teinte des images de la liste déroulante.

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est comprise entre 0,0 et 360,0, avec une valeur par défaut de 0,0.

## <a name="remarks"></a>Notes

Cet attribut modifie la valeur de teinte des images spécifiées par les attributs **dropDownBackgroundImage** et **dropDownImage** si elles ont été spécifiées et s’ils font référence à des images BMP 8 bits.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**PLAYLIST. dropDownImage**](playlist-dropdownimage.md)
</dt> <dt>

[**PLAYLIST. saturation**](playlist-saturation.md)
</dt> </dl>

 

 





