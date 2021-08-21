---
description: Valeur booléenne qui spécifie s’il faut tracer ce verrou.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Membre CCritSec :: m_fTrace (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5a47437e4f9ab475b64979ec970604ac7a621d2ab53ea7a3c87742fa81a8aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074393"
---
# <a name="ccritsecm_ftrace-member"></a>CCritSec :: m \_ fTrace, membre

Valeur booléenne qui spécifie s’il faut tracer ce verrou.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Notes

Cette variable membre est définie uniquement dans la version Debug de la classe de base. Si la valeur est **true**, une trace de l’état du verrou est écrite dans le journal de débogage. (La journalisation du débogage des sections critiques doit être active.) Pour plus d’informations, consultez [**DbgLockTrace**](dbglocktrace.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> </dl>

 

 




