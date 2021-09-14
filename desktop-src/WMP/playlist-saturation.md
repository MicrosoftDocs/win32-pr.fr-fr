---
title: PLAYLIST. saturation
description: L’attribut saturation spécifie ou récupère la valeur de saturation des images de la liste déroulante.
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- PLAYLIST. saturation Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eb53afeafb0754f0e754f68fd5ff785eaade8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292971"
---
# <a name="playlistsaturation"></a>PLAYLIST. saturation

L’attribut **saturation** spécifie ou récupère la valeur de saturation des images de la liste déroulante.

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est comprise entre 0,0 et 2,0, avec une valeur par défaut de 1,0.

## <a name="remarks"></a>Notes

Cet attribut modifie la valeur de saturation des images spécifiées par les attributs **dropDownBackgroundImage** et **dropDownImage** si elles ont été spécifiées et s’ils font référence à des images BMP 8 bits.

## <a name="requirements"></a>Spécifications



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

[**PLAYLIST. hueShift**](playlist-hueshift.md)
</dt> </dl>

 

 





