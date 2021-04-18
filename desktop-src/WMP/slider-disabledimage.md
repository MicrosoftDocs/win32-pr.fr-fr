---
title: Slider. disabledImage
description: L’attribut disabledImage spécifie ou récupère l’image du curseur qui est utilisé lorsque le contrôle Slider est désactivé.
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- Slider. disabledImage lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1b90dcbd551ca0f8bb332f858eac0b69c46733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533000"
---
# <a name="sliderdisabledimage"></a>Slider. disabledImage

L’attribut **disabledImage** spécifie ou récupère l’image du curseur qui est utilisé lorsque le contrôle Slider est désactivé.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Notes

**DisabledImage** est facultatif. S’il n’est pas fourni, l' **BackgroundImage** est utilisé pour tous les États désactivés. Lorsqu’un contrôle Slider est désactivé, aucune image de premier plan n’est visible.

Les formats pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. backgroundImage**](slider-backgroundimage.md)
</dt> </dl>

 

 





