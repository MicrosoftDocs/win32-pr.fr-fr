---
description: 'Méthode CTransformInputPin. CheckMediaType : la méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.'
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Méthode CTransformInputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084997"
---
# <a name="ctransforminputpincheckmediatype-method"></a>Méthode CTransformInputPin. CheckMediaType

La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mtIn* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Notes 

Cette méthode implémente la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) virtuelle pure. Elle appelle la méthode [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) du filtre, qui est également pure virtual. La classe dérivée du filtre doit implémenter **CheckInputType** pour déterminer si un type d’entrée donné est acceptable.

Si la broche de sortie du filtre est connectée, cette méthode appelle également la méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) du filtre pour déterminer si le type d’entrée est compatible avec le type de sortie. La méthode **CheckTransform** est également virtuelle pure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




