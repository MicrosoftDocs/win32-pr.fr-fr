---
description: La méthode CheckHeaderValidity valide une structure BITMAPINFOHEADER. Cette méthode est utile uniquement pour les types RVB non compressés, pas pour les types compressés ou les types YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Méthode CImageDisplay. CheckHeaderValidity (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537961"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>Méthode CImageDisplay. CheckHeaderValidity

La `CheckHeaderValidity` méthode valide une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Cette méthode est utile uniquement pour les types RVB non compressés, pas pour les types compressés ou les types YUV.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInput* 
</dt> <dd>

Pointeur vers une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) contenant la structure **BITMAPINFOHEADER** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si **BITMAPINFOHEADER** est valide, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Cette méthode vérifie que les dimensions de l’image ne sont pas négatives ; le type de compression est BI \_ RGB ou \_ bits bi. les masques de couleur et de profondeur de couleur sont valides ; le membre **biplan** est égal à un et les membres **bisize** et **biSizeImage** sont corrects. Il recherche également des erreurs courantes dans les entrées de palette, le cas échéant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




