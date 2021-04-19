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
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542289"
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

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IQualProp :: obten \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) . C’est ainsi que la page de propriétés récupère les données du planificateur. Les frames peuvent également être supprimés en amont sans que le convertisseur ne les visualise même.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




