---
title: VOLUMESLIDER
description: Il s’agit d’un curseur prédéfini avec les valeurs par défaut suivantes. | VOLUMESLIDER
ms.assetid: 7533863b-49de-4c1b-8750-fd333c573a17
keywords:
- VOLUMESLIDER Lecteur Windows Media
topic_type:
- apiref
api_name:
- VOLUMESLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea872b55f6657d9cf1c9f67230cb3debd955fb4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292879"
---
# <a name="volumeslider"></a>VOLUMESLIDER

Il s’agit d’un curseur prédéfini avec les valeurs par défaut suivantes.

``` syntax
toolTip="Volume"
max="100"
min="0"
value="wmpprop:player.settings.volume"
value_onchange="jscript:player.settings.volume=value;
player.settings.mute=false;"
```

## <a name="remarks"></a>Notes

Cela crée un contrôle Slider qui définit le volume audio. Les info-bulles sont localisées. Toutes les propriétés de ce curseur peuvent être remplacées en les spécifiant explicitement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------|
| Version<br/> | Lecteur Windows Media 7,0 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> </dl>

 

 





