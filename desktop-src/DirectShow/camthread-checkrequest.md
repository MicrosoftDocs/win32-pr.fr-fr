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
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094958"
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

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** s’il y a une demande en attente, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Cette méthode est une version sans blocage de la méthode [**CAMThread :: GetRequest**](camthread-getrequest.md) .

Si un autre thread attend un appel à CallWorker, cette méthode récupère le paramètre de requête et retourne la **valeur true**. Sinon, elle retourne **false**. Si la méthode retourne la **valeur true**, appelez la méthode [**CAMThread :: reply**](camthread-reply.md) pour libérer le thread demandeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




