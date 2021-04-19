---
description: La méthode SetDefaultDestinationPosition rétablit le convertisseur à l’aide de la position de destination par défaut (en général, la zone cliente de la fenêtre entière).
ms.assetid: 228259d7-2f1f-4528-8c8a-d20d7542523c
title: Méthode CBaseControlVideo. SetDefaultDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a959f462d410b83588fb1a8df87cebffd879d8ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528646"
---
# <a name="cbasecontrolvideosetdefaultdestinationposition-method"></a>Méthode CBaseControlVideo. SetDefaultDestinationPosition

La `SetDefaultDestinationPosition` méthode rétablit le convertisseur à l’aide de la position de destination par défaut (en général, la zone cliente de la fenêtre entière).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDefaultDestinationPosition();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.



| Code de retour                                                                                           | Description                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>                | Échec.<br/>                                                              |
| <dl> <dt>**NOERROR**</dt> </dl>                | Opération réussie.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Impossible d’effectuer l’opération, car les broches ne sont pas connectées.<br/> |



 

## <a name="remarks"></a>Notes

Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture. Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu. L’angle supérieur gauche de la fenêtre est coordonnée (0,0).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




