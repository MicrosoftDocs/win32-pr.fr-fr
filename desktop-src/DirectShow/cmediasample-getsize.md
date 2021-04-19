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
ms.openlocfilehash: ff4146b66ca62905fe54eeb88d1e38ccf56ceea9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520804"
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
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




