---
description: La méthode AddHead insère une autre liste au début de cette liste.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Méthode CBaseList. AddHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa8108af5f779bea4c1a1e756ab018ed9c902d3e516556c42b7899f442cb7704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814319"
---
# <a name="cbaselistaddhead-method"></a>Méthode CBaseList. AddHead

La `AddHead` méthode insère une autre liste au début de cette liste.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pList* 
</dt> <dd>

Pointeur vers la liste des éléments à ajouter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Si la méthode échoue, il se peut que certains éléments aient été ajoutés à la liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




