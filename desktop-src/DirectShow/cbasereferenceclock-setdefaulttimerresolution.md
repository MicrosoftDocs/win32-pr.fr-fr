---
description: La méthode SetDefaultTimerResolution définit la résolution de la minuterie de l’horloge de référence.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Méthode CBaseReferenceClock. SetDefaultTimerResolution (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 980f31856aba14079da0f5b9625dca40846255d6f02361b2798d7c38c1cd4f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087419"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a>Méthode CBaseReferenceClock. SetDefaultTimerResolution

La `SetDefaultTimerResolution` méthode définit la résolution de la minuterie de l’horloge de référence.

## <a name="syntax"></a>Syntaxe


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*timerResolution* 
</dt> <dd>

Résolution minimale de la minuterie, en unités de 100 nanosecondes. Si la valeur est égale à zéro, l’horloge de référence annule la requête précédente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode implémente la méthode [**IReferenceClockTimerControl :: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




