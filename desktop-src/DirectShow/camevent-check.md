---
description: La méthode check vérifie si l’événement est défini, sans blocage.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: CAMEvent. Check, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a961d7df45ddac7ade5e39f91c1aed56609ce2d2eeb8e7423799c9a4903884e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955538"
---
# <a name="cameventcheck-method"></a>CAMEvent. Check, méthode

La `Check` méthode vérifie si l’événement est défini, sans blocage.

## <a name="syntax"></a>Syntaxe


```C++
BOOL Check();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Retourne la **valeur true** si l’événement est défini, ou **false** dans le cas contraire. Cette méthode appelle la méthode [**CAMEvent :: wait**](camevent-wait.md) avec un délai d’attente de zéro. Si l’objet est un événement à réinitialisation automatique, cette méthode réinitialise l’événement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMEvent, classe**](camevent.md)
</dt> </dl>

 

 




