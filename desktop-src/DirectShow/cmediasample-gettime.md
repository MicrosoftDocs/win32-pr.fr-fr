---
description: 'La méthode GetTime récupère les temps de flux auxquels cet exemple doit commencer et se terminer. Cette méthode implémente la méthode IMediaSample :: GetTime.'
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: CMediaSample. GetTime, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223468"
---
# <a name="cmediasamplegettime-method"></a>CMediaSample. GetTime, méthode

La `GetTime` méthode récupère les temps de flux auxquels cet exemple doit commencer et se terminer. Cette méthode implémente la méthode [**IMediaSample :: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Pointeur vers une variable qui reçoit le temps de flux de début, en unités de 100 nanosecondes.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Pointeur vers une variable qui reçoit le temps de flux de fin, en unités de 100 nanosecondes. Si l’exemple n’a pas de temps d’arrêt, la valeur est définie sur l’heure de début plus un.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                   | Description                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                          | Réussite.<br/>                                         |
| <dl> <dt>**VFW \_ S \_ sans \_ heure d’arrêt \_**</dt> </dl>         | L’exemple a une heure de début valide, mais aucune heure d’arrêt.<br/> |
| <dl> <dt>**\_exemple de temps d’échantillonnage VFW E \_ \_ \_ non \_ défini**</dt> </dl> | L’exemple n’a pas de datage valide.<br/>          |



 

## <a name="remarks"></a>Notes

Les variables de membre de fin [**CMediaSample :: m \_ Start**](cmediasample-m-start.md) et [**CMediaSample :: m \_**](cmediasample-m-end.md) spécifient les horodatages. La variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) spécifie si les horodatages sont valides.

Pour plus d’informations sur les horodatages, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




