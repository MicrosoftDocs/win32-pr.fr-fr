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
ms.openlocfilehash: ebc2e6ec82327be9cb423d05661a5a38bbcc445450fc6d4f56ceaf7caa8b270d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054007"
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

## <a name="remarks"></a>Remarques

Cela crée un contrôle Slider qui définit le volume audio. Les info-bulles sont localisées. Toutes les propriétés de ce curseur peuvent être remplacées en les spécifiant explicitement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------|
| Version<br/> | Lecteur Windows Media 7,0 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> </dl>

 

 





