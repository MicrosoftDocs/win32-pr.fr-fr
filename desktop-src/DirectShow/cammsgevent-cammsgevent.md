---
description: Méthode constructeur CAMMsgEvent. CAMMsgEvent.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Constructeur CAMMsgEvent. CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fc2eeaab10134022388e6a57628d1c3c5a87fc0e0a443efab19f016a1e5c27b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955498"
---
# <a name="cammsgeventcammsgevent-constructor"></a>Constructeur CAMMsgEvent. CAMMsgEvent

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Si le constructeur échoue, ce paramètre reçoit un code d’erreur. Si cela se produit, l’état de l’objet n’est pas valide.

Pour la compatibilité descendante avec les versions antérieures de strmbase. lib, la valeur par défaut de ce paramètre est **null**. Toutefois, le passage d’une valeur non **null** est préférable, afin que l’appelant puisse vérifier l’état de l’objet.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMMsgEvent, classe**](cammsgevent.md)
</dt> </dl>

 

 




