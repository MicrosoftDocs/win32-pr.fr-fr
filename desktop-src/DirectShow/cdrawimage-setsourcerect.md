---
description: La méthode SetSourceRect définit le rectangle source.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Méthode CDrawImage. SetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999266"
---
# <a name="cdrawimagesetsourcerect-method"></a>Méthode CDrawImage. SetSourceRect

La `SetSourceRect` méthode définit le rectangle source.

## <a name="syntax"></a>Syntaxe


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Pointeur vers une structure **Rect** qui définit le nouveau rectangle source.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le filtre propriétaire doit appeler cette méthode si le rectangle source change ; par exemple, en réponse à un appel de [**IBasicVideo :: SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .

Validez le rectangle donné dans *pSourceRect* avant d’appeler cette méthode pour vous assurer qu’il ne s’étend pas au-delà de la taille de la vidéo native.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




