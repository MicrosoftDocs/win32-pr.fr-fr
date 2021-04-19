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
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523574"
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

## <a name="remarks"></a>Notes

Cette fonction est l’inverse de la fonction [**CritCheckIn**](critcheckin.md) . Si **CritCheckIn** retourne la **valeur true**, **CritCheckOut** retourne la **valeur false**, et vice versa.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de débogage des sections critiques](critical-section-debugging-functions.md)
</dt> </dl>

 

 




