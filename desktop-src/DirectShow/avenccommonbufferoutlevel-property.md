---
description: Spécifie le niveau final de la mémoire tampon d’encodage, en bits, à la fin du processus d’encodage. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Propriété AVEncCommonBufferOutLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111982"
---
# <a name="avenccommonbufferoutlevel-property"></a>Propriété AVEncCommonBufferOutLevel

Spécifie le niveau final de la mémoire tampon d’encodage, en bits, à la fin du processus d’encodage. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonBufferOutLevel**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété a une plage de valeurs linéaire. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Notes

La propriété est disponible uniquement si la durée d’encodage est définie à l’avance, à l’aide de la propriété [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) ou de la propriété [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) .

Pour la vidéo MPEG, cette propriété définit le remplissage du vérificateur de mémoire tampon vidéo (VBV) à la fin du processus d’encodage. Il prend en charge la concaténation de flux pendant l’encodage.

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

 

 




