---
description: Retourne le niveau de volume le plus élevé qui était présent dans le contenu audio.
ms.assetid: 1d9a6a22-bb82-45e1-80d2-88627c90340c
title: Propriété AVEncStatAudioPeakPCMValue (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330f3eea62ce5f0232504786c63e87c233bd802f6d06fad6306f476f9d6b5361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999839"
---
# <a name="avencstataudiopeakpcmvalue-property"></a>Propriété AVEncStatAudioPeakPCMValue

Retourne le niveau de volume le plus élevé qui était présent dans le contenu audio.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncStatAudioPeakPCMValue**

## <a name="remarks"></a>Remarques

Cette propriété est disponible une fois l’encodage terminé.

Cette propriété s’applique uniquement à l’encodage VBR (Quality-based bit rate).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




