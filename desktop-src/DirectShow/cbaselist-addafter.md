---
description: La méthode AddAfter insère une liste après la position spécifiée.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Méthode CBaseList. AddAfter (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28351e1e0762b8e45bc9bf2ba1fe3624c67339e9b8bcf59ec5a919850a853061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983500"
---
# <a name="cbaselistaddafter-method"></a>Méthode CBaseList. AddAfter

La `AddAfter` méthode insère une liste après la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Position après laquelle insérer la liste.

</dd> <dt>

*pList* 
</dt> <dd>

Pointeur vers la liste à insérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Les indicateurs de position existants, y compris celui spécifié dans le paramètre *pos* , restent valides. Si la méthode échoue, certains éléments ont peut-être été ajoutés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




