---
description: La méthode GetNext récupère l’élément à la position spécifiée et avance la position.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: CGenericList. GetNext, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f116dd1a965145e5bdf4808d25a7406b4709967c5cf971ad3529ae9d301ebc4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539739"
---
# <a name="cgenericlistgetnext-method"></a>CGenericList. GetNext, méthode

La `GetNext` méthode récupère l’élément à la position spécifiée et avance la position.

## <a name="syntax"></a>Syntaxe


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RP* \[ Réf\]
</dt> <dd>

Référence à une valeur de POSITION.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers un objet de type **Object** (le type de modèle).

## <a name="remarks"></a>Remarques

Cette méthode avance l’indicateur de position à la position suivante. Si l’indicateur de position se déplace au-delà de la fin de la liste, la méthode lui affecte la **valeur null**.

Si *RP* a la **valeur null**, la méthode retourne la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




