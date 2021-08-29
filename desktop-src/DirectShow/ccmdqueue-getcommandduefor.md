---
description: La méthode GetCommandDueFor récupère une commande différée planifiée à une heure spécifiée.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Méthode CCmdQueue. GetCommandDueFor (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c290c5fac2bdf5fd0591a0b088189182638f6b796506361a288fadffe695a85d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757339"
---
# <a name="ccmdqueuegetcommandduefor-method"></a>Méthode CCmdQueue. GetCommandDueFor

La `GetCommandDueFor` méthode récupère une commande différée qui est planifiée à une heure spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStream* 
</dt> <dd>

Heure pour laquelle la commande est planifiée.

</dd> <dt>

*ppCmd* 
</dt> <dd>

Adresse d’un pointeur vers la commande différée à exécuter au moment spécifié dans le paramètre *tStream* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne VFW \_ E \_ \_ introuvable si aucune commande n’est due ; sinon, retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette fonction membre prend un temps de flux et retourne la commande différée planifiée à ce moment-là. Le décalage de temps de flux réel est calculé lors de l’exécution de la file d’attente de commandes. Les commandes restent en file d’attente jusqu’à l’exécution ou l’annulation. Cette fonction membre ne sera pas bloquée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




