---
description: La méthode SetReconnectWhenActive spécifie si le code PIN prend en charge les reconnexions dynamiques.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Méthode CBasePin. SetReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542220"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a>Méthode CBasePin. SetReconnectWhenActive

La `SetReconnectWhenActive` méthode spécifie si le code PIN prend en charge les reconnexions dynamiques.

## <a name="syntax"></a>Syntaxe


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bCanReconnect* 
</dt> <dd>

Valeur booléenne qui spécifie si le code confidentiel peut se reconnecter dynamiquement. Si la **valeur est true**, le code confidentiel peut se reconnecter dynamiquement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Par défaut, vous devez arrêter un filtre avant de reconnecter l’un de ses pin. Si le code pin peut se reconnecter alors que le filtre est actif, appelez cette méthode avec la valeur **true**. Pour plus d’informations, consultez [génération de graphiques dynamiques](dynamic-graph-building.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




