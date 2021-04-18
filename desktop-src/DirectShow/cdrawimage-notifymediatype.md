---
description: La méthode NotifyMediaType avertit l’objet CDrawImage du type de média actuel.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Méthode CDrawImage. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533197"
---
# <a name="cdrawimagenotifymediatype-method"></a>Méthode CDrawImage. NotifyMediaType

La `NotifyMediaType` méthode notifie l’objet **CDrawImage** du type de média actuel.

## <a name="syntax"></a>Syntaxe


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaType* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) , ou **null** pour effacer le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le filtre propriétaire doit appeler cette méthode chaque fois que le type de média change. En général, cela se produit lorsque le code confidentiel se connecte pour la première fois et après une modification de format dynamique.

L’objet **CDrawImage** stocke le pointeur *pMediaType* dans la variable membre **m \_ pMediaType** . Par conséquent, si l’appelant doit libérer l’objet **CMediaType** , il doit mettre à jour l’objet **CDrawImage** en appelant à nouveau cette méthode, soit avec un nouveau pointeur, soit avec une valeur **null** . Dans le cas contraire, une erreur peut se produire lorsque l’objet **CDrawImage** tente de faire référence à l’ancien pointeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




