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
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526540"
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

## <a name="remarks"></a>Notes

La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) . La classe dérivée doit implémenter cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




