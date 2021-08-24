---
description: La méthode Insert ajoute un objet CDeferredCommand à la file d’attente.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: CCmdQueue. Insert, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90e2bab4a3545e8a02315155ad4a477511ecf961c93a511ccba268b7fde7dd0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757319"
---
# <a name="ccmdqueueinsert-method"></a>CCmdQueue. Insert, méthode

La `Insert` méthode ajoute un objet [**CDeferredCommand**](cdeferredcommand.md) à la file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCmd* 
</dt> <dd>

Pointeur vers l’objet **CDeferredCommand** à ajouter à la file d’attente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK dans l’implémentation par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




