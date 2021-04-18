---
description: La \_ méthode obtenir FramesDrawn récupère la \_ variable membre cFramesDrawn, en donnant le nombre de frames dessinés depuis le début de la diffusion en continu.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: Méthode CBaseVideoRenderer.get_FramesDrawn (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540388"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a>Méthode CBaseVideoRenderer. obten \_ FramesDrawn

La `get_FramesDrawn` méthode récupère la variable de membre **m \_ cFramesDrawn** , en donnant le nombre d’images dessinées depuis le début de la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcFramesDrawn* 
</dt> <dd>

Pointeur vers le nombre de frames dessinés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IQualProp :: obten \_ FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




