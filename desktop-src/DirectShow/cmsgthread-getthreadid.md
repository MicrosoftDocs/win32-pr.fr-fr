---
description: Récupère l’identificateur du thread.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Méthode CMsgThread. GetThreadID (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3b0837a7f050f09794b06e490f45012e0704e187b02668cd2af2a5bf8edf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214098"
---
# <a name="cmsgthreadgetthreadid-method"></a>Méthode CMsgThread. GetThreadID

Récupère l’identificateur du thread.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne le membre de données privées de l' **\_ ThreadID m** .

## <a name="remarks"></a>Remarques

Cette fonction retourne l’identificateur Microsoft Win32 pour le thread de travail. Vous pouvez appeler cette fonction membre sur le thread de travail ou un thread client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




