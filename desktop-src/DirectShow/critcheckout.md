---
description: Retourne la valeur FALSe si le thread actuel est le propriétaire de la section critique spécifiée.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: CritCheckOut, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fb1289bd89771797be88220f49d8af6f468a11c54e9954c32786e3af72dc1956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908089"
---
# <a name="critcheckout-function"></a>CritCheckOut fonction)

Retourne la **valeur false** si le thread actuel est le propriétaire de la section critique spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CritCheckOut(
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

Dans les versions Debug, retourne **false** si le thread actuel est le propriétaire de cette section critique, ou **true** dans le cas contraire. Dans les versions commerciales, retourne toujours la **valeur true**.

## <a name="remarks"></a>Remarques

Cette fonction est l’inverse de la fonction [**CritCheckIn**](critcheckin.md) . Si **CritCheckIn** retourne la **valeur true**, **CritCheckOut** retourne la **valeur false**, et vice versa.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de débogage des sections critiques](critical-section-debugging-functions.md)
</dt> </dl>

 

 




