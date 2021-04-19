---
title: EQUALIZERSETTINGS. Speaker
description: L’attribut Speaker spécifie ou récupère le numéro d’index de la taille actuelle de l’intervenant.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS. Speakers Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532839"
---
# <a name="equalizersettingsspeakersize"></a>EQUALIZERSETTINGS. Speaker

L’attribut **Speaker** spécifie ou récupère le numéro d’index de la taille actuelle de l’intervenant.

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (long) contenant l’une des valeurs suivantes.



| Valeur | Description                              |
|-------|------------------------------------------|
| 0     | Les haut-parleurs actuels sont des casques.     |
| 1     | Les haut-parleurs actuels sont de taille normale. |
| 2     | Les haut-parleurs actuels sont volumineux.          |



 

## <a name="remarks"></a>Notes

Le nom convivial de la taille de l’orateur peut être récupéré à l’aide de l’attribut **currentSpeakerName** .

Cet attribut est ignoré si **enhancedAudio** est défini sur false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.currentSpeakerName**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





