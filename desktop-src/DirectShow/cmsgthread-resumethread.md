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
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532014"
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
| En-tête<br/>  | <dl> <dt>Msgthrd. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




