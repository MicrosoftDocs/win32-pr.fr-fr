---
description: Utilise la fonction Microsoft Win32 SuspendThread pour interrompre l’opération d’un thread en cours d’exécution.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: CMsgThread. SuspendThread, méthode (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5242c8708c07beb85d297dff706dbe192f59f1f7b46b05eba7362c9f0182d52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915739"
---
# <a name="cmsgthreadsuspendthread-method"></a>CMsgThread. SuspendThread, méthode

Utilise la fonction Microsoft Win32 **SuspendThread** pour interrompre l’opération d’un thread en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la fonction membre est réussie, la valeur de retour est le nombre de suspensions précédent du thread. Si la fonction membre échoue, la valeur de retour est 0xFFFFFFFF. Pour obtenir des informations d’erreur étendues, appelez la fonction Microsoft Win32 **GetLastError** .

## <a name="remarks"></a>Remarques

Le thread client appelle cette fonction membre pour interrompre l’opération du thread de travail. Le thread de travail reste suspendu et ne s’exécute pas jusqu’à ce qu’un appel supplémentaire à la fonction membre [**CMsgThread :: ResumeThread**](cmsgthread-resumethread.md) soit effectué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




