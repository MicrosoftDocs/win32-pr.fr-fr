---
description: La \_ méthode obtenir DevSyncOffset récupère l’écart type du temps, en millisecondes, entre le moment où chaque image est due et le moment où elle a été réellement rendue, pour toutes les images depuis le début de la diffusion en continu.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Méthode CBaseVideoRenderer.get_DevSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8be41c3c7ae1be598b7c15f033510134cfa46890c904a79b4d979733e0ab6952
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052349"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a>Méthode CBaseVideoRenderer. obten \_ DevSyncOffset

La `get_DevSyncOffset` méthode récupère l’écart type du temps, en millisecondes, entre le moment où chaque image est due et le moment où elle a été réellement rendue, pour toutes les images depuis le début de la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*piDev* 
</dt> <dd>

Pointeur vers l’écart type de l’heure comme décrit précédemment.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IQualProp :: obten \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




