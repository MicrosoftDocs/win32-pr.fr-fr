---
description: La méthode CheckVideoType vérifie si un format VIDEOINFO spécifié est compatible avec le format d’affichage.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Méthode CImageDisplay. CheckVideoType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535337"
---
# <a name="cimagedisplaycheckvideotype-method"></a>Méthode CImageDisplay. CheckVideoType

La `CheckVideoType` méthode vérifie si un format [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) spécifié est compatible avec le format d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckVideoType(
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

Retourne S \_ OK si le format est compatible, ou E \_ INVALIDARG dans le cas contraire.

## <a name="remarks"></a>Notes

Cette méthode retourne S \_ OK si le type proposé peut être affiché facilement sous les paramètres d’affichage actuels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




