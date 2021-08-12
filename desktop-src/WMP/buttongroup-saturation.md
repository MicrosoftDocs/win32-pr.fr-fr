---
title: BUTTONGROUP. saturation
description: L’attribut saturation spécifie ou récupère la valeur de saturation des images BUTTONGROUP.
ms.assetid: bfd957f0-8201-4a4f-9162-a397ed97c747
keywords:
- BUTTONGROUP. saturation Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d3579ac8109cb56e56c78a07a8f53e4cd7c017a695b6018f6a2ad41f703035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581301"
---
# <a name="buttongroupsaturation"></a>BUTTONGROUP. saturation

L’attribut **saturation** spécifie ou récupère la valeur de saturation des images **BUTTONGROUP** .

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est comprise entre 0,0 et 2,0, avec une valeur par défaut de 1,0.

## <a name="remarks"></a>Notes

Cet attribut modifie la valeur de saturation des images spécifiées par les attributs **disabledImage**, **downImage**, **hoverDownImage**, **hoverImage** et **image** s’ils ont été spécifiés et s’ils font référence à des images BMP 8 bits.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. disabledImage**](buttongroup-disabledimage.md)
</dt> <dt>

[**BUTTONGROUP. downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP. hoverDownImage**](buttongroup-hoverdownimage.md)
</dt> <dt>

[**BUTTONGROUP. hoverImage**](buttongroup-hoverimage.md)
</dt> <dt>

[**BUTTONGROUP. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. image**](buttongroup-image.md)
</dt> </dl>

 

 





