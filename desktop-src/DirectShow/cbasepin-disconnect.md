---
description: 'CBasePin. Disconnect, méthode : la méthode Disconnect interrompt la connexion de code confidentiel actuelle. Cette méthode implémente la méthode IPin ::D éconnecter.'
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: CBasePin. Disconnect, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0048624b79daa6948851fd9a56142b97c7e185caa9bbcbdeb6c2c1b19f591eb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916629"
---
# <a name="cbasepindisconnect-method"></a>CBasePin. Disconnect, méthode

La `Disconnect` méthode interrompt la connexion de code confidentiel actuelle. Cette méthode implémente la méthode [**IPIN ::D éconnecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Disconnect();
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

La classe de base délègue la majeure partie du travail à la méthode [**CBasePin ::D isconnectinternal**](cbasepin-disconnectinternal.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




