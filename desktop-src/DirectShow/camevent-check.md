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
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111377"
---
# <a name="cameventcheck-method"></a>CAMEvent. Check, méthode

La `Check` méthode vérifie si l’événement est défini, sans blocage.

## <a name="syntax"></a>Syntaxe


```C++
BOOL Check();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="remarks"></a>Notes

Retourne la **valeur true** si l’événement est défini, ou **false** dans le cas contraire. Cette méthode appelle la méthode [**CAMEvent :: wait**](camevent-wait.md) avec un délai d’attente de zéro. Si l’objet est un événement à réinitialisation automatique, cette méthode réinitialise l’événement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMEvent, classe**](camevent.md)
</dt> </dl>

 

 




