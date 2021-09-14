---
description: La méthode Free est appelée pendant une opération de dévalidation.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: CMemAllocator. free, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224857"
---
# <a name="cmemallocatorfree-method"></a>CMemAllocator. free, méthode

La `Free` méthode est appelée pendant une opération de dévalidation. Cette méthode implémente la méthode [**CBaseAllocator :: Free**](cbaseallocator-free.md) virtuelle pure, mais ne fait rien. La mémoire tampon n’est pas libérée tant que l’objet **CMemAllocator** n’est pas détruit. La méthode de destructeur appelle [**CMemAllocator :: ReallyFree**](cmemallocator-reallyfree.md) pour libérer la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
void Free();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMemAllocator, classe**](cmemallocator.md)
</dt> </dl>

 

 




