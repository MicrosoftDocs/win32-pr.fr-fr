---
description: La méthode GetCurrentImage récupère une copie de l’image actuelle au niveau du convertisseur.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Méthode CBaseControlVideo. GetCurrentImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 782f540959b134f7ca00c2bc674a64ce60ccb4f6ddf166c79f2597e582ca9fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087569"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>Méthode CBaseControlVideo. GetCurrentImage

La `GetCurrentImage` méthode récupère une copie de l’image actuelle au niveau du convertisseur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Pointeur vers la taille de la mémoire tampon de sortie.

</dd> <dt>

*pVideoImage* 
</dt> <dd>

Pointeur vers la mémoire tampon de sortie de l’image.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.



| Code de retour                                                                                        | Description                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>             | Échec.<br/>                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>       | Argument non valide.<br/>                                                      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>      | Mémoire insuffisante. Retourné lorsque le paramètre *pVideoInfo* a la **valeur null**.<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | Réussite.<br/>                                                               |
| <dl> <dt>**VFW \_ E \_ non \_ suspendu**</dt> </dl> | L’opération n’a pas pu être effectuée car le filtre n’est pas suspendu.<br/> |



 

## <a name="remarks"></a>Remarques

Cette fonction membre récupère l’image à partir de l’exemple et la copie dans la mémoire tampon de sortie. La section de la vidéo copiée dans la mémoire tampon de sortie reflète le rectangle source défini par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Elle ne reflète pas le rectangle de destination.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




