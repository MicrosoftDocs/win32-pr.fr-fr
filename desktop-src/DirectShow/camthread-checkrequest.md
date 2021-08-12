---
description: La méthode CheckRequest vérifie s’il existe une demande, sans blocage.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Méthode CAMThread. CheckRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 292f8a7fb1ed4f12ad558993d6b1932b2ddff4656bada5e0a89067bac1baa9c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662355"
---
# <a name="camthreadcheckrequest-method"></a>Méthode CAMThread. CheckRequest

La `CheckRequest` méthode vérifie s’il existe une demande, sans blocage.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pParam* 
</dt> <dd>

Pointeur vers une variable qui reçoit la valeur passée dans le dernier appel à la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** s’il y a une demande en attente, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette méthode est une version sans blocage de la méthode [**CAMThread :: GetRequest**](camthread-getrequest.md) .

Si un autre thread attend un appel à CallWorker, cette méthode récupère le paramètre de requête et retourne la **valeur true**. Sinon, elle retourne **false**. Si la méthode retourne la **valeur true**, appelez la méthode [**CAMThread :: reply**](camthread-reply.md) pour libérer le thread demandeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




