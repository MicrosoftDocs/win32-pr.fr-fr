---
description: La méthode DisplayPinInfo suit une connexion de code confidentiel pendant le débogage.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Méthode CBasePin. DisplayPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea563ca07eaea6b6974a831726918866414a33b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999337"
---
# <a name="cbasepindisplaypininfo-method"></a>Méthode CBasePin. DisplayPinInfo

La `DisplayPinInfo` méthode effectue le suivi d’une connexion de code confidentiel pendant le débogage.

## <a name="syntax"></a>Syntaxe


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Pointeur vers le code confidentiel de réception.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Dans les versions Debug, cette méthode appelle la fonction [**DbgLog**](dbglog.md) pour effectuer le suivi d’une tentative de connexion. Dans les versions commerciales, cette méthode n’a aucun effet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




