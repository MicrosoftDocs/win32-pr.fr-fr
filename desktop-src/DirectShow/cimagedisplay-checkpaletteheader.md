---
description: La méthode CheckPaletteHeader valide les entrées de palette dans une structure VIDEOINFO.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Méthode CImageDisplay. CheckPaletteHeader (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542711"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>Méthode CImageDisplay. CheckPaletteHeader

La `CheckPaletteHeader` méthode valide les entrées de palette dans une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInput* 
</dt> <dd>

Pointeur vers une structure **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si les entrées de palette sont valides, ou la **valeur false** dans le cas contraire.

## <a name="remarks"></a>Notes

Si le format d’image n’est pas en palette, la méthode vérifie que **biClrUsed** est égal à zéro. Dans le cas contraire, la méthode vérifie que l’indicateur de **bicompression** est bi \_ RGB ; **biClrImportant** n’est pas supérieur à **biClrUsed**; en raison de la profondeur de couleur, le nombre d’entrées de palette ne dépasse pas la valeur maximale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




