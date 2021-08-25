---
description: Retourne la valeur TRUE si le thread actuel est le propriétaire de la section critique spécifiée.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: CritCheckIn, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f4e9ff0078f6efe8dee9b060e61858c24aea0a64e7e35b9fb867125b8612ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908079"
---
# <a name="critcheckin-function"></a>CritCheckIn fonction)

Retourne la **valeur true** si le thread actuel est le propriétaire de la section critique spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcCrit* 
</dt> <dd>

Pointeur vers une section critique [**CCritSec**](ccritsec.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Dans les versions Debug, retourne la **valeur true** si le thread actuel est le propriétaire de cette section critique, ou **false** dans le cas contraire. Dans les versions commerciales, retourne toujours la **valeur true**.

## <a name="remarks"></a>Remarques

Cette fonction est particulièrement utile dans la macro [**Assert**](assert.md) pour tester si un thread possède un verrou donné.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment utiliser cette fonction :


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de débogage des sections critiques](critical-section-debugging-functions.md)
</dt> </dl>

 

 




