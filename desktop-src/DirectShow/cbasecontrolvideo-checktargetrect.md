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
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542554"
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

## <a name="remarks"></a>Notes

Cette fonction membre détermine si le rectangle cible demandé est valide. Étant donné que le rectangle de destination spécifie une position dans le client logique de la fenêtre, les coordonnées peuvent être négatives, même si la largeur et la hauteur globales ne peuvent pas être égales à zéro ou à une valeur négative.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




