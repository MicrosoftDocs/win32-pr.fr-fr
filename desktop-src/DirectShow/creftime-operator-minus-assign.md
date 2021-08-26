---
description: L’opérateur-= soustrait une heure de référence d’une autre.
ms.assetid: 5b0ec72e-87d8-4562-96b1-40e4f5036fd4
title: CRefTime. Operator-=, méthode (reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 854831c2ed9cf5b636160dccaf002a7ea9ac37ebaa5e970f8b63dd3f112cdda6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108039"
---
# <a name="creftimeoperator--method"></a>CRefTime. Operator-= méthode

L’opérateur-= soustrait une heure de référence d’une autre.

## <a name="syntax"></a>Syntaxe


```C++
CRefTime& operator-=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RT* \[ Réf\]
</dt> <dd>

Référence à un objet **CRefTime** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une référence à l’objet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Reftime. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




