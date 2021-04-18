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
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533439"
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

## <a name="remarks"></a>Notes

Cette méthode implémente la méthode [**IReferenceClockTimerControl :: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




