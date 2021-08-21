---
description: La méthode CheckBitFields valide les masques de couleur dans une structure VIDEOINFO.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Méthode CImageDisplay. CheckBitFields (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44e60b6693dde202cd458cd09495dce9e4bea52ed96a468a8d3dcb6b2370eac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074173"
---
# <a name="cimagedisplaycheckbitfields-method"></a>Méthode CImageDisplay. CheckBitFields

La `CheckBitFields` méthode valide les masques de couleur dans une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL CheckBitFields(
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

Retourne la **valeur true** si les masques de couleur sont valides, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette méthode vérifie que le masque de couleur pour chaque composant de couleur est compris entre un et huit bits et que chaque masque de couleur est une séquence contiguë de bits. Appelez cette méthode uniquement lorsque le membre de bicompression est défini sur les champs de **décompression** bi \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




