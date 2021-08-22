---
description: CBaseList. CBaseList (TCHAR \* , int) Constructor-constructeur Method.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Constructeur CBaseList. CBaseList (TCHAR *, INT) (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bd3462da5b8403f4db8f4727c0baa0a825e0db62b95216801300442d5cc393c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586269"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a>Constructeur CBaseList. CBaseList (TCHAR \* , int)

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Pointeur vers le nom de la liste.

</dd> <dt>

*iItems* 
</dt> <dd>

Taille du cache du nœud.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour des performances optimales, la `CBaseList` classe gère un cache de nœuds de liste. Si vous connaissez approximativement le nombre d’éléments que la liste doit contenir, utilisez cette version du constructeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




