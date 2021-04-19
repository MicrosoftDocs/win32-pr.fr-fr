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
# <a name="viewbackgroundimage"></a>VIEW. backgroundImage

L’attribut **BackgroundImage** spécifie ou récupère l’image d’arrière-plan de la **vue** ou de la sous- **vue**.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Les formats pris en charge sont BMP, JPG, GIF et PNG. Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **backgroundImageHueShift** et **backgroundImageSaturation** .

Dans un package de téléchargement Windows Media, si vous spécifiez l’attribut **BackgroundImage** pour un élément **View** , vous devez également spécifier l’attribut **backgroundColor** pour cet élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIEW**](view-element.md)
</dt> <dt>

[**VUE. backgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**VUE. backgroundImageSaturation**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





