---
description: La méthode OnRenderEnd effectue un lissage pour les cas où le temps de rendu varie en raison des interruptions.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Méthode CBaseVideoRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523475"
---
# <a name="cbasevideorendereronrenderend-method"></a>Méthode CBaseVideoRenderer. OnRenderEnd

La `OnRenderEnd` méthode effectue un lissage pour les cas où le temps de rendu varie en raison des interruptions.

## <a name="syntax"></a>Syntaxe


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’exemple de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction membre doit être appelée juste après le dessin d’une image.

Cette fonction membre substitue [**CBaseRenderer :: OnRenderEnd**](cbaserenderer-onrenderend.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




