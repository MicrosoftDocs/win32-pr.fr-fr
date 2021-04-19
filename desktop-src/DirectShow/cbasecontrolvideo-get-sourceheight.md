---
description: La \_ méthode obtenir SourceHeight récupère la hauteur du rectangle source actuel.
ms.assetid: bf727cf6-9143-41f0-a482-782a4178ea92
title: Méthode CBaseControlVideo.get_SourceHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b724f63907c8372867095b059ff728b4c646df21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542342"
---
# <a name="cbasecontrolvideoget_sourceheight-method"></a>Méthode CBaseControlVideo. obten \_ SourceHeight

La `get_SourceHeight` méthode récupère la hauteur du rectangle source actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SourceHeight(
   long *pSourceHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSourceHeight* 
</dt> <dd>

Pointeur vers la hauteur du rectangle source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.



| Code de retour                                                                                           | Description                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>                | Échec.<br/>                                                              |
| <dl> <dt>**\_pointeur E**</dt> </dl>             | Argument de pointeur **null** .<br/>                                            |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Impossible d’effectuer l’opération, car les broches ne sont pas connectées.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Opération réussie.<br/>                                                              |



 

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ SourceHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) .

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

 

 




