---
description: La fonction ContainsPalette détermine si une structure VIDEOINFOHEADER spécifiée contient une palette.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: ContainsPalette, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111229"
---
# <a name="containspalette-function"></a>ContainsPalette fonction)

La fonction **ContainsPalette** détermine si une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) spécifiée contient une palette.

## <a name="syntax"></a>Syntaxe


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si bitdepth est inférieur ou égal à 8 (**bmiHeader. biBitCount**), ou si le nombre d’index de couleurs est supérieur à zéro (**bmiHeader. biClrUsed**). Sinon, retourne **false** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




