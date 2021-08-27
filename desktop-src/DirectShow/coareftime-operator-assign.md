---
description: Cet opérateur affecte une nouvelle heure de référence.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: COARefTime. Operator =, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31784a008a2074156c69abf868739ec27c459dabdba1437397780086d28f9847
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084459"
---
# <a name="coareftimeoperator-method-ctlutilh"></a>COARefTime. Operator =, méthode (Ctlutil. h)

Cet opérateur affecte une nouvelle heure de référence.

## <a name="syntax"></a>Syntaxe


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*services Bureau à distance* \[ Réf\]
</dt> <dd>

Référence à une valeur **double** qui spécifie la nouvelle durée de référence en secondes.

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

 

 




