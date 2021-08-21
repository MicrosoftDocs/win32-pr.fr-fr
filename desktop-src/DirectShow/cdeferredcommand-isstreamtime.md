---
description: La méthode IsStreamTime spécifie si la commande doit être exécutée au moment du flux ou de la présentation.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: Méthode CDeferredCommand. IsStreamTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82c541220a2b89ecdd23e4676175f4c7b2aacd93aac008546349b38e7bc2455a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657202"
---
# <a name="cdeferredcommandisstreamtime-method"></a>Méthode CDeferredCommand. IsStreamTime

La `IsStreamTime` méthode spécifie si la commande doit être exécutée au moment du flux ou de la présentation.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** s’il est défini sur Time Stream. Sinon, retourne **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




