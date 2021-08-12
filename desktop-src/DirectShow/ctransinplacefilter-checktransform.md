---
description: 'La méthode CheckTransform vérifie si un type de média d’entrée est compatible avec un type de média de sortie. Cette méthode remplace la méthode CTransformFilter :: CheckTransform.'
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Méthode CTransInPlaceFilter. CheckTransform (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49b7f4aaac21cf6a55360e2e1b970bd9dfa62c0422241f7356871117e138d57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654958"
---
# <a name="ctransinplacefilterchecktransform-method"></a>Méthode CTransInPlaceFilter. CheckTransform

La `CheckTransform` méthode vérifie si un type de média d’entrée est compatible avec un type de média de sortie. Cette méthode remplace la méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mtIn* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type d’entrée.

</dd> <dt>

*mtOut* 
</dt> <dd>

Pointeur vers un objet **CMediaType** qui spécifie le type de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Le filtre **CTransInPlace** n’appelle jamais `CheckTransform` . Au lieu de cela, toute connexion de code confidentiel utilise [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) pour vérifier le type de média, en partant du principe que les types d’entrée et de sortie correspondent toujours.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




