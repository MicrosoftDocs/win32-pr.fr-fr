---
title: VIEW. backgroundImage
description: L’attribut backgroundImage spécifie ou récupère l’image d’arrière-plan de la vue ou de la sous-vue.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- VIEW. backgroundImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1de8bcbd0eb47f03aaff46b4292a8afe226ca8a221ec570537351af8e509801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761739"
---
# <a name="viewbackgroundimage"></a>VIEW. backgroundImage

L’attribut **BackgroundImage** spécifie ou récupère l’image d’arrière-plan de la **vue** ou de la sous- **vue**.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Les formats pris en charge sont BMP, JPG, GIF et PNG. Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **backgroundImageHueShift** et **backgroundImageSaturation** .

dans un package Windows Media Download, si vous spécifiez l’attribut **backgroundImage** pour un élément **VIEW** , vous devez également spécifier l’attribut **backgroundColor** pour cet élément.

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

 

 





