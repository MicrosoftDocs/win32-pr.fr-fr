---
description: La méthode GetVideoSize récupère la largeur et la hauteur de la vidéo native.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Méthode CBaseControlVideo. GetVideoSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49f58901ac362b5a03d069485ec4dbf74e22d4549dc628f26baa5c2bfa85234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056939"
---
# <a name="cbasecontrolvideogetvideosize-method"></a>Méthode CBaseControlVideo. GetVideoSize

La `GetVideoSize` méthode récupère la largeur et la hauteur de la vidéo native.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWidth* 
</dt> <dd>

Pointeur vers la largeur vidéo.

</dd> <dt>

*pHeight* 
</dt> <dd>

Pointeur désignant la hauteur de la vidéo.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




