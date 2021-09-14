---
description: La fonction GetBitmapSize calcule le nombre d’octets requis par une image bitmap indépendante du périphérique (DIB, Device-Independent Bitmap). Cette fonction appelle simplement la macro DIBSIZE.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: GetBitmapSize, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999140"
---
# <a name="getbitmapsize-function"></a>GetBitmapSize fonction)

La `GetBitmapSize` fonction calcule le nombre d’octets requis par une image bitmap indépendante du périphérique (DIB, Device-Independent Bitmap). Cette fonction appelle simplement la macro [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) .

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pHeader* 
</dt> <dd>

Pointeur vers une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la taille en octets.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




