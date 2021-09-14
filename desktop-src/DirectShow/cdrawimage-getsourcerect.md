---
description: La méthode GetSourceRect récupère le rectangle source actuel.
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: Méthode CDrawImage. GetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a2188a183794b94a5d6d05ac237f91dbcb5d6dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999272"
---
# <a name="cdrawimagegetsourcerect-method"></a>Méthode CDrawImage. GetSourceRect

La `GetSourceRect` méthode récupère le rectangle source actuel.

## <a name="syntax"></a>Syntaxe


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Pointeur vers une structure **Rect** qui reçoit le rectangle source.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




