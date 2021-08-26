---
description: 'Méthode CBasePin. CheckConnect : la méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.'
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Méthode CBasePin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a91e936f13c76ed4d99d7c5048820777afa47c9a52c260bb7f34acb702cb777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916849"
---
# <a name="cbasepincheckconnect-method"></a>Méthode CBasePin. CheckConnect

La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                               | Description                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                      | Réussite.<br/>                           |
| <dl> <dt>**VFW \_ E \_ sens non valide \_**</dt> </dl> | Les directions de code confidentiel ne sont pas compatibles.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode est appelée sur les deux codes confidentiels au début du processus de connexion. le code pin de connexion l’appelle à partir de la méthode [**CBasePin :: Connecter**](cbasepin-connect.md) , et l’épingle de réception l’appelle à partir de la méthode [**CBasePin :: ReceiveConnection**](cbasepin-receiveconnection.md) .

Utilisez cette méthode pour déterminer si le code confidentiel spécifié par le paramètre *pPin* convient pour une connexion. La classe de base retourne une erreur si les deux broches ont la même direction (à la fois l’entrée ou les deux). Les classes dérivées peuvent substituer cette méthode pour vérifier d’autres fonctionnalités dans le code confidentiel. Par exemple, la classe [**CBaseOutputPin**](cbaseoutputpin.md) interroge la broche d’entrée pour son interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

Si cette méthode échoue, la connexion échoue et le code PIN appelle la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) . Utilisez **BreakConnect** pour libérer toutes les ressources obtenues dans `CheckConnect` . Par exemple, si `CheckConnect` appelle la méthode **QueryInterface** , **BreakConnect** doit libérer l’interface.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




