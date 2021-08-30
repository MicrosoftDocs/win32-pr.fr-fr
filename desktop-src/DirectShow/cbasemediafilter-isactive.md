---
description: La méthode IsActive détermine si l’objet est actif (en cours d’exécution ou en pause).
ms.assetid: 6531cf1f-e057-4094-9354-d5a32371c83c
title: CBaseMediaFilter. IsActive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2e59e15994f9a00f15538b95bf303195083bb364b5a34378ee32cd99bd88a50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084499"
---
# <a name="cbasemediafilterisactive-method"></a>CBaseMediaFilter. IsActive, méthode

La `IsActive` méthode détermine si l’objet est actif (en cours d’exécution ou en pause).

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsActive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’objet est en pause ou en cours d’exécution, ou **false** s’il est arrêté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




