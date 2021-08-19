---
description: 'La méthode active indique au code confidentiel que le filtre est maintenant actif. Cette méthode remplace la méthode CBasePin :: active. Si le code PIN est connecté, cette méthode démarre le thread de streaming.'
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Méthode CSourceStream. active (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 427c0318bad4df810b29f3596e3a9516f8dbb73e97dd7e378c561bef28bf2f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073342"
---
# <a name="csourcestreamactive-method"></a>CSourceStream. active, méthode

La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif. Cette méthode remplace la méthode [**CBasePin :: active**](cbasepin-active.md) . Si le code PIN est connecté, cette méthode démarre le thread de streaming.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le code PIN est déjà actif.<br/>  |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                    |
| <dl> <dt>**E \_ échec**</dt> </dl>  | Impossible de démarrer le thread.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




