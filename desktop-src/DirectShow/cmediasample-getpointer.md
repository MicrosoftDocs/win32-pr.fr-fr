---
description: 'La méthode GetPointer récupère un pointeur de lecture/écriture vers la mémoire tampon. Cette méthode implémente la méthode IMediaSample :: GetPointer.'
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Méthode CMediaSample. GetPointer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528064"
---
# <a name="cmediasamplegetpointer-method"></a>Méthode CMediaSample. GetPointer

La `GetPointer` méthode récupère un pointeur en lecture/écriture vers la mémoire tampon. Cette méthode implémente la méthode [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




