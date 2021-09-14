---
description: La méthode Disconnect interrompt la connexion avec la broche de sortie.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: CPullPin. Disconnect, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007605"
---
# <a name="cpullpindisconnect-method"></a>CPullPin. Disconnect, méthode

La `Disconnect` méthode interrompt la connexion avec la broche de sortie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

cette méthode interrompt toute connexion effectuée dans la méthode [**CPullPin :: Connecter**](cpullpin-connect.md) . Appelez cette méthode à l’intérieur de votre méthode [**IPIN ::D éconnecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) . (Si votre code confidentiel est dérivé de [**CBasePin**](cbasepin.md), remplacez [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) pour appeler cette méthode.)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




