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
ms.openlocfilehash: 29afc98da01351f63df45997b8cc338e17a1234c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010082"
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

## <a name="return-value"></a>Valeur de retour

Retourne une référence à l’objet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




