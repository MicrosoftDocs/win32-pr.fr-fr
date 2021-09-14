---
title: BUTTONGROUP. hueShift
description: L’attribut hueShift spécifie ou récupère la valeur de décalage de la teinte des images BUTTONGROUP.
ms.assetid: 156256ef-ec24-40c4-ad23-064e38c79e69
keywords:
- BUTTONGROUP. hueShift Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf77faea27ecc5adee6525c4ee8d8ff1541aac4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126852700"
---
# <a name="buttongrouphueshift"></a>BUTTONGROUP. hueShift

L’attribut **hueShift** spécifie ou récupère la valeur de décalage de la teinte des images **BUTTONGROUP** .

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est comprise entre 0,0 et 360,0, avec une valeur par défaut de 0,0.

## <a name="remarks"></a>Notes

Cet attribut modifie la valeur de teinte des images spécifiées par les attributs **disabledImage**, **downImage**, **hoverDownImage**, **hoverImage** et **image** s’ils ont été spécifiés et s’ils font référence à des images BMP 8 bits.

## <a name="requirements"></a>Spécifications



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

[**BUTTONGROUP. image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





