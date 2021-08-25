---
description: La méthode DisconnectInternal interrompt la connexion de code confidentiel actuelle.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Méthode CBasePin. DisconnectInternal (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c420419e49f7093e6fdf1fdc66880035f4844d03277db18b5c134d9ee69b10fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916529"
---
# <a name="cbasepindisconnectinternal-method"></a>Méthode CBasePin. DisconnectInternal

La `DisconnectInternal` méthode interrompt la connexion de code confidentiel actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                         | Description                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | Le pin n’était pas connecté.<br/>                                              |
| <dl> <dt>**\_OK**</dt> </dl>                | Réussite.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ non \_ arrêté**</dt> </dl> | Le filtre est actif et le code confidentiel ne prend pas en charge la reconnexion dynamique.<br/> |



 

## <a name="remarks"></a>Remarques

La méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) délègue le processus de déconnexion à cette méthode. Cette méthode appelle la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) . Elle libère également le décompte de références sur l’autre code confidentiel, qui est détenu par la variable membre [**\_ connectée CBasePin :: m**](cbasepin-m-connected.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




