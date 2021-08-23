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
ms.openlocfilehash: 8ae7ab918c8c4ef707b2754f8b1ba1f8f3e76265a6b8ac0b252e765de2aff1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016917"
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

## <a name="remarks"></a>Remarques

Cette méthode fractionne la liste après la position spécifiée par le paramètre *pos* . La partie fin reste dans la liste. La partie Head est ajoutée à la fin de l’autre liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




