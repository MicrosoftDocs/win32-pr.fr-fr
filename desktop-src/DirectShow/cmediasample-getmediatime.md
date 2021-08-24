---
description: 'La méthode GetMediaTime récupère les temps de support pour cet exemple. Cette méthode implémente la méthode IMediaSample :: GetMediaTime.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Méthode CMediaSample. GetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901531b3aaff882700a6a6196330cc7b0823b8b0069024101953f5f79a54e17d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634679"
---
# <a name="cmediasamplegetmediatime-method"></a>Méthode CMediaSample. GetMediaTime

La `GetMediaTime` méthode récupère les temps de support pour cet exemple. Cette méthode implémente la méthode [**IMediaSample :: GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStart* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure de début du média.

</dd> <dt>

*Attente* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure d’arrêt du support.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                  | Description                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Réussite.<br/>                                 |
| <dl> <dt>**\_heure du média VFW E \_ \_ \_ non \_ définie**</dt> </dl> | Aucun temps de support n’a été défini pour cet exemple.<br/> |



 

## <a name="remarks"></a>Remarques

La variable de membre [**CMediaSample :: m \_ MediaEnd**](cmediasample-m-mediaend.md) spécifie un décalage à partir de [**CMediaSample :: m \_ MediaStart**](cmediasample-m-mediastart.md), mais la valeur reçue par le paramètre en *attente* est un temps de support absolu, calculé comme **m \_** MediaStart  +  **m \_ MediaEnd**.

Pour plus d’informations sur les temps de support, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




