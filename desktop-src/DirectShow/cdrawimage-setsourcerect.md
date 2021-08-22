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
ms.openlocfilehash: a7c2ab656de8c3dd45a9543aafff64ac704f5d1e37a509781f767c4a3b2002f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384129"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le filtre propriétaire doit appeler cette méthode si le rectangle source change ; par exemple, en réponse à un appel de [**IBasicVideo :: SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .

Validez le rectangle donné dans *pSourceRect* avant d’appeler cette méthode pour vous assurer qu’il ne s’étend pas au-delà de la taille de la vidéo native.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




