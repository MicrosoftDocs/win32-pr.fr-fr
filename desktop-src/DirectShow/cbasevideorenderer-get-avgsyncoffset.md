---
description: La \_ méthode obtenir AvgSyncOffset récupère la moyenne du temps, en millisecondes, entre le moment où chaque trame est due et le moment où elle a été réellement restituée pour toutes les trames depuis le début de la diffusion en continu.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Méthode CBaseVideoRenderer.get_AvgSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545407"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a>Méthode CBaseVideoRenderer. obten \_ AvgSyncOffset

La `get_AvgSyncOffset` méthode récupère la moyenne du temps, en millisecondes, entre le moment où chaque trame est due et le moment où elle a été réellement restituée pour toutes les trames depuis le début de la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*piAvg* 
</dt> <dd>

Pointeur vers la moyenne du temps, comme décrit précédemment.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IQualProp :: obten \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




