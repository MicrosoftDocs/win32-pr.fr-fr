---
description: 'La méthode SetSyncPoint spécifie si le début de cet exemple est un point de synchronisation. Cette méthode implémente la méthode IMediaSample :: SetSyncPoint.'
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Méthode CMediaSample. SetSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219068"
---
# <a name="cmediasamplesetsyncpoint-method"></a>Méthode CMediaSample. SetSyncPoint

La `SetSyncPoint` méthode spécifie si le début de cet exemple est un point de synchronisation. Cette méthode implémente la méthode [**IMediaSample :: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bIsSyncPoint* 
</dt> <dd>

Valeur booléenne qui spécifie s’il s’agit d’un point de synchronisation. Si la **valeur est true**, il s’agit d’un point de synchronisation.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode met à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie la propriété de point de synchronisation.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




