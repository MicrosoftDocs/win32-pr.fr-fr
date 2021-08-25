---
description: 'Méthode CTransformFilter. GetMediaType : la méthode GetMediaType récupère un type de média préféré pour la broche de sortie.'
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Méthode CTransformFilter. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b471ac42ceb44f5e65a2ac08365bf97ab0e3157816b772b331cde0fa0b13bde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907529"
---
# <a name="ctransformfiltergetmediatype-method"></a>Méthode CTransformFilter. GetMediaType

La `GetMediaType` méthode récupère un type de média par défaut pour la broche de sortie.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                            | Description                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Réussite.<br/>              |
| <dl> <dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt> </dl> | Index hors limites.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Index inférieur à zéro.<br/> |



 

## <a name="remarks"></a>Remarques

La méthode [**CTransformOutputPin :: GetMediaType**](ctransformoutputpin-getmediatype.md) de la broche de sortie appelle cette méthode. La classe dérivée doit implémenter cette méthode. Pour plus d’informations, consultez [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




