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
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085207"
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
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




