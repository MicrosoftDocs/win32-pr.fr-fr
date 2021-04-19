---
description: Cet opérateur multiplie une heure de référence par une valeur.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: COARefTime. Operator *, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545568"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator, \* méthode

Cet opérateur multiplie une heure de référence par une valeur.

## <a name="syntax"></a>Syntaxe


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*l* 
</dt> <dd>

Multiplicateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un nouvel objet **COARefTime** égal au produit de cet objet et **l**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




