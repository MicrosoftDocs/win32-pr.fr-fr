---
title: Interface INapEnforcementClientConnection (NapEnforcementClient. h)
description: Autoriser la gestion des connexions clientes. | Interface INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- NAP de l’interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, Description
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413796"
---
# <a name="inapenforcementclientconnection-interface"></a>Interface INapEnforcementClientConnection

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

**INapEnforcementClientConnection** fournit des méthodes qui permettent la gestion des connexions clientes.

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) hérite de toutes les méthodes de cette interface et doit être utilisé à la place.

 

## <a name="members"></a>Membres

L’interface **INapEnforcementClientConnection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientConnection** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapEnforcementClientConnection** possède ces méthodes.



| Méthode                                                                                                                           | Description                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection :: GetConnectionID,**](inapenforcementclientconnection-getconnectionid-method.md)               | Obtient l’ID de connexion du client.<br/>                                                                                          |
| [**INapEnforcementClientConnection::GetCorrelationId**](inapenforcementclientconnection-getcorrelationid-method.md)             | Obtient l’ID utilisé pour corréler les demandes SoH et les réponses SoH.<br/>                                                                  |
| [**INapEnforcementClientConnection::GetEnforcerPrivateData**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | Utilisé par l’application pour recevoir des données privées.<br/>                                                                                      |
| [**INapEnforcementClientConnection :: GetFlags**](inapenforcementclientconnection-getflags-method.md)                             | Obtient la valeur de l’indicateur qui différencie les réponses premières des réponses en raison des SoHRequests mises en cache par les enforceurs.<br/> |
| [**INapEnforcementClientConnection::GetIsolationInfo**](inapenforcementclientconnection-getisolationinfo-method.md)             | Utilisé pour récupérer les informations d’isolation du client.<br/>                                                                              |
| [**INapEnforcementClientConnection::GetMaxSize**](inapenforcementclientconnection-getmaxsize-method.md)                         | Obtient la taille maximale du paquet SoH pour ce client.<br/>                                                                       |
| [**INapEnforcementClientConnection::GetPrivateData**](inapenforcementclientconnection-getprivatedata-method.md)                 | Utilisé par NapAgent pour accéder aux données privées.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetSoHRequest**](inapenforcementclientconnection-getsohrequest-method.md)                   | Obtient la demande de déclaration d’intégrité.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::GetSoHResponse**](inapenforcementclientconnection-getsohresponse-method.md)                 | Obtient le SoH-Response reçu par le client de mise en œuvre.<br/>                                                                      |
| [**INapEnforcementClientConnection::GetStringCorrelationId**](inapenforcementclientconnection-getstringcorrelationid-method.md) | Obtient la version de chaîne de l’ID de corrélation. Principalement utilisé à des fins de journalisation.<br/>                                             |
| [**INapEnforcementClientConnection :: Initialize**](inapenforcementclientconnection-initialize-method.md)                         | Initialise la connexion.<br/>                                                                                                    |
| [**INapEnforcementClientConnection::SetConnectionId**](inapenforcementclientconnection-setconnectionid-method.md)               | Définit l’ID de connexion du client.<br/>                                                                                          |
| [**INapEnforcementClientConnection::SetCorrelationId**](inapenforcementclientconnection-setcorrelationid-method.md)             | Définit l’ID utilisé pour corréler les demandes SoH et les réponses SoH.<br/>                                                                  |
| [**INapEnforcementClientConnection::SetEnforcerPrivateData**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | Utilisé par l’application pour définir des données privées.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetFlags**](inapenforcementclientconnection-setflags-method.md)                             | Définit l’indicateur qui différencie les réponses de première heure des réponses en raison des SoHRequests mises en cache par les enforceurs.<br/>                  |
| [**INapEnforcementClientConnection::SetIsolationInfo**](inapenforcementclientconnection-setisolationinfo-method.md)             | Utilisé par NapAgent pour définir les informations d’isolation du client.<br/>                                                           |
| [**INapEnforcementClientConnection::SetMaxSize**](inapenforcementclientconnection-setmaxsize-method.md)                         | Définit la taille maximale du paquet SoH pour ce client.<br/>                                                                       |
| [**INapEnforcementClientConnection::SetPrivateData**](inapenforcementclientconnection-setprivatedata-method.md)                 | Utilisé par NapAgent pour définir les données privées.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetSoHRequest**](inapenforcementclientconnection-setsohrequest-method.md)                   | Définit la demande de déclaration d’intégrité.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::SetSoHResponse**](inapenforcementclientconnection-setsohresponse-method.md)                 | Définit le SoH-Response et est utilisé par le client de mise en œuvre lors de la réception d’un paquet.<br/>                                             |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

