---
description: La méthode GetDueCommand récupère un pointeur vers la commande suivante qui est due.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Méthode CCmdQueue. GetDueCommand (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6e7c8d133537dc2b185c755e65f3a4febbee762c5c2306de37ad0c627434df7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016427"
---
# <a name="ccmdqueuegetduecommand-method"></a>Méthode CCmdQueue. GetDueCommand

La `GetDueCommand` méthode récupère un pointeur vers la commande suivante qui est due.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppCmd* 
</dt> <dd>

Adresse d’un pointeur vers la commande différée.

</dd> <dt>

*msTimeout* 
</dt> <dd>

Délai d’attente avant l’expiration du délai d’attente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ Abort si un dépassement de délai se produit. Retourne S \_ OK en cas de réussite ; sinon, retourne une erreur. Retourne un objet qui a été incrémenté à l’aide de **IUnknown :: AddRef**.

## <a name="remarks"></a>Remarques

Cette fonction membre se bloque jusqu’à ce qu’une commande en attente soit due. La fonction membre se bloque pendant la durée, en millisecondes, spécifiée dans le paramètre *msTimeout* . Les commandes au moment du flux sont dues uniquement entre les fonctions membres [**CCmdQueue :: Run**](ccmdqueue-run.md) et [**CCmdQueue :: EndRun**](ccmdqueue-endrun.md) . La commande reste en file d’attente jusqu’à l’exécution ou à l’annulation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




