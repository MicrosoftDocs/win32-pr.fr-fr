---
description: Spécifie comment le décodeur reproduit un double audio mono.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Propriété AVDecAudioDualMonoReproMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9151ed6b996ec4ab92791221b7fb4c920913c818eac4a079ee6f40d04591a9db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917059"
---
# <a name="avdecaudiodualmonorepromode-property"></a>Propriété AVDecAudioDualMonoReproMode

Spécifie comment le décodeur reproduit un double audio mono.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecAudioDualMonoReproMode**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) .

## <a name="remarks"></a>Remarques

Cette propriété s’applique uniquement lorsque le flux de bits d’entrée du décodeur contient du son double mono. Pour tester cette condition, récupérez la valeur de la propriété [AVDecAudioDualMono](avdecaudiodualmono-property.md) .

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

 

 




