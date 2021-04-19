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
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537508"
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
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




