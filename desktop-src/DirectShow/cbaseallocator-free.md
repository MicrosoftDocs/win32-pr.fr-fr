---
description: La méthode Free libère toute la mémoire tampon. Cette méthode est appelée lorsque le filtre propriétaire annule la validation de l’allocateur, après la libération du dernier échantillon multimédia.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: CBaseAllocator. free, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296855"
---
# <a name="cbaseallocatorfree-method"></a>CBaseAllocator. free, méthode

La `Free` méthode libère toute la mémoire tampon. Cette méthode est appelée lorsque le filtre propriétaire annule la validation de l’allocateur, après la libération du dernier échantillon multimédia.

## <a name="syntax"></a>Syntaxe


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Après l’appel de la méthode de [**dévalidation**](cbaseallocator-decommit.md) , l’allocateur appelle cette méthode lorsqu’il libère le dernier exemple multimédia. La classe dérivée doit implémenter cette méthode.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




