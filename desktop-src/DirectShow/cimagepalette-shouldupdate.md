---
description: La méthode ShouldUpdate détermine s’il est nécessaire de créer une nouvelle palette.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Méthode CImagePalette. ShouldUpdate (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543784"
---
# <a name="cimagepaletteshouldupdate-method"></a>Méthode CImagePalette. ShouldUpdate

La `ShouldUpdate` méthode détermine s’il est nécessaire de créer une nouvelle palette.

## <a name="syntax"></a>Syntaxe


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNewInfo* 
</dt> <dd>

Pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenant la nouvelle table de couleurs.

</dd> <dt>

*pOldInfo* 
</dt> <dd>

Pointeur vers une structure **VIDEOINFOHEADER** contenant l’ancienne table de couleurs. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la palette doit être mise à jour, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

-   Si aucune structure **VIDEOINFOHEADER** ne contient de table de couleurs, la méthode retourne **false**.
-   Si une seule structure contient une table de couleurs ou si *pOldInfo* a la **valeur null**, la méthode retourne **true**.
-   Si les deux structures contiennent des tables de couleurs et que les entrées de couleur correspondent, la méthode retourne la **valeur false**.
-   Si les deux structures contiennent des tables de couleurs, mais que les entrées de couleur ne correspondent pas, la méthode retourne la **valeur true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImagePalette, classe**](cimagepalette.md)
</dt> </dl>

 

 




