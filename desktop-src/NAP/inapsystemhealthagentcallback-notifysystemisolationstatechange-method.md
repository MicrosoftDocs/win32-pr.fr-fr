---
title: Méthode INapSystemHealthAgentCallback NotifySystemIsolationStateChange (NapSystemHealthAgent. h)
description: Est appelé par le NapAgent pour indiquer que l’état d’isolement système ou l’heure de fin de la période d’essai a changé.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- Méthode NotifySystemIsolationStateChange NAP
- Méthode NotifySystemIsolationStateChange NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode NotifySystemIsolationStateChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc75686801148e0866f8996dabdb31af66eac9b55c60473782a794ea59f7463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621150"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a>INapSystemHealthAgentCallback :: NotifySystemIsolationStateChange, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentCallback :: NotifySystemIsolationStateChange** est appelée par le NapAgent pour indiquer que l’état d’isolement système ou l’heure de fin de la période d’essai a changé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                          | Description                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Indique la réussite de l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.

L’agent d’intégrité peut interroger l’état du système NAP à l’aide de [**INapSystemHealthAgentBinding :: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





