---
description: La méthode PreparePalette configure une palette, en fonction d’un type de média à partir du filtre propriétaire.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Méthode CImagePalette. PreparePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525151"
---
# <a name="cimagepalettepreparepalette-method"></a>Méthode CImagePalette. PreparePalette

La `PreparePalette` méthode Configure une palette, en fonction d’un type de média à partir du filtre propriétaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pmtNew* 
</dt> <dd>

Pointeur vers le nouveau type de média. Le bloc de format doit être une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

</dd> <dt>

*pmtOld* 
</dt> <dd>

Pointeur vers l’ancien type de média. Si le type de média est défini pour la première fois, ce paramètre peut être un type vide sans bloc de format. Dans le cas contraire, le bloc de format doit être une structure **VIDEOINFOHEADER** .

</dd> <dt>

*szDevice* 
</dt> <dd>

Pointeur vers une chaîne qui contient le nom du périphérique d’affichage, tel que retourné par la fonction GDI **EnumDisplayDevices** . Pour utiliser le périphérique d’affichage principal, attribuez la valeur **null** à ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ si la palette a été mise à jour ou \_ false si elle n’a pas changé.

## <a name="remarks"></a>Notes

Si la palette doit être mise à jour, cette méthode effectue les actions suivantes :

-   Appelle [**CImagePalette :: MakePalette**](cimagepalette-makepalette.md) pour créer une nouvelle palette logique.
-   Envoie un événement de [**\_ \_ modification de palette EC**](ec-palette-changed.md) au gestionnaire de graphes de filtre.
-   Appelle [**CBaseWindow :: SetPalette**](cbasewindow-setpalette.md) sur l’objet **CBaseWindow** .
-   Appelle [**CDrawImage :: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) sur l’objet **CDrawImage** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImagePalette, classe**](cimagepalette.md)
</dt> </dl>

 

 




