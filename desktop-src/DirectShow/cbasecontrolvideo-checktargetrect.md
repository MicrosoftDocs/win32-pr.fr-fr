---
description: La méthode CheckTargetRect détermine si un rectangle cible est valide.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Méthode CBaseControlVideo. CheckTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8444764af729f9536471a6a9df221cc118edb7d043112eb0b5351f45982d87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057319"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>Méthode CBaseControlVideo. CheckTargetRect

La `CheckTargetRect` méthode détermine si un rectangle cible est valide.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Pointeur vers le rectangle cible à vérifier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ INVALIDARG s’il n’est pas valide ; sinon, retourne NOERROR (S \_ OK).

## <a name="remarks"></a>Remarques

Cette fonction membre détermine si le rectangle cible demandé est valide. Étant donné que le rectangle de destination spécifie une position dans le client logique de la fenêtre, les coordonnées peuvent être négatives, même si la largeur et la hauteur globales ne peuvent pas être égales à zéro ou à une valeur négative.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




