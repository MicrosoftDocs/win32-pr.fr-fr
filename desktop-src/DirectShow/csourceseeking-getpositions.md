---
description: 'La méthode GetPositions récupère la position actuelle et la position d’arrêt. Cette méthode implémente la méthode IMediaSeeking :: GetPositions.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Méthode CSourceSeeking. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b6f52d8d8b30a28d942d4395a465b9c7c49d0a23020ad212c81eb170d20ca0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073334"
---
# <a name="csourceseekinggetpositions-method"></a>Méthode CSourceSeeking. GetPositions

La `GetPositions` méthode récupère la position actuelle et la position d’arrêt. Cette méthode implémente la méthode [**IMediaSeeking :: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCurrent* 
</dt> <dd>

Pointeur vers une variable qui reçoit la position de début.

</dd> <dt>

*pStop* 
</dt> <dd>

Pointeur vers une variable qui reçoit la position d’arrêt.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Pour le paramètre *pCurrent* , cette méthode retourne la valeur de la variable membre [**CSourceSeeking :: m \_ rtStart**](csourceseeking-m-rtstart.md) , qui représente l’heure de recherche la plus récente, et non la position de diffusion en continu actuelle. Toutefois, lorsqu’une application appelle **IMediaSeeking :: GetPositions** via le gestionnaire de graphique de filtre, les valeurs proviennent généralement d’un filtre de convertisseur, et non d’un filtre source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




