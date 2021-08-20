---
title: Interface INapEnforcementClientCallback (NapEnforcementClient. h)
description: Les clients de contrainte doivent implémenter pour permettre à NapAgent de communiquer avec eux.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- NAP de l’interface INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP, Description
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48c595918d28d912725353eb856de8f0af4541a68dabcb6f5a7cb0bb944496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134038"
---
# <a name="inapenforcementclientcallback-interface"></a>Interface INapEnforcementClientCallback

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapEnforcementClientCallback** fournit des méthodes de rappel que les clients de mise en œuvre doivent implémenter pour permettre à NapAgent de communiquer avec eux.

## <a name="members"></a>Membres

L’interface **INapEnforcementClientCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapEnforcementClientCallback** possède ces méthodes.



| Méthode                                                                                                         | Description                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientCallback::GetConnections**](inapenforcementclientcallback-getconnections-method.md)   | Utilisé par NapAgent pour récupérer des connexions.<br/>                         |
| [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) | Utilisé par NapAgent pour informer le client de contrainte des modifications de SoH.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



 

