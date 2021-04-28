---
description: 'CDynamicOutputPin. Disconnect, méthode : la méthode Disconnect interrompt la connexion de code confidentiel actuelle. Cette méthode implémente la méthode IPin ::D éconnecter.'
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: CDynamicOutputPin. Disconnect, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099297"
---
# <a name="cdynamicoutputpindisconnect-method"></a>CDynamicOutputPin. Disconnect, méthode

La `Disconnect` méthode interrompt la connexion de code confidentiel actuelle. Cette méthode implémente la méthode [**IPIN ::D éconnecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le pin n’était pas connecté.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                   |



 

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) pour activer la déconnexion pendant que le filtre est actif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




