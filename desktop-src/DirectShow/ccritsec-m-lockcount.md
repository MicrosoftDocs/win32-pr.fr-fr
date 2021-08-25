---
description: Nombre de verrous en attente sur cet objet.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Membre CCritSec :: m_lockCount (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9885f3270c021432342605ad84c1b521672022f4a13cecac5ac49c9248c65d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872209"
---
# <a name="ccritsecm_lockcount-member"></a>CCritSec :: m \_ lockCount, membre

Nombre de verrous en attente sur cet objet.

## <a name="syntax"></a>Syntaxe


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a>Notes

Cette variable membre est définie uniquement dans la version Debug de la classe de base. Les fonctions de [débogage des sections critiques](critical-section-debugging-functions.md) utilisent ce membre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> </dl>

 

 




