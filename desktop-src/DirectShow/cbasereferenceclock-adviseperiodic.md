---
description: 'La méthode AdvisePeriodic crée une demande de notification périodique. Cette méthode implémente la méthode IReferenceClock :: AdvisePeriodic.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Méthode CBaseReferenceClock. AdvisePeriodic (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4b81fc8dfc33cc2a6e5207e984de0c2e693b8c00b8f8d35949d0bb7150484bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052429"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>Méthode CBaseReferenceClock. AdvisePeriodic

La `AdvisePeriodic` méthode crée une demande de notification périodique. Cette méthode implémente la méthode [**IReferenceClock :: AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartTime* 
</dt> <dd>

Heure de la première notification, en unités de 100 nanosecondes. Doit être supérieur à zéro et inférieur à la \_ durée maximale.

</dd> <dt>

*PeriodTime* 
</dt> <dd>

Temps entre les notifications, en unités de 100 nanosecondes. Doit être supérieur à zéro.

</dd> <dt>

*hSemaphore* 
</dt> <dd>

Handle vers un sémaphore, créé par l’appelant.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Pointeur vers une variable qui reçoit un identificateur pour la demande de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                   | Description                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Succès<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valeurs de temps non valides<br/>       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Échec<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null**<br/> |



 

## <a name="remarks"></a>Remarques

À chaque heure de notification, l’horloge libère le sémaphore spécifié dans le paramètre *hSemaphore* . Quand aucune autre notification n’est requise, appelez la méthode [**CBaseReferenceClock :: Unadvise**](cbasereferenceclock-unadvise.md) et transmettez la valeur *pdwAdviseToken* retournée à partir de cet appel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




