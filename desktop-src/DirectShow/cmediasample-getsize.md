---
description: 'La méthode Desize récupère la taille de la mémoire tampon. Cette méthode implémente la méthode IMediaSample :: AD.'
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: CMediaSample., méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3559f972f35a01738c60f32414ab0b42a079032ac5bc6b3ab0e5b7212900d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156750"
---
# <a name="cmediasamplegetsize-method"></a>CMediaSample. adla méthode

La `GetSize` méthode récupère la taille de la mémoire tampon. Cette méthode implémente la méthode [**IMediaSample :: AD**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) .

## <a name="syntax"></a>Syntaxe


```C++
LONG GetSize();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la taille de la mémoire tampon, en octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




