---
description: Cet opérateur vérifie si une heure de référence est inférieure ou égale à une autre.
ms.assetid: ae7449b7-d319-4e76-892f-0f9ae63ddf94
title: COARefTime. Operator>=, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6d19686fc2c904534f66882172db6bec52b4873a36104ce78d2d826a771978d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108469"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator>=, méthode

Cet opérateur vérifie si une heure de référence est inférieure ou égale à une autre.

## <a name="syntax"></a>Syntaxe


```C++
BOOL operator>=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RT* \[ Réf\]
</dt> <dd>

Référence à l’objet **COARefTime** à comparer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si cet objet est inférieur ou égal à *RT*. Sinon, retourne **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




