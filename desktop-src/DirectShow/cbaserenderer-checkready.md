---
description: La méthode CheckReady interroge si une transition d’État est terminée.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Méthode CBaseRenderer. CheckReady (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a1fac55eba92141ac8174b30ed2dcbc4685ba250b7bb21236432bb998b3b5e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043949"
---
# <a name="cbaserenderercheckready-method"></a>Méthode CBaseRenderer. CheckReady

La `CheckReady` méthode demande si une transition d’État est terminée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la transition d’État est terminée, ou **false** si le filtre est toujours en cours de transition vers un nouvel État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer :: nochapy**](cbaserenderer-notready.md)
</dt> <dt>

[**CBaseRenderer :: prêt**](cbaserenderer-ready.md)
</dt> </dl>

 

 




