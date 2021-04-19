---
description: La méthode GetDefaultTimerResolution retourne la résolution actuelle de la minuterie de l’horloge de référence.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Méthode CBaseReferenceClock. GetDefaultTimerResolution (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520922"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a>Méthode CBaseReferenceClock. GetDefaultTimerResolution

La `GetDefaultTimerResolution` méthode retourne la résolution actuelle de la minuterie de l’horloge de référence.

## <a name="syntax"></a>Syntaxe


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTimerResolution* 
</dt> <dd>

Reçoit la résolution de la minuterie demandée, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode implémente la méthode [**IReferenceClockTimerControl :: GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




