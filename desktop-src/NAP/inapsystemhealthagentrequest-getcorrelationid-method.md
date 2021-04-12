---
title: Méthode INapSystemHealthAgentRequest GetCorrelationId (NapSystemHealthAgent. h)
description: Est utilisé par les agents d’intégrité système pour mettre en corrélation les réponses SOH et SoH.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- Méthode GetCorrelationId NAP
- Méthode GetCorrelationId NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, méthode GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519273"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a>INapSystemHealthAgentRequest :: GetCorrelationId, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentRequest :: GetCorrelationId** est utilisée par les agents d’intégrité système pour mettre en corrélation les réponses SoH et SOH.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CorrelationId* \[ à\]
</dt> <dd>

Pointeur vers un ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid) unique pour l’échange de déclaration d’intégrité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





