---
description: La méthode GetDestinationPosition récupère le rectangle de destination dans une opération atomique.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Méthode CBaseControlVideo. GetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526901"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a>Méthode CBaseControlVideo. GetDestinationPosition

La `GetDestinationPosition` méthode récupère le rectangle de destination dans une opération atomique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pLeft* 
</dt> <dd>

Pointeur vers la coordonnée gauche du rectangle de destination.

</dd> <dt>

*pTop* 
</dt> <dd>

Pointeur vers la coordonnée supérieure du rectangle de destination.

</dd> <dt>

*pWidth* 
</dt> <dd>

Pointeur vers la largeur du rectangle de destination.

</dd> <dt>

*pHeight* 
</dt> <dd>

Pointeur vers la hauteur du rectangle de destination.

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

Cette fonction membre peut être utilisée à la place d’appels séparés aux fonctions membres [**CBaseControlVideo :: obten \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo :: obten \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo :: obten \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)et [**CBaseControlVideo :: obtient \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) . Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture. Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu. L’angle supérieur gauche de la fenêtre est coordonnée (0,0).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




