---
description: La \_ méthode obtenir DestinationHeight récupère la hauteur du rectangle de destination actuel.
ms.assetid: 0001d98a-3a5c-47f1-8f5e-ce464d64131a
title: Méthode CBaseControlVideo.get_DestinationHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57e2eb96a36f0902dccbba052080fa27b5e61f96b852bf44bd1a238d59010145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057279"
---
# <a name="cbasecontrolvideoget_destinationheight-method"></a>Méthode CBaseControlVideo. obten \_ DestinationHeight

La `get_DestinationHeight` méthode récupère la hauteur du rectangle de destination actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DestinationHeight(
   long *pDestinationHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDestinationHeight* 
</dt> <dd>

Pointeur vers la hauteur de destination.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.



| Code de retour                                                                                           | Description                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>                | Échec.<br/>                                                              |
| <dl> <dt>**\_pointeur E**</dt> </dl>             | Argument de pointeur **null** .<br/>                                            |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Impossible d’effectuer l’opération, car les broches ne sont pas connectées.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Réussite.<br/>                                                              |



 

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ DestinationHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) .

Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où il sera joué. Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu. L’angle supérieur gauche de la fenêtre est coordonnée (0,0).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




