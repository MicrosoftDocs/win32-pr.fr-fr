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
ms.openlocfilehash: de22d8a6fc634ffbb16ac111de1ad20dc0638660c5091c835a44f256d9ed1d4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076619"
---
# <a name="cbaseinputpincheckstreaming-method"></a>Méthode CBaseInputPin. CheckStreaming

Détermine si le code confidentiel peut accepter des exemples.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                                           | Description                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                   |
| <dl> <dt>**S \_ false**</dt> </dl>               | Le code PIN est en cours de vidage.<br/> |
| <dl> <dt>**\_erreur d' \_ exécution VFW E \_**</dt> </dl> | Une erreur d’exécution s’est produite.<br/> |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl>   | Le code PIN est arrêté.<br/>        |



 

## <a name="remarks"></a>Remarques

La classe dérivée peut substituer cette méthode pour effectuer des vérifications supplémentaires. Dans la méthode de substitution, appelez également l’implémentation de la classe de base.

La méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) appelle cette méthode. Vous devez substituer la méthode [**CBasePin :: EndOfStream**](cbasepin-endofstream.md) pour appeler également cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




