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
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540663"
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
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> </dl>

 

 




