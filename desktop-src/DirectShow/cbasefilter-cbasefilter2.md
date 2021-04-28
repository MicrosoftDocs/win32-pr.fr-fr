---
description: Méthode de constructeur de constructeur CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID).
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID), constructeur (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b621bdb3f6a15ae950959a65eba8841bde399b81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099827"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a>Constructeur CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID)

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseFilter(
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

Pointeur vers une chaîne contenant le nom du filtre, à des fins de débogage.

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

Identificateur de classe (CLSID) du filtre.

</dd> </dl>

## <a name="remarks"></a>Notes 

Pour l’objet de section critique, vous pouvez généralement effectuer l’une des opérations suivantes :

-   Dérivez une classe qui hérite à la fois de **CBaseFilter** et de **CCritSec**. Pour *pLock*, transmettez le `this` pointeur.
-   Dérivez une classe qui hérite de **CBaseFilter** et qui contient une variable membre **CCritSec** . Pour *pLock*, transmettez l’adresse de cette variable.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




