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
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111337"
---
# <a name="cbaserenderercheckready-method"></a>Méthode CBaseRenderer. CheckReady

La `CheckReady` méthode demande si une transition d’État est terminée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si la transition d’État est terminée, ou **false** si le filtre est toujours en cours de transition vers un nouvel État.

## <a name="requirements"></a>Spécifications



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

 

 




