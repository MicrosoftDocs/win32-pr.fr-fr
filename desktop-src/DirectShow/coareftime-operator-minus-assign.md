---
description: Cet opérateur soustrait une heure de référence d’une autre et définit cet objet sur le résultat.
ms.assetid: 573b6f6b-7634-4e78-872c-f869b59a75e2
title: COARefTime. Operator-=, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fd8e567933cf9061b6add3b3f756baec3120fdaeb1ffa0d71d4278e4221829f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757099"
---
# <a name="coareftimeoperator--method"></a>COARefTime. Operator-= méthode

Cet opérateur soustrait une heure de référence d’une autre et définit cet objet sur le résultat.

## <a name="syntax"></a>Syntaxe


```C++
COARefTime& operator-=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RT* \[ Réf\]
</dt> <dd>

Référence à l’objet **COARefTime** à soustraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une référence à l’objet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




