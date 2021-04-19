---
description: La méthode ScaleSourceRect met à l’échelle un rectangle, s’il existe une différence entre la taille de la vidéo native et le format du type de média.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Méthode CDrawImage. ScaleSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528019"
---
# <a name="cdrawimagescalesourcerect-method"></a>Méthode CDrawImage. ScaleSourceRect

La `ScaleSourceRect` méthode met à l’échelle un rectangle, s’il existe une différence entre la taille de la vidéo native et le format du type de média.

## <a name="syntax"></a>Syntaxe


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSource* 
</dt> <dd>

Pointeur vers un rectangle non mis à l’échelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le rectangle mis à l’échelle.

## <a name="remarks"></a>Notes

Dans la classe **CDrawImage** , cette méthode retourne *pSource* sans aucune modification. Vous pouvez remplacer cette méthode si le filtre étire l’image vidéo entrante. Par exemple, la taille de la vidéo Native peut être 320 240, mais le type de média sur la broche d’entrée peut être 640 480. Dans ce cas, le filtre doit mettre à l’échelle le rectangle source d’un facteur de 2.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




