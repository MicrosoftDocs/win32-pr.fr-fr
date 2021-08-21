---
description: La méthode CheckMediaType détermine si le filtre accepte un type de média spécifique.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Méthode CBaseRenderer. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8de57346138b4683f59cfa612f01fff1ef3d8fd9aceec9b34daee49bfa74ebbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157979"
---
# <a name="cbaserenderercheckmediatype-method"></a>Méthode CBaseRenderer. CheckMediaType

La `CheckMediaType` méthode détermine si le filtre accepte un type de média spécifique.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si le type de média proposé est acceptable. Sinon, retourne S \_ false ou un code d’erreur.

## <a name="remarks"></a>Remarques

La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) . La classe dérivée doit implémenter cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




