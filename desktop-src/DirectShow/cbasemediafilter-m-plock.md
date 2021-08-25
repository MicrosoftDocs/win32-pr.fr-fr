---
description: Pointeur vers une section critique.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Membre CBaseMediaFilter :: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad92cf07cc096c50ffa50f862c26f6133fc8dbb9b9b059419bb516e07cbd5daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910789"
---
# <a name="cbasemediafilterm_plock-member"></a>CBaseMediaFilter :: m \_ pLock, membre

Pointeur vers une section critique.

## <a name="syntax"></a>Syntaxe


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Notes

La section critique est conservée lors des transitions d’État ([**CBaseMediaFilter :: Run**](cbasemediafilter-run.md), [**CBaseMediaFilter ::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter :: Stop**](cbasemediafilter-stop.md)), lors de l’accès à l’horloge de référence ([**CBaseMediaFilter :: SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter :: GetSyncSource**](cbasemediafilter-getsyncsource.md)) et dans la méthode [**CBaseMediaFilter :: IsActive**](cbasemediafilter-isactive.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




