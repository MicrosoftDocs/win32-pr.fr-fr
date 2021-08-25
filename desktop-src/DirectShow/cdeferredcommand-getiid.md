---
description: La méthode GetIID récupère l’identificateur d’interface (IID) de l’interface sur laquelle la méthode sera exécutée.
ms.assetid: d6eb7d46-294a-4169-96d3-4bed02c48c08
title: Méthode CDeferredCommand. GetIID (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetIID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c5d43f04d8331f39e46e3223a64c09ad306585a1e29fd7627a0f50159d74cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910079"
---
# <a name="cdeferredcommandgetiid-method"></a>Méthode CDeferredCommand. GetIID

La `GetIID` méthode récupère l’identificateur d’interface (IID) de l’interface sur laquelle la méthode sera exécutée.

## <a name="syntax"></a>Syntaxe


```C++
REFIID GetIID();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’IID de l’interface sur laquelle la méthode sera exécutée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




