---
description: La méthode Remove supprime l’objet CDeferredCommand de la file d’attente.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: CCmdQueue. Remove, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d0b0a4b416c5adb97b1a9efba1fbd5f6142b0e0fb761c6d4c0b277ac0cda7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954578"
---
# <a name="ccmdqueueremove-method"></a>CCmdQueue. Remove, méthode

La `Remove` méthode supprime l’objet [**CDeferredCommand**](cdeferredcommand.md) de la file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCmd* 
</dt> <dd>

Pointeur vers l’objet **CDeferredCommand** à supprimer de la file d’attente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne VFW \_ E \_ \_ introuvable si l’objet est introuvable dans la file d’attente. Sinon, retourne S \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




