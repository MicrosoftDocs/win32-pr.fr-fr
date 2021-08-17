---
description: La \_ méthode obtenir FramesDroppedInRenderer récupère le nombre de frames supprimés par le convertisseur.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Méthode CBaseVideoRenderer.get_FramesDroppedInRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21bd2e9c2f9edb50ca3800c95b59ba19fd91674d5ef343cf35842380ce617978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016757"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a>Méthode CBaseVideoRenderer. obten \_ FramesDroppedInRenderer

La `get_FramesDroppedInRenderer` méthode récupère le nombre de frames supprimés par le convertisseur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcFramesDropped* 
</dt> <dd>

Pointeur vers le nombre de frames supprimés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IQualProp :: obten \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) . C’est ainsi que la page de propriétés récupère les données du planificateur. Les frames peuvent également être supprimés en amont sans que le convertisseur ne les visualise même.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




