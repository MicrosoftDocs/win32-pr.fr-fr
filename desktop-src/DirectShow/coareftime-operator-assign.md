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
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528899"
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
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




