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
ms.openlocfilehash: c7897e14aec690ec67451fe868b5352e99c9bd513c8c182a47556fe075cffb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916029"
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

## <a name="remarks"></a>Remarques

-   Si aucune structure **VIDEOINFOHEADER** ne contient de table de couleurs, la méthode retourne **false**.
-   Si une seule structure contient une table de couleurs ou si *pOldInfo* a la **valeur null**, la méthode retourne **true**.
-   Si les deux structures contiennent des tables de couleurs et que les entrées de couleur correspondent, la méthode retourne la **valeur false**.
-   Si les deux structures contiennent des tables de couleurs, mais que les entrées de couleur ne correspondent pas, la méthode retourne la **valeur true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImagePalette, classe**](cimagepalette.md)
</dt> </dl>

 

 




