---
description: La méthode EndOfStream avertit le filtre que la broche d’entrée a reçu une notification de fin de flux.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Méthode CBaseRenderer. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ff047865aa4f52dee6c03411cddb0c957327851f0f6ca1b7a03f0b6adaacfe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822730"
---
# <a name="cbaserendererendofstream-method"></a>Méthode CBaseRenderer. EndOfStream

La `EndOfStream` méthode notifie le filtre que la broche d’entrée a reçu une notification de fin de flux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit une notification de fin de flux.

Cette méthode affecte à l’indicateur [**CBaseRenderer :: m \_ BeOS**](cbaserenderer-m-beos.md) la **valeur true** et appelle la méthode [**CBaseRenderer :: SendEndOfStream**](cbaserenderer-sendendofstream.md) pour planifier un événement [**EC \_ Complete**](ec-complete.md) . Si le filtre est suspendu et en attente d’un exemple, cette méthode termine la transition d’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




