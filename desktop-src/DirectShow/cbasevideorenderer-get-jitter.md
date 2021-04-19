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
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542288"
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

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IQualProp :: obtient \_ Gigu**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




