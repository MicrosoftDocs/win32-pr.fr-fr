---
description: AM_RATE_ResetOnTimeDisc propriété-s’applique à Windows Vista et versions ultérieures.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c42b8e9d158f644d9e630555d96bf4d06e4ea9ef3cddced67742c057d0ab3859
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079519"
---
# <a name="am_rate_resetontimedisc-property"></a>\_ \_ Propriété RESETONTIMEDISC rate AM

s’applique à Windows Vista et versions ultérieures.

Cette propriété interroge si le décodeur resynchronise les horodatages de sortie aux horodatages d’entrée lorsque le décodeur reçoit un exemple avec l’indicateur de discontinuité.

Cette propriété est en lecture/écriture.



| Étiquette | Valeur |
|-------------------|-------------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ TSRateChange |
| ID de propriété       | \_Taux am \_ ResetOnTimeDisc     |
| Type de données         | **DWORD**                     |



 

## <a name="remarks"></a>Remarques

Cette propriété prend en charge les changements de taux d’accélération. Si la valeur de cette propriété est **true** et que le décodeur reçoit un exemple d’entrée avec l' \_ indicateur AM Sample \_ TIMEDISCONTINUITY, la trame décodée doit avoir le même horodatage que le frame d’entrée.

Pour récupérer l' \_ \_ indicateur TIMEDISCONTINUITY AM, appelez [**IMediaSample2 :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) sur l’exemple. L’indicateur est défini dans le membre **dwSampleFlags** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

pour plus d’informations, consultez [améliorations de la lecture de DVD dans Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Définition de la propriété change rate**](rate-change-property-set.md)
</dt> </dl>

 

 




