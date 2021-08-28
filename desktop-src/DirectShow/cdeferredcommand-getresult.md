---
description: La méthode GetResult récupère la liste d’arguments résultante, s’il en existe une.
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: CDeferredCommand. GetResult, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2176d6787bd520517cccbf484bdf6642921d499aaeb97c2917d64fa148323b66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076419"
---
# <a name="cdeferredcommandgetresult-method"></a>CDeferredCommand. GetResult, méthode

La `GetResult` méthode récupère la liste d’arguments résultante, le cas échéant.

## <a name="syntax"></a>Syntaxe


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers un **Variant** contenant la liste d’arguments de la méthode, si elle existe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




