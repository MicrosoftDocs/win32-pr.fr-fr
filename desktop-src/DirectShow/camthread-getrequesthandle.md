---
description: 'La méthode GetRequestHandle récupère un handle vers l’événement signalé par la méthode CAMThread :: CallWorker.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Méthode CAMThread. GetRequestHandle (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fa1be333ff35821f187cea980746c6b729a05c12e2103f4465bb44bbcc6f9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652589"
---
# <a name="camthreadgetrequesthandle-method"></a>Méthode CAMThread. GetRequestHandle

La `GetRequestHandle` méthode récupère un handle vers l’événement signalé par la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .

## <a name="syntax"></a>Syntaxe


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un handle d’événement.

## <a name="remarks"></a>Remarques

La classe CAMEvent conserve un événement de réinitialisation manuelle privé, qui est défini par CallWorker et réinitialisé par la méthode [**CAMThread :: reply**](camthread-reply.md) .

Si vous appelez une fonction telle que WaitForMultipleObjects, utilisez GetRequestHandle pour récupérer le handle d’événement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




