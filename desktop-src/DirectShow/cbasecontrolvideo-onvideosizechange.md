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
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532911"
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



 

## <a name="remarks"></a>Notes

Un convertisseur vidéo doit appeler cette fonction membre chaque fois que la taille de la vidéo est modifiée ; elle est généralement appelée une fois après la connexion initiale. Si le convertisseur peut prendre en charge des modifications de format dynamiques (de 320 x 240 à 160 x 120), il doit également l’appeler après chaque modification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




