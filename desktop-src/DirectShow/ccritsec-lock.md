---
description: La méthode Lock verrouille l’objet de section critique.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: CCritSec. Lock, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4241b2cd5e94fbd6a3cbe0abd91d47ad6312c44b71f76c214cffb22836033a7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928588"
---
# <a name="ccritseclock-method"></a>CCritSec. Lock, méthode

La méthode **Lock** verrouille l’objet de section critique.

## <a name="syntax"></a>Syntaxe


```C++
void Lock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode appelle la fonction [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .

Appelez la fonction membre [**CCritSec :: Unlock**](ccritsec-unlock.md) pour déverrouiller la section critique. Vous pouvez effectuer plusieurs appels à la méthode **Lock** sur le même thread. Veillez à appeler **Unlock** un nombre de fois correspondant.

Si l’objet est déjà verrouillé par un autre thread, la méthode **CCritSec :: Lock** est bloquée jusqu’à ce que l’objet soit libéré, ou jusqu’à ce qu’une exception de blocage possible se produise.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> </dl>

 

