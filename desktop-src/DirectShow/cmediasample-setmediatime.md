---
description: 'La méthode SetMediaTime définit les temps de support pour cet exemple. Cette méthode implémente la méthode IMediaSample :: SetMediaTime.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Méthode CMediaSample. SetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530412"
---
# <a name="cmediasamplesetmediatime-method"></a>Méthode CMediaSample. SetMediaTime

La `SetMediaTime` méthode définit les temps de support pour cet exemple. Cette méthode implémente la méthode [**IMediaSample :: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStart* 
</dt> <dd>

Pointeur désignant l’heure de début du média, ou **null**.

</dd> <dt>

*Attente* 
</dt> <dd>

Pointeur désignant l’heure d’arrêt du support, ou **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

L’heure d’arrêt du support doit être supérieure à l’heure de début du support. Utilisez **null** pour invalider les temps de support.

Le paramètre en *attente* spécifie un temps de support absolu, mais la variable de membre [**CMediaSample :: m \_ MediaEnd**](cmediasample-m-mediaend.md) est calculée comme un décalage par rapport à *pstart*. En d’autres termes, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  

Pour plus d’informations sur les temps de support, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




