---
description: La méthode SetPopEvent spécifie un événement qui est signalé chaque fois que l’objet supprime un échantillon de la file d’attente.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Méthode COutputQueue. SetPopEvent (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006721"
---
# <a name="coutputqueuesetpopevent-method"></a>Méthode COutputQueue. SetPopEvent

La `SetPopEvent` méthode spécifie un événement qui est signalé chaque fois que l’objet supprime un échantillon de la file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hEvent* 
</dt> <dd>

Handle vers un événement créé par l’appelant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




