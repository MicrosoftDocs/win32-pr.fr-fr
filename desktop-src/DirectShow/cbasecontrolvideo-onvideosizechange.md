---
description: Transmet un \_ \_ \_ message de modification de la taille de la vidéo ce au gestionnaire de graphes de filtre.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Méthode CBaseControlVideo. OnVideoSizeChange (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 689f6f14426d88270136d6cc3687f9e214b72d6e42e2af44f3d189510d61f327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076689"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>Méthode CBaseControlVideo. OnVideoSizeChange

Transmet un \_ \_ \_ message de modification de la taille de la vidéo ce au gestionnaire de graphes de filtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.



| Code de retour                                                                                   | Description               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>        | Échec.<br/>       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/> |



 

## <a name="remarks"></a>Remarques

Un convertisseur vidéo doit appeler cette fonction membre chaque fois que la taille de la vidéo est modifiée ; elle est généralement appelée une fois après la connexion initiale. Si le convertisseur peut prendre en charge des modifications de format dynamiques (de 320 x 240 à 160 x 120), il doit également l’appeler après chaque modification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




