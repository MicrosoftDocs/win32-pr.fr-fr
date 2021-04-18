---
description: La méthode ThreadProc est la procédure de thread.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: CAMThread. ThreadProc, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526366"
---
# <a name="camthreadthreadproc-method"></a>CAMThread. ThreadProc, méthode

La `ThreadProc` méthode est la procédure de thread.

## <a name="syntax"></a>Syntaxe


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** dont la signification est définie par la classe dérivée.

## <a name="remarks"></a>Notes

Il s’agit d’une méthode virtuelle pure. Implémentez cette méthode dans votre classe dérivée pour fournir une procédure de thread. Quand la méthode [**CAMThread :: Create**](camthread-create.md) crée un thread, elle donne l’adresse de la méthode [**CAMThread :: InitialThreadProc**](camthread-initialthreadproc.md) , qui à son tour appelle votre méthode ThreadProc.

En règle générale, votre méthode ThreadProc entrera dans une boucle qui récupère les requêtes (en appelant les méthodes [**CAMThread :: GetRequest**](camthread-getrequest.md) ou [**CAMThread :: CheckRequest**](camthread-checkrequest.md) ) et traite les données.

Lorsque cette méthode est retournée, le thread se termine.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




