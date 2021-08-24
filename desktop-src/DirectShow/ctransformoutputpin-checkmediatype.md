---
description: 'Méthode CTransformOutputPin. CheckMediaType : la méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.'
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Méthode CTransformOutputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3894e701b22f6380e591eccf978e84a1321f57a84485cea8a6e3116181f3f2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538459"
---
# <a name="ctransformoutputpincheckmediatype-method"></a>Méthode CTransformOutputPin. CheckMediaType

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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                  | Description                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | La broche d’entrée du filtre n’est pas connectée.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode implémente la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) virtuelle pure. La méthode échoue si la broche d’entrée du filtre n’est pas connectée. Sinon, elle appelle la méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) du filtre, qui est également pure virtual. La classe dérivée du filtre doit implémenter **CheckTransform**, qui détermine si le type de média de sortie proposé est compatible avec le type de média d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




