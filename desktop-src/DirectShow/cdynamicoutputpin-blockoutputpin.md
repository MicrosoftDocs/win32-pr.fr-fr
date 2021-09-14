---
description: La méthode BlockOutputPin bloque le code confidentiel.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Méthode CDynamicOutputPin. BlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224953"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>Méthode CDynamicOutputPin. BlockOutputPin

La `BlockOutputPin` méthode bloque le code confidentiel. Pendant que le code confidentiel est bloqué, la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) attend que le code confidentiel soit débloqué. L’État bloqué empêche la broche de sortie de remettre des échantillons, de modifier son format de sortie ou de se reconnecter.

## <a name="syntax"></a>Syntaxe


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) . N’appelez pas cette méthode si un thread de streaming utilise le code confidentiel, soit pour fournir des données, soit pour modifier la connexion. Pour vérifier si un thread de diffusion en continu utilise le code confidentiel, appelez la méthode [**CDynamicOutputPin :: StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




