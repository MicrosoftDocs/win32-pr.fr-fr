---
description: La méthode IsQueued détermine si l’objet utilise un thread de travail pour fournir des exemples.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Méthode COutputQueue. IsQueued (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47093acedb3a28d633ea2c8b0bbdbba3c1493de7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195619"
---
# <a name="coutputqueueisqueued-method"></a>Méthode COutputQueue. IsQueued

La `IsQueued` méthode détermine si l’objet utilise un thread de travail pour fournir des exemples.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsQueued();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si l’objet utilise un thread de travail, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




