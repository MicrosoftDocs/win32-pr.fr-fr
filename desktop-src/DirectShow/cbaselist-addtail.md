---
description: La méthode AddTail ajoute une autre liste à la fin de cette liste.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Méthode CBaseList. AddTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5663a69d803def2b37f9a1ba677966a5b26a8bfc6f7b6eb1eb98eef85bcd961d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659152"
---
# <a name="cbaselistaddtail-method"></a>Méthode CBaseList. AddTail

La `AddTail` méthode ajoute une autre liste à la fin de cette liste.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pList* 
</dt> <dd>

Pointeur vers la liste à ajouter.

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

 

 




