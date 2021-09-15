---
title: Interface INapEnforcementClientBinding (NapEnforcementClient. h)
description: Les clients de contrainte utilisent pour communiquer avec le NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- NAP de l’interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, Description
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311981"
---
# <a name="inapenforcementclientbinding-interface"></a>Interface INapEnforcementClientBinding

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

**INapEnforcementClientBinding** fournit des méthodes que les clients de mise en œuvre utilisent pour communiquer avec NapAgent.

## <a name="members"></a>Membres

L’interface **INapEnforcementClientBinding** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientBinding** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapEnforcementClientBinding** possède ces méthodes.



| Méthode                                                                                                                           | Description                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientBinding :: CreateConnection**](inapenforcementclientbinding-createconnection-method.md)                   | Utilisé par les enforceurs pour créer des objets de connexion.<br/>                                                                                                                                                            |
| [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | Utilisé par le client de mise en œuvre lorsqu’il a besoin d’une requête SoH pour une connexion particulière.<br/>                                                                                                                   |
| [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md)                               | Démarre le service NapAgent. Le client de contrainte doit appeler cette méthode avant d’appeler toute autre méthode de cette interface.<br/>                                                                            |
| [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | Utilisé pour informer le NapAgent qu’une connexion à un client de contrainte s’est déroulée.<br/>                                                                                                                      |
| [**INapEnforcementClientBinding::NotifySoHChangeFailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | Utilisé par le client de mise en œuvre pour informer NapAgent qu’il n’a pas pu traiter un précédent [**INapEnforcementClientCallback :: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).<br/> |
| [**INapEnforcementClientBinding ::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md)               | Utilisé par les clients de mise en œuvre chaque fois qu’ils obtiennent une SoH-Response objet blob de données à partir du serveur de mise en œuvre.<br/>                                                                                                       |
| [**INapEnforcementClientBinding :: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)                           | Conclut le service NapAgent pour cette connexion client.<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>Remarques

Toutes les API de cette interface renverront RPC \_ E \_ Disconnected si le NapAgent est arrêté. Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.

## <a name="requirements"></a>Configuration requise



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

 

