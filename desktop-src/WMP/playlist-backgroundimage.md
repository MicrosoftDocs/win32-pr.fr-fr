---
title: PLAYLIST. backgroundImage
description: L’attribut backgroundImage spécifie ou récupère l’image d’arrière-plan.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- PLAYLIST. backgroundImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ddcb42f118a5a672b6678079825b6cb3d6aba5fbdc54953fb566e4222f583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054247"
---
# <a name="playlistbackgroundimage"></a>PLAYLIST. backgroundImage

L’attribut **BackgroundImage** spécifie ou récupère l’image d’arrière-plan.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image. Il n'a aucune valeur par défaut.

## <a name="remarks"></a>Remarques

Si la hauteur et la largeur de l’image sont inférieures à la hauteur et à la largeur de l’élément de **sélection** , l’image est affichée en mosaïque. Les formats pris en charge sont BMP, JPG, GIF et PNG.

Si vous spécifiez la valeur « gradient » pour l’image d’arrière-plan, l’arrière-plan de la sélection s’affiche sous la forme d’un dégradé de couleur. Cela signifie que la couleur d’arrière-plan transite graduellement entre les valeurs [playlist. BackgroundColor](playlist-backgroundcolor.md) (en haut de l’arrière-plan) et [playlist. statusColor](playlist-statuscolor.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media la version 7,0 ou ultérieure, Lecteur Windows Media 10 pour la fonctionnalité de dégradé<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





