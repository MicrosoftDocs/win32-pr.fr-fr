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
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999339"
---
# <a name="cbasepindisconnectinternal-method"></a>Méthode CBasePin. DisconnectInternal

La `DisconnectInternal` méthode interrompt la connexion de code confidentiel actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                         | Description                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | Le pin n’était pas connecté.<br/>                                              |
| <dl> <dt>**\_OK**</dt> </dl>                | Réussite.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ non \_ arrêté**</dt> </dl> | Le filtre est actif et le code confidentiel ne prend pas en charge la reconnexion dynamique.<br/> |



 

## <a name="remarks"></a>Notes

La méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) délègue le processus de déconnexion à cette méthode. Cette méthode appelle la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) . Elle libère également le décompte de références sur l’autre code confidentiel, qui est détenu par la variable membre [**\_ connectée CBasePin :: m**](cbasepin-m-connected.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




