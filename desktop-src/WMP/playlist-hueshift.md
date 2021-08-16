---
title: PLAYLIST. hueShift
description: L’attribut hueShift spécifie ou récupère la quantité de décalage de la teinte des images de la liste déroulante.
ms.assetid: 9d4d8b73-527e-43f3-a921-0576b8897918
keywords:
- PLAYLIST. hueShift Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a615549c25b57ed9693843a09433200f73c8e4ffad131c2a4e4057932c5e92b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747072"
---
# <a name="playlisthueshift"></a>PLAYLIST. hueShift

L’attribut **hueShift** spécifie ou récupère la quantité de décalage de la teinte des images de la liste déroulante.

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est comprise entre 0,0 et 360,0, avec une valeur par défaut de 0,0.

## <a name="remarks"></a>Remarques

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

 

 





