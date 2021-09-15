---
title: Interface INapEnforcementClientConnection2 (NapEnforcementClient. h)
description: Autoriser la gestion des connexions clientes. | Interface INapEnforcementClientConnection2 (NapEnforcementClient. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- NAP de l’interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413786"
---
# <a name="inapenforcementclientconnection2-interface"></a>Interface INapEnforcementClientConnection2

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

**INapEnforcementClientConnection2** fournit des méthodes qui permettent la gestion des connexions clientes.

> [!Note]  
> Cette interface hérite de toutes les méthodes de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) et doit être utilisée à la place.

 

## <a name="members"></a>Membres

L’interface **INapEnforcementClientConnection2** hérite de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md). **INapEnforcementClientConnection2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapEnforcementClientConnection2** possède ces méthodes.



| Méthode                                                                                                              | Description                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection2::GetInstalledShvs**](inapenforcementclientconnection2-getinstalledshvs.md)     | Permet d’obtenir les ID des validateurs d’intégrité du client.<br/>             |
| [**INapEnforcementClientConnection2::GetIsolationInfoEx**](inapenforcementclientconnection2-getisolationinfoex.md) | Utilisé pour obtenir les informations d’isolation pour le client.<br/>                 |
| [**INapEnforcementClientConnection2::SetInstalledShvs**](inapenforcementclientconnection2-setinstalledshvs.md)     | Utilisé par NapAgent pour définir les ID SHV installés pour le client.<br/>     |
| [**INapEnforcementClientConnection2::SetIsolationInfoEx**](inapenforcementclientconnection2-setisolationinfoex.md) | Utilisé par NapAgent pour définir les informations d’isolation pour le client.<br/> |



 

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

 





