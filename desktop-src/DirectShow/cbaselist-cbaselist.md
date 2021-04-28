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
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099637"
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

## <a name="remarks"></a>Notes 

Pour des performances optimales, la `CBaseList` classe gère un cache de nœuds de liste. Si vous connaissez approximativement le nombre d’éléments que la liste doit contenir, utilisez cette version du constructeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




