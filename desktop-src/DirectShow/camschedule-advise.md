---
description: La méthode Advise répartit toutes les demandes planifiées pour une heure spécifiée ou antérieure.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: CAMSchedule. Advise, méthode (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094997"
---
# <a name="camscheduleadvise-method"></a>CAMSchedule. Advise, méthode

La `Advise` méthode distribue toutes les demandes planifiées pour une heure spécifiée ou antérieure.

## <a name="syntax"></a>Syntaxe


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rtTime* \[ Réf\]
</dt> <dd>

Valeur qui spécifie le temps de référence actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le temps de référence de la prochaine demande de notification planifiée, ou le \_ temps maximal s’il n’y en a aucun.

## <a name="remarks"></a>Notes

Quand l’horloge appelle cette méthode, elle spécifie le temps de référence actuel. Le planificateur détermine les demandes de notification qui ont expiré, le cas échéant, et les distribue. Si une demande d’une seule capture expire, le planificateur la supprime. En cas d’expiration d’une demande périodique, le planificateur la replanifie pour la prochaine notification. La méthode retourne l’heure de la demande en attente suivante.

Pour distribuer une demande de notification, le planificateur signale l’événement ou le sémaphore donné dans le paramètre *hNotify* de la méthode [**CAMSchedule :: AddAdvisePacket**](camschedule-addadvisepacket.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dsschedule. h (inclure Flux. h)</dt> </dl>                                                                                |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMSchedule, classe**](camschedule.md)
</dt> </dl>

 

 




