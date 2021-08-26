---
description: La méthode CheckInputType vérifie si un type de média spécifié est acceptable pour l’entrée.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Méthode CTransformFilter. CheckInputType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ef410ac8d96160b39ca9b7103e5125be8619169ba6b287a32b8769e57a0cbf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053619"
---
# <a name="ctransformfiltercheckinputtype-method"></a>Méthode CTransformFilter. CheckInputType

La `CheckInputType` méthode vérifie si un type de média spécifié est acceptable pour l’entrée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mtIn* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                | Description                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Le type de média est acceptable.<br/>     |
| <dl> <dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt> </dl> | Le type de média n’est pas acceptable.<br/> |



 

## <a name="remarks"></a>Remarques

La classe dérivée doit implémenter cette méthode. Retourne S \_ OK si le format d’entrée proposé est acceptable, ou un code d’erreur dans le cas contraire.

Cette méthode n’a pas besoin de vérifier que le format d’entrée est compatible avec le format de sortie (le cas échéant). La broche d’entrée vérifie cela en appelant la méthode [**CheckTransform**](ctransformfilter-checktransform.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




