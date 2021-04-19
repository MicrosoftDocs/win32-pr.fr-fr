---
description: La méthode MakeIdentityPalette tente de créer une &\# 0034 ; palette d’identité, &\# 0034 ; définie comme une correspondance directe avec la palette sélectionnée dans le périphérique d’affichage.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Méthode CImagePalette. MakeIdentityPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539566"
---
# <a name="cimagepalettemakeidentitypalette-method"></a>Méthode CImagePalette. MakeIdentityPalette

La `MakeIdentityPalette` méthode tente de faire une « palette d’identité » définie comme un mappage direct à la palette sélectionnée dans le périphérique d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pEntry* 
</dt> <dd>

Pointeur vers un tableau d’entrées de palette.

</dd> <dt>

*iColours* 
</dt> <dd>

Nombre d’entrées de palette dans *pEntry*.

</dd> <dt>

*szDevice* 
</dt> <dd>

Pointeur vers une chaîne qui contient le nom du périphérique d’affichage, tel que retourné par la fonction GDI **EnumDisplayDevices** . Pour utiliser le périphérique d’affichage principal, attribuez la valeur **null** à ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite ou S \_ false en cas d’échec.

## <a name="remarks"></a>Notes

Cette méthode compare les entrées réservées de la palette système aux entrées correspondantes dans le tableau *pEntry* . Si elles correspondent exactement, la méthode définit l' \_ indicateur NOcollapse du PC dans les entrées de palette restantes (non réservées) dans *pEntry*. Cet indicateur empêche GDI de tenter de mapper les entrées de palette logique aux entrées de la palette système.

La méthode [**CImagePalette :: MakePalette**](cimagepalette-makepalette.md) appelle cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImagePalette, classe**](cimagepalette.md)
</dt> </dl>

 

 




