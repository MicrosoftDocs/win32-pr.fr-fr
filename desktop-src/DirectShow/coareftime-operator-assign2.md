---
description: L’opérateur assigne une nouvelle heure de référence et utilise le paramètre « RT [ref] ».
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: COARefTime. Operator = méthode (Ctlutil. h)-RT [ref], paramètre
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
ms.openlocfilehash: e1a1e4c9482c187db7d5d5377535763b9fbab126b2153e0efa56bc341b402b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103159"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a>COARefTime. Operator = méthode (Ctlutil. h)-RT [ref], paramètre

Cet opérateur affecte une nouvelle heure de référence.

## <a name="syntax"></a>Syntaxe


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RT* \[ Réf\]
</dt> <dd>

Référence à une valeur de [**\_ temps de référence**](reference-time.md) qui spécifie la nouvelle durée de référence en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une référence à l’objet.

## <a name="requirements"></a>Configuration requise

| Condition requise                    | Valeur                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Ctlutil. h (inclure Flux. h)                                                                                   |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




