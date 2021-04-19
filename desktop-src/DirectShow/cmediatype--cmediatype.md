---
description: Méthode de destructeur.
ms.assetid: 92375e95-adfb-414b-abbb-e827db2186ac
title: CMediaType. ~ CMediaType, destructeur (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.~CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26efde8fe7d3c3efd0f29c77945011cef5834829
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535223"
---
# <a name="cmediatypecmediatype-destructor"></a>CMediaType. ~ CMediaType, destructeur

Méthode de destructeur.

## <a name="syntax"></a>Syntaxe


```C++
~CMediaType();
```



## <a name="remarks"></a>Notes

Le destructeur appelle la fonction [**FreeMediaType**](freemediatype.md) sur lui-même.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




