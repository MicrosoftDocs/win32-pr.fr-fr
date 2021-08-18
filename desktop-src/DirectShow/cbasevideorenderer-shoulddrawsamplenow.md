---
description: La méthode ShouldDrawSampleNow détermine si la vidéo doit être dessinée sans définir un lien de notification de minuterie avec l’horloge.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Méthode CBaseVideoRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3c0297ccf670de12380c5f02af2c67d6050bac29dd1fa7e7e89a6e6c7c20592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074684"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>Méthode CBaseVideoRenderer. ShouldDrawSampleNow

La `ShouldDrawSampleNow` méthode détermine si la vidéo doit être dessinée sans définir un lien de notification de minuterie avec l’horloge.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pour l’exemple.

</dd> <dt>

*ptrStart* 
</dt> <dd>

Pointeur vers l’heure de début du rendu.

</dd> <dt>

*ptrEnd* 
</dt> <dd>

Pointeur vers le temps d’arrêt du rendu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Retourne \_ la valeur OK pour signifier un dessin à la fois sans attendre, s \_ false pour signifier dessiner à l' *ptrStart*, ou une erreur pour signifier ne pas dessiner l’exemple ; autrement dit, vous pouvez l’ignorer pour gagner du temps.

## <a name="remarks"></a>Remarques

Cette fonction membre substitue [**CBaseRenderer :: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




