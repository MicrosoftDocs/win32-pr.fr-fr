---
description: Identificateur de thread du thread propriétaire.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Membre CCritSec :: m_currentOwner (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71c88055f5068a5486c1eb6e3ac739235a6b7cde2e8d6b767380160ff12503be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657212"
---
# <a name="ccritsecm_currentowner-member"></a>CCritSec :: m \_ currentOwner, membre

Identificateur de thread du thread propriétaire.

## <a name="syntax"></a>Syntaxe


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>Notes

Cette variable membre est définie uniquement dans la version Debug de la classe de base. Les [fonctions de débogage de la section critique](critical-section-debugging-functions.md) utilisent ce membre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> </dl>

 

 




