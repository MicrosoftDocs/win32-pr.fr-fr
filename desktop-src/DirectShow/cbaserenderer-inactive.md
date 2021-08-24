---
description: La méthode inactive est appelée lorsque l’état passe à arrêté.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: CBaseRenderer. inactive, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e84afd1d4e4ffb013a2029f7d56a223f0aef2f019bc3beb11bd7bd6c202b88d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652399"
---
# <a name="cbaserendererinactive-method"></a>CBaseRenderer. inactive, méthode

La `Inactive` méthode est appelée lorsque l’état passe à arrêté.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CRendererInputPin :: inactive**](crendererinputpin-inactive.md) . Le filtre appelle la méthode [**CBaseRenderer :: ClearPendingSample**](cbaserenderer-clearpendingsample.md) pour libérer l’exemple le plus récent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




