---
description: 'Propriété AVDecAudioDualMono : spécifie si l’audio à 2 canaux est encodé en stéréo ou double mono.'
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Propriété AVDecAudioDualMono (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112109"
---
# <a name="avdecaudiodualmono-property"></a>Propriété AVDecAudioDualMono

Spécifie si le contenu audio à 2 canaux est encodé en stéréo ou en double mono.

Cette propriété est en lecture seule.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecAudioDualMono**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) .

## <a name="remarks"></a>Notes

Cette propriété s’applique uniquement lorsque le flux de bits d’entrée du décodeur contient du son de deux canaux. Un flux audio à deux canaux peut être encodé en stéréo ou en double mono. Si le son est double mono, vous pouvez définir la propriété [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) pour configurer la façon dont le décodeur reproduit l’audio.

## <a name="requirements"></a>Spécifications



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

 

 




