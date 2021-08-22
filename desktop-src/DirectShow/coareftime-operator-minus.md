---
description: Cet opérateur soustrait une heure de référence d’une autre.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: COARefTime. Operator-Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da8de864f344321cc5dca801782aab1f8476eb91608b42577cca6a34c625e153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073823"
---
# <a name="coareftimeoperator--method"></a>COARefTime. Operator-méthode

Cet opérateur soustrait une heure de référence d’une autre.

## <a name="syntax"></a>Syntaxe


```C++
COARefTime operator-(
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

Retourne un nouvel objet **COARefTime** égal à la différence entre les temps de référence.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




