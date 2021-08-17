---
description: 'La méthode GetTime récupère le temps de référence actuel. Cette méthode implémente la méthode IReferenceClock :: GetTime.'
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: CBaseReferenceClock. GetTime, méthode (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a1ffd021ac917a7aa1e12f3d3dc9c4a62ea1f883f126bca1d9c1300d335bdae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954978"
---
# <a name="cbasereferenceclockgettime-method"></a>CBaseReferenceClock. GetTime, méthode

La `GetTime` méthode récupère le temps de référence actuel. Cette méthode implémente la méthode [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTime* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure actuelle, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                               | Description                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null** .<br/>                       |
| <dl> <dt>**S \_ false**</dt> </dl>   | L’heure retournée est identique à la valeur précédente.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Réussite.<br/>                                         |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode [**CBaseReferenceClock :: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) pour déterminer l’heure réelle de l’horloge. Si l’heure de l’horloge est strictement supérieure à la valeur précédente, `GetTime` utilise l’heure de l’horloge et retourne S \_ OK. Dans le cas contraire, `GetTime` utilise la valeur précédente et retourne S \_ false. Par conséquent, l’horloge interne peut s’exécuter en arrière pendant une brève période, sans entraîner la réexécution du temps de référence. Au lieu de cela, le temps de référence est « bloqué » à la même valeur jusqu’à ce que l’horloge interne soit interceptée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




