---
title: Slider. thumbDownImage
description: L’attribut thumbDownImage spécifie ou récupère l’image représentant l’état inactif du curseur de défilement.
ms.assetid: 6e7c694a-b651-4327-9550-8e05d0c42f02
keywords:
- Slider. thumbDownImage lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.thumbDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f35638edee2b84231d76917a0710ae6d691a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537593"
---
# <a name="sliderthumbdownimage"></a>Slider. thumbDownImage

L’attribut **thumbDownImage** spécifie ou récupère l’image représentant l’état inactif du curseur de défilement.

``` syntax
        elementID.thumbDownImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Notes

**ThumbDownImage** est facultatif et est l’image utilisée pour représenter l’état inactif du **thumbImage**. Si aucun **thumbDownImage** n’est fourni, le curseur utilise **thumbImage**.

Les formats pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. thumbImage**](slider-thumbimage.md)
</dt> </dl>

 

 





