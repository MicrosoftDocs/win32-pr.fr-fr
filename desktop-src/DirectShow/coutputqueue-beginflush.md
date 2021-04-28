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
ms.openlocfilehash: e7c6168daf766ec11e18e86673d9d25542b50462
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099027"
---
# <a name="coutputqueuebeginflush-method"></a>Méthode COutputQueue. BeginFlush

La `BeginFlush` méthode commence une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
void BeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes 

Cette méthode définit la variable de membre [**COutputQueue :: m \_ BFlushing**](coutputqueue-m-bflushing.md) sur **true**. Si l’objet utilise un thread, le thread appelle la méthode [**COutputQueue :: FreeSamples**](coutputqueue-freesamples.md) pour libérer les échantillons en attente. Dans le cas contraire, l’objet appelle **FreeSamples** pendant la méthode [**COutputQueue :: EndFlush**](coutputqueue-endflush.md) . Cette méthode définit également la variable de membre [**COutputQueue :: m \_ HR**](coutputqueue-m-hr.md) sur S \_ false, ce qui provoque l’annulation de tous les nouveaux exemples de l’objet.

L’objet transmet la notification de vidage en aval en appelant la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




