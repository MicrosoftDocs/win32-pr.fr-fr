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
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525191"
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
| <dl> <dt>**\_OK**</dt> </dl>                         | Opération réussie.<br/>                                 |
| <dl> <dt>**\_heure du média VFW E \_ \_ \_ non \_ définie**</dt> </dl> | Aucun temps de support n’a été défini pour cet exemple.<br/> |



 

## <a name="remarks"></a>Notes

La variable de membre [**CMediaSample :: m \_ MediaEnd**](cmediasample-m-mediaend.md) spécifie un décalage à partir de [**CMediaSample :: m \_ MediaStart**](cmediasample-m-mediastart.md), mais la valeur reçue par le paramètre en *attente* est un temps de support absolu, calculé comme **m \_** MediaStart  +  **m \_ MediaEnd**.

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

 

 




