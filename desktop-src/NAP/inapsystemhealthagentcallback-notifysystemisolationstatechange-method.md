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
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741956"
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



 

## <a name="remarks"></a>Notes

Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.

L’agent d’intégrité peut interroger l’état du système NAP à l’aide de [**INapSystemHealthAgentBinding :: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





