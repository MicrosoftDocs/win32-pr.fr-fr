---
description: La méthode TriggerThread sort le thread de travail qui gère la planification.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Méthode CBaseReferenceClock. TriggerThread (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543310"
---
# <a name="cbasereferenceclocktriggerthread-method"></a>Méthode CBaseReferenceClock. TriggerThread

La `TriggerThread` méthode sort du thread de travail qui gère la planification.

## <a name="syntax"></a>Syntaxe


```C++
void TriggerThread();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

L’horloge utilise un thread de travail qui appelle la méthode [**CAMSchedule :: Advise**](camschedule-advise.md) aux moments opportuns. La classe dérivée peut appeler `TriggerThread` pour réveiller le thread.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




