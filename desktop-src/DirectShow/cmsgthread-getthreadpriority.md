---
description: Utilise la fonction Microsoft Win32 GetThreadPriority pour récupérer la priorité du thread de travail actuel.
ms.assetid: a9db15cf-2c22-4c61-a817-20af5ade434b
title: Méthode CMsgThread. GetThreadPriority (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24f102a315ebb20bc9c17ed6a7bab6bae2e503e13aa62bd11883c7a8290702ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915909"
---
# <a name="cmsgthreadgetthreadpriority-method"></a>Méthode CMsgThread. GetThreadPriority

Utilise la fonction Microsoft Win32 **GetThreadPriority** pour récupérer la priorité du thread de travail actuel.

## <a name="syntax"></a>Syntaxe


```C++
int GetThreadPriority();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la priorité de thread sous la forme d’un entier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




