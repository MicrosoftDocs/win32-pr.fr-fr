---
description: La méthode MakePalette crée une palette logique à partir de la table de couleurs dans un format vidéo.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Méthode CImagePalette. MakePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239165"
---
# <a name="cimagepalettemakepalette-method"></a>Méthode CImagePalette. MakePalette

La `MakePalette` méthode crée une palette logique à partir de la table de couleurs dans un format vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) qui contient la table des couleurs.

</dd> <dt>

*szDevice* 
</dt> <dd>

Pointeur vers une chaîne qui contient le nom du périphérique d’affichage, tel que retourné par la fonction GDI **EnumDisplayDevices** . Pour utiliser le périphérique d’affichage principal, attribuez la valeur **null** à ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

En cas de réussite, retourne un handle vers la palette. Sinon, retourne la **valeur null**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImagePalette, classe**](cimagepalette.md)
</dt> </dl>

 

 




