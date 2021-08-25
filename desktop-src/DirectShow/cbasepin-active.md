---
description: 'CBasePin. active, méthode : la méthode active indique au code confidentiel que le filtre est maintenant actif.'
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: CBasePin. active, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1d651c58693789945af34d266aa8541679d1226d655530b90c542c8b0fc88b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872539"
---
# <a name="cbasepinactive-method"></a>CBasePin. active, méthode

La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Lorsque le filtre passe de arrêté à suspendu, la classe [**CBaseFilter**](cbasefilter.md) appelle cette méthode sur toutes les broches connectées du filtre.

Cette méthode n’a aucun effet dans la classe de base. Les classes dérivées peuvent substituer cette méthode. par exemple, un code confidentiel peut valider des allocateurs ou obtenir des ressources matérielles.

L’état interne du gestionnaire de graphique de filtre n’est pas mis à jour avant le retour de cette fonction membre, donc ne Testez pas l’État à partir de cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




