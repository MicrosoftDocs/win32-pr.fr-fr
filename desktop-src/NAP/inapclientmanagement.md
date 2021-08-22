---
title: Interface INapClientManagement (NapManagement. h)
description: Fournit des méthodes pour la gestion des clients NAP. | Interface INapClientManagement (NapManagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- NAP de l’interface INapClientManagement
- INapClientManagement interface NAP, Description
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a9d338cdaad8ed46fd3c3c730ca3ae4c2065cda9803c283ae262addd939713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622115"
---
# <a name="inapclientmanagement-interface"></a>Interface INapClientManagement

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapClientManagement** fournit des méthodes pour la gestion des clients NAP.

> [!Note]  
> [**INapClientManagement2**](inapclientmanagement2.md) hérite de toutes les méthodes de cette interface et doit être utilisé à la place.

 

## <a name="members"></a>Membres

L’interface **INapClientManagement** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapClientManagement** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapClientManagement** possède ces méthodes.



| Méthode                                                                                                                | Description                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**INapClientManagement::GetNapClientInfo**](inapclientmanagement-getnapclientinfo.md)                               | Récupère des informations sur un client NAP.<br/>                          |
| [**INapClientManagement::GetRegisteredEnforcementClients**](inapclientmanagement-getregisteredenforcementclients.md) | Récupère des informations sur les clients de mise en œuvre inscrits.<br/>    |
| [**INapClientManagement::GetRegisteredSystemHealthAgents**](inapclientmanagement-getregisteredsystemhealthagents.md) | Récupérez des informations sur un SHA inscrit.<br/>                       |
| [**INapClientManagement::GetSystemIsolationInfo**](inapclientmanagement-getsystemisolationinfo.md)                   | Récupère des informations sur l’état d’isolement du client NAP.<br/> |
| [**INapClientManagement::RegisterEnforcementClient**](inapclientmanagement-registerenforcementclient.md)             | Inscrit un client de mise en œuvre auprès du système NAP.<br/>               |
| [**INapClientManagement::RegisterSystemHealthAgent**](inapclientmanagement-registersystemhealthagent.md)             | Inscrit un SHA auprès du système NAP.<br/>                              |
| [**INapClientManagement::UnregisterEnforcementClient**](inapclientmanagement-unregisterenforcementclient.md)         | Annule l’inscription d’un client de contrainte auprès du système NAP.<br/>             |
| [**INapClientManagement::UnregisterSystemHealthAgent**](inapclientmanagement-unregistersystemhealthagent.md)         | Annule l’inscription d’un SHA auprès du système NAP.<br/>                            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

