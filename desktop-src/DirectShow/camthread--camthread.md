---
description: CAMThread. ~ CAMThread, destructeur, méthode de destructeur.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: CAMThread. ~ CAMThread, destructeur (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094965"
---
# <a name="camthreadcamthread-destructor"></a>CAMThread. ~ CAMThread, destructeur

Méthode de destructeur.

## <a name="syntax"></a>Syntaxe


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Notes

Le destructeur appelle la méthode [**CAMThread :: Close**](camthread-close.md) , qui attend que le thread se termine.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




