---
description: Méthode constructeur CBaseList. CBaseList.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Constructeur CBaseList. CBaseList (Wxlist. h)
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
ms.openlocfilehash: 0b734722371aa80e3c120dde3c6fb629785dfc6cdf9786c7f4ab1cbea87e5559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016977"
---
# <a name="cbaselistcbaselist-constructor"></a>Constructeur CBaseList. CBaseList

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Pointeur vers le nom de la liste.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour des performances optimales, la `CBaseList` classe gère un cache de nœuds de liste. Cette version du constructeur utilise une taille de cache par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




