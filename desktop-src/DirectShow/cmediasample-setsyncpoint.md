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
ms.openlocfilehash: 0be51ed18e25bcbd12e33f9167493d73f0c140480f4ec0042fb0c43928720d3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156521"
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

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode met à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie la propriété de point de synchronisation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




