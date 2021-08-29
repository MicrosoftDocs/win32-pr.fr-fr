---
description: CSourceStream. ~ CSourceStream, destructeur, méthode de destructeur.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: CSourceStream. ~ CSourceStream, destructeur (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2e5fb1a09fe089df7d90846e25870a2c1e42987c07361809d958d303f257fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073353"
---
# <a name="csourcestreamcsourcestream-destructor"></a>CSourceStream. ~ CSourceStream, destructeur

Méthode de destructeur.

## <a name="syntax"></a>Syntaxe


```C++
~CSourceStream();
```



## <a name="remarks"></a>Notes

Le destructeur supprime automatiquement le code confidentiel du filtre propriétaire en appelant [**CSource :: RemovePin**](csource-removepin.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




