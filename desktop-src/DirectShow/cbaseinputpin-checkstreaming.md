---
description: Détermine si le code confidentiel peut accepter des exemples.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Méthode CBaseInputPin. CheckStreaming (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123778"
---
# <a name="cbaseinputpincheckstreaming-method"></a>Méthode CBaseInputPin. CheckStreaming

Détermine si le code confidentiel peut accepter des exemples.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                                           | Description                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                   |
| <dl> <dt>**S \_ false**</dt> </dl>               | Le code PIN est en cours de vidage.<br/> |
| <dl> <dt>**\_erreur d' \_ exécution VFW E \_**</dt> </dl> | Une erreur d’exécution s’est produite.<br/> |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl>   | Le code PIN est arrêté.<br/>        |



 

## <a name="remarks"></a>Notes

La classe dérivée peut substituer cette méthode pour effectuer des vérifications supplémentaires. Dans la méthode de substitution, appelez également l’implémentation de la classe de base.

La méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) appelle cette méthode. Vous devez substituer la méthode [**CBasePin :: EndOfStream**](cbasepin-endofstream.md) pour appeler également cette méthode.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




