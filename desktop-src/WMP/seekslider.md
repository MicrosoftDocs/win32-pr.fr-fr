---
title: SEEKSLIDER
description: Il s’agit d’un curseur prédéfini avec les valeurs par défaut suivantes. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SEEKSLIDER Lecteur Windows Media
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a294eede05ec2b2f0f84e925aa299c9bcb2388ee2151385e48f2c68e6b4c1328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833338"
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

## <a name="remarks"></a>Remarques

Cela crée un contrôle **Slider** qui recherche le fichier multimédia à n’importe quelle position. Les info-bulles sont localisées. Toutes les propriétés de ce **curseur** peuvent être remplacées en les spécifiant explicitement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------|
| Version<br/> | Lecteur Windows Media 7,0 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> </dl>

 

 





