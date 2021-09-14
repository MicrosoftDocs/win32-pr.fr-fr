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
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012278"
---
# <a name="ccritsecm_ftrace-member"></a>CCritSec :: m \_ fTrace, membre

Valeur booléenne qui spécifie s’il faut tracer ce verrou.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Notes

Cette variable membre est définie uniquement dans la version Debug de la classe de base. Si la valeur est **true**, une trace de l’état du verrou est écrite dans le journal de débogage. (La journalisation du débogage des sections critiques doit être active.) Pour plus d’informations, consultez [**DbgLockTrace**](dbglocktrace.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> </dl>

 

 




