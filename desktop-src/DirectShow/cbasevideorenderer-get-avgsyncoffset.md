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
ms.openlocfilehash: 4550445d0a2596edcb9d76b88b371eb060257b29730a386c4f9444dae2624b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526499"
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

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IQualProp :: obten \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




