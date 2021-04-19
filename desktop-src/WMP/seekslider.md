---
title: SEEKSLIDER
description: Il s’agit d’un curseur prédéfini avec les valeurs par défaut suivantes. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- Lecteur Windows Media SEEKSLIDER
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528783"
---
# <a name="seekslider"></a>SEEKSLIDER

Il s’agit d’un **curseur** prédéfini avec les valeurs par défaut suivantes.

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a>Notes

Cela crée un contrôle **Slider** qui recherche le fichier multimédia à n’importe quelle position. Les info-bulles sont localisées. Toutes les propriétés de ce **curseur** peuvent être remplacées en les spécifiant explicitement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------|
| Version<br/> | Lecteur Windows Media 7,0 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> </dl>

 

 





