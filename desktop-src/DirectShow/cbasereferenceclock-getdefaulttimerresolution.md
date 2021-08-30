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
ms.openlocfilehash: dbd3eb192839d6957af9fb63c32a1b1dcbb3a5c386c47d2f66408ec63d7cba21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076562"
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

## <a name="remarks"></a>Remarques

Cette méthode implémente la méthode [**IReferenceClockTimerControl :: GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




