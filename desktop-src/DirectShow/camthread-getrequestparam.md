---
description: La méthode GetRequestParam récupère la dernière requête.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Méthode CAMThread. GetRequestParam (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c511fdb68bb6ee9372530d9e19290342a57fbcc5817148613d20fd8afe029b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384919"
---
# <a name="camthreadgetrequestparam-method"></a>Méthode CAMThread. GetRequestParam

La `GetRequestParam` méthode récupère la dernière requête.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur du paramètre passé le plus récemment à la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




