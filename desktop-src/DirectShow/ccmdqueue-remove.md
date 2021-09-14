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
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012295"
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

## <a name="return-value"></a>Valeur de retour

Retourne VFW \_ E \_ \_ introuvable si l’objet est introuvable dans la file d’attente. Sinon, retourne S \_ OK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




