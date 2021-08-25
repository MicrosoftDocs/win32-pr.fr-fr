---
description: 'Méthode COutputQueue. BeginFlush : la méthode BeginFlush commence une opération de vidage.'
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Méthode COutputQueue. BeginFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7b002c03ee0bfb95733ac9af0f6e88444cc6a42bec2af7d9a40a307d83d2fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909649"
---
# <a name="coutputqueuebeginflush-method"></a>Méthode COutputQueue. BeginFlush

La `BeginFlush` méthode commence une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
void BeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode définit la variable de membre [**COutputQueue :: m \_ BFlushing**](coutputqueue-m-bflushing.md) sur **true**. Si l’objet utilise un thread, le thread appelle la méthode [**COutputQueue :: FreeSamples**](coutputqueue-freesamples.md) pour libérer les échantillons en attente. Dans le cas contraire, l’objet appelle **FreeSamples** pendant la méthode [**COutputQueue :: EndFlush**](coutputqueue-endflush.md) . Cette méthode définit également la variable de membre [**COutputQueue :: m \_ HR**](coutputqueue-m-hr.md) sur S \_ false, ce qui provoque l’annulation de tous les nouveaux exemples de l’objet.

L’objet transmet la notification de vidage en aval en appelant la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




