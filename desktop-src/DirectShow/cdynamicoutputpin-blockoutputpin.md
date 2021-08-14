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
ms.openlocfilehash: 9dc1f4cdafd732821398ee04e127c0525798dd6cc02f67f8af5d977b195a6a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983359"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>Méthode CDynamicOutputPin. BlockOutputPin

La `BlockOutputPin` méthode bloque le code confidentiel. Pendant que le code confidentiel est bloqué, la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) attend que le code confidentiel soit débloqué. L’État bloqué empêche la broche de sortie de remettre des échantillons, de modifier son format de sortie ou de se reconnecter.

## <a name="syntax"></a>Syntaxe


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) . N’appelez pas cette méthode si un thread de streaming utilise le code confidentiel, soit pour fournir des données, soit pour modifier la connexion. Pour vérifier si un thread de diffusion en continu utilise le code confidentiel, appelez la méthode [**CDynamicOutputPin :: StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




