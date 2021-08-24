---
description: 'Méthode COutputQueue. EndFlush : la méthode EndFlush termine une opération de vidage.'
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
ms.openlocfilehash: d9a283867036254b7a13b45ba152c3f16ecccbdb59d4d59e98c8d1dae7480e13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634219"
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

## <a name="remarks"></a>Remarques

Si l’objet utilise un thread, cette méthode attend l’événement [**COutputQueue :: m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) . Le thread signale cet événement après qu’il a libéré des échantillons en attente. Si l’objet n’utilise pas de thread, cette méthode appelle la méthode [**COutputQueue :: FreeSamples**](coutputqueue-freesamples.md) . La `EndFlush` méthode appelle ensuite la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




