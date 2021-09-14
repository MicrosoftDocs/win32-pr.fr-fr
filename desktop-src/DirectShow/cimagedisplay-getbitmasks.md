---
description: La méthode GetBitMasks récupère les masques de couleur pour un format VIDEOINFO spécifié.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Méthode CImageDisplay. GetBitMasks (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094821"
---
# <a name="cimagedisplaygetbitmasks-method"></a>Méthode CImageDisplay. GetBitMasks

La `GetBitMasks` méthode récupère les masques de couleur pour un format [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) spécifié.

## <a name="syntax"></a>Syntaxe


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Pointeur vers la structure **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un tableau de trois valeurs **DWORD** .

## <a name="remarks"></a>Notes

Si le membre de **décompression** est bi-champs \_ , la méthode retourne un pointeur vers les masques de couleur qui sont fournis dans le membre **dwBitMasks** . Si le membre de **bicompression** est bi \_ RGB, la méthode retourne les masques de couleur qui correspondent à la profondeur de bit. Si la méthode échoue (par exemple, la profondeur du bit est inférieure à 16), la méthode retourne le tableau {0,0,0} .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




