---
title: PLAYLIST. backgroundImage
description: L’attribut backgroundImage spécifie ou récupère l’image d’arrière-plan.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- PLAYLIST. backgroundImage lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545543"
---
# <a name="playlistbackgroundimage"></a>PLAYLIST. backgroundImage

L’attribut **BackgroundImage** spécifie ou récupère l’image d’arrière-plan.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image. Il n'a aucune valeur par défaut.

## <a name="remarks"></a>Notes

Si la hauteur et la largeur de l’image sont inférieures à la hauteur et à la largeur de l’élément de **sélection** , l’image est affichée en mosaïque. Les formats pris en charge sont BMP, JPG, GIF et PNG.

Si vous spécifiez la valeur « gradient » pour l’image d’arrière-plan, l’arrière-plan de la sélection s’affiche sous la forme d’un dégradé de couleur. Cela signifie que la couleur d’arrière-plan transite graduellement entre les valeurs [playlist. BackgroundColor](playlist-backgroundcolor.md) (en haut de l’arrière-plan) et [playlist. statusColor](playlist-statuscolor.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure, lecteur Windows Media 10 pour la fonctionnalité de dégradé<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





