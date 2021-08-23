---
description: Cet opérateur divise une heure de référence par une valeur.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: COARefTime. Operator/Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ff5f23691a3c4c44fdb9b93006834913648391ed473cf84906dff3eb8afb21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566019"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator/méthode

Cet opérateur divise une heure de référence par une valeur.

## <a name="syntax"></a>Syntaxe


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*l* 
</dt> <dd>

Division.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un nouvel objet **COARefTime** égal au quotient de cet objet et **l**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




