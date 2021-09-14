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
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239285"
---
# <a name="cbasemediafilterm_plock-member"></a>CBaseMediaFilter :: m \_ pLock, membre

Pointeur vers une section critique.

## <a name="syntax"></a>Syntaxe


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Notes

La section critique est conservée lors des transitions d’État ([**CBaseMediaFilter :: Run**](cbasemediafilter-run.md), [**CBaseMediaFilter ::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter :: Stop**](cbasemediafilter-stop.md)), lors de l’accès à l’horloge de référence ([**CBaseMediaFilter :: SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter :: GetSyncSource**](cbasemediafilter-getsyncsource.md)) et dans la méthode [**CBaseMediaFilter :: IsActive**](cbasemediafilter-isactive.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




