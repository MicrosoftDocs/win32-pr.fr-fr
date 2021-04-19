---
description: La méthode MoveToTail fractionne la liste et ajoute la partie d’en-tête à la fin d’une autre liste.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Méthode CBaseList. MoveToTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539276"
---
# <a name="cbaselistmovetotail-method"></a>Méthode CBaseList. MoveToTail

La `MoveToTail` méthode fractionne la liste et ajoute la partie d’en-tête à la fin d’une autre liste.

## <a name="syntax"></a>Syntaxe


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Indicateur de position qui marque le fractionnement dans la liste.

</dd> <dt>

*pList* 
</dt> <dd>

Pointeur vers une autre liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Cette méthode fractionne la liste après la position spécifiée par le paramètre *pos* . La partie fin reste dans la liste. La partie Head est ajoutée à la fin de l’autre liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




