---
description: La méthode SetDestinationPosition définit le rectangle de destination de la vidéo.
ms.assetid: 397e90ea-7535-4cac-9f47-7a93737b1e3a
title: Méthode CBaseControlVideo. SetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798a65c44dd490587e3ad46fcae2c61a03986df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526892"
---
# <a name="cbasecontrolvideosetdestinationposition-method"></a>Méthode CBaseControlVideo. SetDestinationPosition

La `SetDestinationPosition` méthode définit le rectangle de destination de la vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDestinationPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Left* 
</dt> <dd>

Nouvelle coordonnée gauche.

</dd> <dt>

*Top* 
</dt> <dd>

Nouvelle coordonnée supérieure.

</dd> <dt>

*Width* 
</dt> <dd>

Nouvelle largeur.

</dd> <dt>

*Height* 
</dt> <dd>

Nouvelle hauteur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.



| Code de retour                                                                                           | Description                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>                | Échec.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Argument non valide.<br/>                                                     |
| <dl> <dt>**\_pointeur E**</dt> </dl>             | Argument de pointeur **null** .<br/>                                            |
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

 

 




