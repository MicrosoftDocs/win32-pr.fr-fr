---
description: La \_ méthode obtenir gigue récupère l’écart-type de temps en millisecondes entre chaque frame et le suivant pour toutes les trames depuis le début de la diffusion en continu.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: Méthode CBaseVideoRenderer.get_Jitter (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac86cb74267c508a1f0f266455955e486d3686548202d2a524ee4a49288793e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052279"
---
# <a name="cbasevideorendererget_jitter-method"></a>CBaseVideoRenderer. obtient la \_ méthode d’instabilité

La `get_Jitter` méthode récupère l’écart type de temps, en millisecondes, entre chaque frame et le suivant pour tous les frames depuis le début de la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*piJitter* 
</dt> <dd>

Pointeur vers l’écart type du temps d’intertramage, en millisecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IQualProp :: obtient \_ Gigu**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




