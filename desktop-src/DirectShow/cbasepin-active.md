---
description: La méthode active indique au code confidentiel que le filtre est maintenant actif.
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
ms.openlocfilehash: 4a89c0c75671e6eb29b6ddb260c5f5ec0c385399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521655"
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

## <a name="remarks"></a>Notes

Lorsque le filtre passe de arrêté à suspendu, la classe [**CBaseFilter**](cbasefilter.md) appelle cette méthode sur toutes les broches connectées du filtre.

Cette méthode n’a aucun effet dans la classe de base. Les classes dérivées peuvent substituer cette méthode. par exemple, un code confidentiel peut valider des allocateurs ou obtenir des ressources matérielles.

L’état interne du gestionnaire de graphique de filtre n’est pas mis à jour avant le retour de cette fonction membre, donc ne Testez pas l’État à partir de cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




