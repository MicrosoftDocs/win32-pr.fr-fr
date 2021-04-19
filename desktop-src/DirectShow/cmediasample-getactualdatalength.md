---
description: 'La méthode GetActualDataLength récupère la longueur des données valides dans la mémoire tampon. Cette méthode implémente la méthode IMediaSample :: GetActualDataLength.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Méthode CMediaSample. GetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535368"
---
# <a name="cmediasamplegetactualdatalength-method"></a>Méthode CMediaSample. GetActualDataLength

La `GetActualDataLength` méthode récupère la longueur des données valides dans la mémoire tampon. Cette méthode implémente la méthode [**IMediaSample :: GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) .

## <a name="syntax"></a>Syntaxe


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la longueur des données valides, en octets.

## <a name="remarks"></a>Notes

La variable membre [**CMediaSample :: m \_ lActual**](cmediasample-m-lactual.md) spécifie cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

