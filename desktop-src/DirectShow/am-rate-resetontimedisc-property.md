---
description: S’applique à Windows Vista et versions ultérieures.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d465329c2c8de1a66f04a830d183b8cba88c0728
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910247"
---
# <a name="am_rate_resetontimedisc-property"></a>\_ \_ Propriété RESETONTIMEDISC rate AM

S’applique à Windows Vista et versions ultérieures.

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

Pour plus d’informations, consultez [améliorations de la lecture de DVD dans Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Définition de la propriété change rate**](rate-change-property-set.md)
</dt> </dl>

 

 




