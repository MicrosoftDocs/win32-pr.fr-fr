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
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999322"
---
# <a name="cbaserendererendofstream-method"></a>Méthode CBaseRenderer. EndOfStream

La `EndOfStream` méthode notifie le filtre que la broche d’entrée a reçu une notification de fin de flux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit une notification de fin de flux.

Cette méthode affecte à l’indicateur [**CBaseRenderer :: m \_ BeOS**](cbaserenderer-m-beos.md) la **valeur true** et appelle la méthode [**CBaseRenderer :: SendEndOfStream**](cbaserenderer-sendendofstream.md) pour planifier un événement [**EC \_ Complete**](ec-complete.md) . Si le filtre est suspendu et en attente d’un exemple, cette méthode termine la transition d’État.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




