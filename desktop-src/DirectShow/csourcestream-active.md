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
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542619"
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
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                    |
| <dl> <dt>**E \_ échec**</dt> </dl>  | Impossible de démarrer le thread.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




