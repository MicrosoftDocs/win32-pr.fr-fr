---
description: La méthode GetSchedule récupère un pointeur vers l’objet de planification de l’horloge.
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: Méthode CBaseReferenceClock. GetSchedule (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a37cdb3e18f3ab71b144af071233aee5a6a3a93d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528460"
---
# <a name="cbasereferenceclockgetschedule-method"></a>Méthode CBaseReferenceClock. GetSchedule

La `GetSchedule` méthode récupère un pointeur vers l’objet de planification de l’horloge.

## <a name="syntax"></a>Syntaxe


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la variable de membre [**CBaseReferenceClock :: m \_ pSchedule**](cbasereferenceclock-m-pschedule.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




