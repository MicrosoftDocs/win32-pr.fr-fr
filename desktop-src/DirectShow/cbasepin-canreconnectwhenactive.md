---
description: La méthode CanReconnectWhenActive interroge si le code PIN prend en charge les reconnexions dynamiques.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Méthode CBasePin. CanReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525568"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>Méthode CBasePin. CanReconnectWhenActive

La `CanReconnectWhenActive` méthode interroge si le code PIN prend en charge les reconnexions dynamiques.

## <a name="syntax"></a>Syntaxe


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur booléenne qui spécifie si le code confidentiel peut se reconnecter dynamiquement. Si la **valeur est true**, le code confidentiel peut se reconnecter dynamiquement.

## <a name="remarks"></a>Notes

Par défaut, vous devez arrêter un filtre avant de reconnecter l’un de ses pin. Toutefois, si un code PIN prend en charge la reconnexion dynamique, il peut se reconnecter alors que le filtre est actif. Pour plus d’informations, consultez [génération de graphiques dynamiques](dynamic-graph-building.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




