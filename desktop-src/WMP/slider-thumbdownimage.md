---
title: Slider. thumbDownImage
description: L’attribut thumbDownImage spécifie ou récupère l’image représentant l’état inactif du curseur de défilement.
ms.assetid: 6e7c694a-b651-4327-9550-8e05d0c42f02
keywords:
- slider. thumbDownImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.thumbDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1e4c9944d8d352f8ffb1bf2f54fe8d6edfc401421891d079f2ce7696e1bd19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832545"
---
# <a name="sliderthumbdownimage"></a>Slider. thumbDownImage

L’attribut **thumbDownImage** spécifie ou récupère l’image représentant l’état inactif du curseur de défilement.

``` syntax
        elementID.thumbDownImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Remarques

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

 

 





