---
description: 'Utilise la fonction Win32 ResumeThread de Microsoft pour poursuivre l’opération du thread de travail après un appel précédent à la fonction membre CMsgThread :: SuspendThread.'
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: CMsgThread. ResumeThread, méthode (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed9e2ea546f2c14ceea4f3766db68c1d70ce44ab4dda542315bf7dd30a2d715d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915829"
---
# <a name="cmsgthreadresumethread-method"></a>CMsgThread. ResumeThread, méthode

Utilise la fonction Win32 **ResumeThread** de Microsoft pour poursuivre l’opération du thread de travail après un appel précédent à la fonction membre [**CMsgThread :: SuspendThread**](cmsgthread-suspendthread.md) .

## <a name="syntax"></a>Syntaxe


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la fonction membre est réussie, la valeur de retour est le nombre de suspensions précédent du thread. Si la fonction membre échoue, la valeur de retour est 0xFFFFFFFF. Pour obtenir des informations d’erreur étendues, appelez la fonction Microsoft Win32 **GetLastError** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




