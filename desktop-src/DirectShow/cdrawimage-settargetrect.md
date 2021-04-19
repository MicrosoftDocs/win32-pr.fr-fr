---
description: La méthode SetTargetRect définit le rectangle cible.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Méthode CDrawImage. SetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528710"
---
# <a name="cdrawimagesettargetrect-method"></a>Méthode CDrawImage. SetTargetRect

La `SetTargetRect` méthode définit le rectangle cible.

## <a name="syntax"></a>Syntaxe


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Pointeur vers une structure **Rect** qui définit le nouveau rectangle cible.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le filtre propriétaire doit appeler cette méthode si le rectangle source change ; par exemple, en réponse à un appel de [**IBasicVideo :: SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .

Avant d’appeler cette méthode, validez le rectangle fourni dans *pTargetRect*, par rapport à la fenêtre vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




