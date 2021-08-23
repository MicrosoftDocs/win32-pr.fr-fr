---
description: La méthode RemoveHeadI supprime le premier élément de la liste.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Méthode CBaseList. RemoveHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc4d9e039735888d6694422a1802b73b3781316210fd42e13eec9bac5094d322
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814309"
---
# <a name="cbaselistremoveheadi-method"></a>Méthode CBaseList. RemoveHeadI

La `RemoveHeadI` méthode supprime le premier élément de la liste.

## <a name="syntax"></a>Syntaxe


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’élément, ou **null** si la liste est vide.

## <a name="remarks"></a>Remarques

Cette méthode supprime le nœud de liste, mais pas l’élément contenu dans le nœud.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




