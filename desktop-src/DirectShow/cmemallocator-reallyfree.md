---
description: La méthode ReallyFree libère la mémoire pour les mémoires tampons.
ms.assetid: c5c5d09f-b4f2-4a06-9309-3b2a8b8f8f1f
title: Méthode CMemAllocator. ReallyFree (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.ReallyFree
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ad7ca95fc7a79e97e5aea79da79fb1b161911e5835509f3a2288578e068e0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954358"
---
# <a name="cmemallocatorreallyfree-method"></a>Méthode CMemAllocator. ReallyFree

La `ReallyFree` méthode libère la mémoire pour les mémoires tampons.

## <a name="syntax"></a>Syntaxe


```C++
void ReallyFree();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La classe [**CMemAllocator**](cmemallocator.md) conserve la mémoire jusqu’à ce que l’objet soit supprimé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMemAllocator, classe**](cmemallocator.md)
</dt> </dl>

 

 




