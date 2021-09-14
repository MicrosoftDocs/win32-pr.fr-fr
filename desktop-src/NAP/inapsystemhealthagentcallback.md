---
title: Interface INapSystemHealthAgentCallback (NapSystemHealthAgent. h)
description: Sont déclarés par le système et implémentés par l’enregistreur SHA afin que le NapAgent puisse communiquer avec l’algorithme SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- NAP de l’interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011638"
---
# <a name="inapsystemhealthagentcallback-interface"></a>Interface INapSystemHealthAgentCallback

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapSystemHealthAgentCallback** fournit des méthodes de rappel qui sont déclarées par le système et implémentées par l’enregistreur SHA afin que le NapAgent puisse communiquer avec l’algorithme SHA.

## <a name="members"></a>Membres

L’interface **INapSystemHealthAgentCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthAgentCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapSystemHealthAgentCallback** possède ces méthodes.



| Méthode                                                                                                                                           | Description                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentCallback::CompareSoHRequests**](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | Utilisé par l’algorithme SHA pour comparer le SoHs.<br/>                                                                      |
| [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | Appelé par NapAgent pour déterminer l’état de l’agent SHA.<br/>                                                 |
| [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | Appelée par NapAgent pour interroger la demande de déclaration d’intégrité de l’algorithme de hachage.<br/>                                                    |
| [**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | Appelé si une requête SoH a été interrogée à partir de l’agent SHA, mais que la réponse n’a jamais été renvoyée.<br/>                      |
| [**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | Appelée par NapAgent pour indiquer que l’état d’isolement système ou l’heure de fin de la période d’essai a changé.<br/> |
| [**INapSystemHealthAgentCallback ::P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md)                             | Appelé lorsque NapAgent reçoit une réponse SoH destinée à cet agent d’intégrité.<br/>                         |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

