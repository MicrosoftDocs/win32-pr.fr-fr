---
description: La méthode GetNextAdviseTime récupère l’heure de la demande de notification suivante.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Méthode CAMSchedule. GetNextAdviseTime (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528865"
---
# <a name="camschedulegetnextadvisetime-method"></a>Méthode CAMSchedule. GetNextAdviseTime

La `GetNextAdviseTime` méthode récupère l’heure de la demande de notification suivante.

## <a name="syntax"></a>Syntaxe


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne le temps de référence de la demande d’avis suivante ou la \_ durée maximale pendant laquelle aucune demande n’est planifiée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dsschedule. h (include streams. h)</dt> </dl>                                                                                |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMSchedule, classe**](camschedule.md)
</dt> </dl>

 

 




