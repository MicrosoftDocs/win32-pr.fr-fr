---
description: Méthode constructeur CBaseMediaFilter. CBaseMediaFilter.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Constructeur CBaseMediaFilter. CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096317"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>Constructeur CBaseMediaFilter. CBaseMediaFilter

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Pointeur vers une chaîne contenant le nom de l’objet.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*pLock* 
</dt> <dd>

Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.

</dd> <dt>

*identificateur* 
</dt> <dd>

Identificateur de classe de l’objet.

</dd> </dl>

## <a name="remarks"></a>Notes 

Si un autre objet contient ou agrège l' `CBaseMediaFilter` objet, le verrou **CCritSec** peut être externe à l' `CBaseMediaFilter` objet. Dans ce cas, transmettez un pointeur vers le verrou dans *pLock*.

Dans le cas contraire, vous pouvez :

-   Dérivez une classe qui hérite à la fois `CBaseMediaFilter` de et de **CCritSec**. Pour *pLock*, transmettez le pointeur this.
-   Dérivez une classe qui hérite de `CBaseMediaFilter` et contient une variable membre **CCritSec** . Pour *pLock*, transmettez l’adresse de cette variable.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




