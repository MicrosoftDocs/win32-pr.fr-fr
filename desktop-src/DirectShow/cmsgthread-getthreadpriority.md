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
ms.openlocfilehash: 3c9716b43ccc314ba487d982e0c1685960593f95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542267"
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
| En-tête<br/>  | <dl> <dt>Msgthrd. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




