---
description: La méthode reply répond à une demande.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: CAMThread. Reply, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094913"
---
# <a name="camthreadreply-method"></a>CAMThread. Reply, méthode

La `Reply` méthode répond à une demande.

## <a name="syntax"></a>Syntaxe


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dw* 
</dt> <dd>

Valeur à retourner dans la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode CallWorker se bloque jusqu’à ce que cette méthode soit appelée. Le paramètre *DW* fournit la valeur de retour pour CallWorker. Appelez cette méthode dans votre procédure de thread après avoir récupéré une demande, pour libérer le thread demandeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




