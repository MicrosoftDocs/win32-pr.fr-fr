---
title: Interface INapSystemHealthAgentRequest (NapSystemHealthAgent. h)
description: SHA utilise pour communiquer et coordonner le traitement avec le système NAP.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- NAP de l’interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508526"
---
# <a name="inapsystemhealthagentrequest-interface"></a>Interface INapSystemHealthAgentRequest

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapSystemHealthAgentRequest** fournit des méthodes que SHA utilise pour communiquer et coordonner le traitement avec le système NAP.

## <a name="members"></a>Membres

L’interface **INapSystemHealthAgentRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthAgentRequest** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapSystemHealthAgentRequest** possède ces méthodes.



| Méthode                                                                                                                     | Description                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentRequest::GetCacheSoHFlag**](inapsystemhealthagentrequest-getcachesohflag-method.md)               | Utilisé uniquement par NapAgent.<br/>                                                            |
| [**INapSystemHealthAgentRequest::GetCorrelationId**](inapsystemhealthagentrequest-getcorrelationid-method.md)             | Utilisé par les agents d’intégrité système pour corréler SoHs et [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).<br/> |
| [**INapSystemHealthAgentRequest::GetSoHRequest**](inapsystemhealthagentrequest-getsohrequest-method.md)                   | Utilisé par les Sha pour récupérer les SoHs précédemment mis en cache par le NapAgent.<br/>                           |
| [**INapSystemHealthAgentRequest::GetSoHResponse**](inapsystemhealthagentrequest-getsohresponse-method.md)                 | Utilisé par l’agent d’intégrité pour récupérer son [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).<br/>         |
| [**INapSystemHealthAgentRequest::GetStringCorrelationId**](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | Utilisé par les agents d’intégrité système pour enregistrer l’ID de corrélation.<br/>                               |
| [**INapSystemHealthAgentRequest::SetSoHRequest**](inapsystemhealthagentrequest-setsohrequest-method.md)                   | Utilisé par les agents d’intégrité pour écrire leur demande d’intégrité.<br/>                                     |



 

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

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

