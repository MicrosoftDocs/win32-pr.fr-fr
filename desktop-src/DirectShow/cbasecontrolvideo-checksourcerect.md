---
description: Détermine si un rectangle source est valide.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Méthode CBaseControlVideo. CheckSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225033"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a>Méthode CBaseControlVideo. CheckSourceRect

Détermine si un rectangle source est valide.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Pointeur vers le rectangle source à vérifier.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne E \_ INVALIDARG s’il n’est pas valide ; sinon, retourne NOERROR (S \_ OK).

## <a name="remarks"></a>Notes

Cette fonction membre vérifie que le rectangle source demandé ne dépasse pas la vidéo source disponible. Les coordonnées gauche et supérieure ne peuvent pas être négatives, et la largeur et la hauteur ne peuvent pas dépasser la droite et la fin de la vidéo.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




