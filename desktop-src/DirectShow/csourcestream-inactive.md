---
description: 'La méthode inactive indique au code confidentiel que le filtre n’est plus actif. Cette méthode remplace la méthode CBasePin :: inactive. Si le thread de diffusion en continu est actif, cette méthode l’arrête et attend que le thread se termine.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Méthode CSourceStream. inactive (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9d9424f4299d7a07ad98010846fa917307bd38eead028b4b8c38c40e2284c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687369"
---
# <a name="csourcestreaminactive-method"></a>CSourceStream. inactive, méthode

La `Inactive` méthode notifie le code confidentiel que le filtre n’est plus actif. Cette méthode remplace la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) . Si le thread de diffusion en continu est actif, cette méthode l’arrête et attend que le thread se termine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




