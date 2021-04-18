---
description: La méthode EndFlush termine une opération de vidage.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Méthode COutputQueue. EndFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e18afec866176147c5c75a57fca522c4ebc5fcf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540562"
---
# <a name="coutputqueueendflush-method"></a>Méthode COutputQueue. EndFlush

La `EndFlush` méthode termine une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
void EndFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si l’objet utilise un thread, cette méthode attend l’événement [**COutputQueue :: m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) . Le thread signale cet événement après qu’il a libéré des échantillons en attente. Si l’objet n’utilise pas de thread, cette méthode appelle la méthode [**COutputQueue :: FreeSamples**](coutputqueue-freesamples.md) . La `EndFlush` méthode appelle ensuite la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




