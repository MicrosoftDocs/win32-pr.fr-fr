---
title: EQUALIZERSETTINGS. Speaker
description: L’attribut Speaker spécifie ou récupère le numéro d’index de la taille actuelle de l’intervenant.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS. speakers Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d289a89a22e8c10cf669e9b55fc304826acb3ce0f72468f725e7d5fae0dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748647"
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



 

## <a name="remarks"></a>Remarques

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

 

 





