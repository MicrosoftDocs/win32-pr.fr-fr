---
description: 'Méthode CBasePin. GetMediaType : la méthode GetMediaType récupère un type de média préféré, par valeur d’index.'
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Méthode CBasePin. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 186f2eddbedf4eb0565a4ca66ff4ed7e5b080090
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999331"
---
# <a name="cbasepingetmediatype-method"></a>Méthode CBasePin. GetMediaType

La `GetMediaType` méthode récupère un type de média préféré, par valeur d’index.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iPosition* 
</dt> <dd>

Valeur d’index de base zéro.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                            | Description                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Réussite.<br/>              |
| <dl> <dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt> </dl> | Index hors limites.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Index inférieur à zéro.<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>           | Erreur inattendue.<br/>     |



 

## <a name="remarks"></a>Notes

Dans la liste des types de média préférés du pin, cette méthode retourne le type avec une valeur d’index de *iPosition*. La classe [**CEnumMediaTypes**](cenummediatypes.md) appelle cette méthode pour énumérer les types de média préférés.

La classe de base retourne E \_ inattendue. Substituez cette méthode dans votre classe dérivée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




