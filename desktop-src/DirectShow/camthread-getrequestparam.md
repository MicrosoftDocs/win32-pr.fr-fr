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
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094926"
---
# <a name="camthreadgetrequestparam-method"></a>Méthode CAMThread. GetRequestParam

La `GetRequestParam` méthode récupère la dernière requête.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la valeur du paramètre passé le plus récemment à la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




