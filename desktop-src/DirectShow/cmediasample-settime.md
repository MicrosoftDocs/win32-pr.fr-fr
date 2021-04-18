---
description: 'La méthode SetTime définit les temps de flux lorsque cet exemple doit commencer et se terminer. Cette méthode implémente la méthode IMediaSample :: SetTime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: CMediaSample. SetTime, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520369"
---
# <a name="cmediasamplesettime-method"></a>CMediaSample. SetTime, méthode

La `SetTime` méthode définit les temps de flux lorsque cet exemple doit commencer et se terminer. Cette méthode implémente la méthode [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Pointeur vers le temps de flux auquel l’échantillon commence, en unités de 100 nanosecondes, ou **null**.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Pointeur vers le temps de flux auquel l’échantillon se termine, en unités de 100 nanosecondes, ou **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode définit les variables de membre de fin [**CMediaSample :: m \_ Start**](cmediasample-m-start.md) et [**CMediaSample :: m \_**](cmediasample-m-end.md) , qui spécifient les horodatages. Il met également à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie si les horodatages sont valides.

Pour plus d’informations sur les horodatages, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




