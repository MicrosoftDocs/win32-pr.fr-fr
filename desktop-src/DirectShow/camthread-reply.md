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
ms.openlocfilehash: 9783703d711800b8002aa0372292349d83620eafb097be2256ffde6ab2c91c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662365"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La méthode CallWorker se bloque jusqu’à ce que cette méthode soit appelée. Le paramètre *DW* fournit la valeur de retour pour CallWorker. Appelez cette méthode dans votre procédure de thread après avoir récupéré une demande, pour libérer le thread demandeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




