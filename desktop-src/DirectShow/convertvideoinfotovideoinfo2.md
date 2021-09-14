---
description: La fonction ConvertVideoInfoToVideoInfo2 convertit un type de média qui utilise VIDEOINFOHEADER en un type qui utilise VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: ConvertVideoInfoToVideoInfo2, fonction (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111193"
---
# <a name="convertvideoinfotovideoinfo2-function"></a>ConvertVideoInfoToVideoInfo2 fonction)

La `ConvertVideoInfoToVideoInfo2` fonction convertit un type de média qui utilise [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en un type qui utilise [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) à convertir. La structure doit avoir le type de format \_ videoinfo.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette fonction alloue une nouvelle structure **VIDEOINFOHEADER2** , y copie les membres de la structure **VIDEOINFOHEADER** , puis remplace l’ancienne structure par la nouvelle structure dans le bloc de format du type de média.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




