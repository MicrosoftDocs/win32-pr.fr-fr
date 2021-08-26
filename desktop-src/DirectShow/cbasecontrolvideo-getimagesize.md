---
description: La méthode GetImageSize récupère les informations sur la taille de l’image vidéo.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Méthode CBaseControlVideo. GetImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a7e0d970e06186ced3800d4b1f4dc4190778834941b69ac17402e2294312b05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057059"
---
# <a name="cbasecontrolvideogetimagesize-method"></a>Méthode CBaseControlVideo. GetImageSize

La `GetImageSize` méthode récupère les informations sur la taille de l’image vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à remplir.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Pointeur vers la taille de la mémoire tampon vidéo.

</dd> <dt>

*pSourceRect* 
</dt> <dd>

Pointeur vers les dimensions du rectangle de la vidéo source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.



| Code de retour                                                                                  | Description                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>       | Échec.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argument non valide. Le format de données n’est pas compatible.<br/>           |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Une erreur inattendue s'est produite. Un ou plusieurs arguments ont la **valeur null**.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>       | Réussite.<br/>                                                       |



 

## <a name="remarks"></a>Remarques

Cette fonction membre est une fonction d’assistance utilisée pour créer des rendus d’image mémoire d’images DIB. Elle est appelée à partir de l’implémentation de la classe de base de [**CBaseControlVideo :: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) lorsqu’un paramètre _pVideoImage_ **null** est passé à cette fonction membre. Par conséquent, cette fonction membre construit et retourne une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , à l’aide des informations contenues dans *pBufferSize* et *pSourceRect*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




