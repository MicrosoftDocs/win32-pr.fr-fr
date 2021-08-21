---
description: La méthode ThrottleWait insère un point d’attente après chaque image.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Méthode CBaseVideoRenderer. ThrottleWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d61c0e934208ad72e678595ce668c6c7ff72eda3371c792b294df9f2d5915612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954748"
---
# <a name="cbasevideorendererthrottlewait-method"></a>Méthode CBaseVideoRenderer. ThrottleWait

La `ThrottleWait` méthode insère un point d’attente après chaque image.

## <a name="syntax"></a>Syntaxe


```C++
void ThrottleWait();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction membre attend pendant une période de temps obtenue à partir du membre de données **m \_ trThrottle** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




