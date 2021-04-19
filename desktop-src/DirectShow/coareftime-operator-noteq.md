---
description: Cet opérateur teste l’inégalité entre deux heures de référence.
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: COARefTime. Operator ! =, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e93934d7b31715422f2cc091e606b681a57e7f61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526775"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator ! =, méthode

Cet opérateur teste l’inégalité entre deux heures de référence.

## <a name="syntax"></a>Syntaxe


```C++
BOOL operator!=(
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

Retourne la **valeur true** si les deux objets ne sont pas égaux. Sinon, retourne **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




