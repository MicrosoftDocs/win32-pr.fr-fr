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
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111314"
---
# <a name="cbaserendererinactive-method"></a>CBaseRenderer. inactive, méthode

La `Inactive` méthode est appelée lorsque l’état passe à arrêté.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CRendererInputPin :: inactive**](crendererinputpin-inactive.md) . Le filtre appelle la méthode [**CBaseRenderer :: ClearPendingSample**](cbaserenderer-clearpendingsample.md) pour libérer l’exemple le plus récent.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




