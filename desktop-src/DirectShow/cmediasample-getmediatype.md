---
description: 'La méthode GetMediaType récupère le type de média si le type de média diffère de l’exemple précédent. Cette méthode implémente la méthode IMediaSample :: GetMediaType.'
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Méthode CMediaSample. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296767"
---
# <a name="cmediasamplegetmediatype-method"></a>Méthode CMediaSample. GetMediaType

La `GetMediaType` méthode récupère le type de média si le type de média diffère de l’exemple précédent. Cette méthode implémente la méthode [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppMediaType* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Si le type de média n’a pas été modifié par rapport à l’exemple précédent, *\* ppMediaType* a la valeur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                   | Description                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Le type de média n’a pas été modifié par rapport à l’exemple précédent.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                                                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                                     |



 

## <a name="remarks"></a>Notes

Lorsque vous avez terminé avec le type de média, libérez le bloc de mémoire en appelant la fonction de l’utilitaire [**DeleteMediaType**](deletemediatype.md) .

La variable membre [**CMediaSample :: m \_ pMediaType**](cmediasample-m-pmediatype.md) spécifie le type de média. La variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) spécifie si le type de média a changé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




