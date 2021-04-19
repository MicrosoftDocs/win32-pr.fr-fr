---
description: La méthode DrawVideoImageHere dessine une image à partir d’un exemple de média dans un contexte de périphérique spécifié.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Méthode CDrawImage. DrawVideoImageHere (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535953"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>Méthode CDrawImage. DrawVideoImageHere

La `DrawVideoImageHere` méthode dessine une image à partir d’un exemple de média dans un contexte de périphérique spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* 
</dt> <dd>

Handle vers un contexte de périphérique (Device Context), où le dessin se produira.

</dd> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple qui contient l’image.

</dd> <dt>

*lprcSrc* 
</dt> <dd>

Pointeur désignant un rectangle source à utiliser pour le dessin. Si la **valeur est null**, le rectangle dans [**CDrawImage :: m \_ SourceRect**](cdrawimage-m-sourcerect.md) est utilisé.

</dd> <dt>

*lprcDst* 
</dt> <dd>

Pointeur désignant un rectangle cible à utiliser pour le dessin. Si la **valeur est null**, le rectangle dans [**CDrawImage :: m \_ TargetRect**](cdrawimage-m-targetrect.md) est utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




