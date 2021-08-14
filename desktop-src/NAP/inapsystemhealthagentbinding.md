---
title: Interface INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: L’SHA utilise pour communiquer avec le NapAgent. | Interface INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- NAP de l’interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38fe66a5cd6883114ff46da3e98174d299f1813e670ed5ce67ee3843dc210d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799184"
---
# <a name="inapsystemhealthagentbinding-interface"></a>Interface INapSystemHealthAgentBinding

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

**INapSystemHealthAgentBinding** fournit des méthodes que l’SHA utilise pour communiquer avec NapAgent.

> [!Note]  
> [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) hérite de toutes les méthodes de cette interface et doit être utilisé à la place.

 

## <a name="members"></a>Membres

L’interface **INapSystemHealthAgentBinding** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthAgentBinding** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapSystemHealthAgentBinding** possède ces méthodes.



| Méthode                                                                                                                     | Description                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding::FlushCache**](inapsystemhealthagentbinding-flushcache-method.md)                         | Appelée par un SHA pour vider son cache SoH.<br/>                                                |
| [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | Appelée par l’SHA pour déterminer l’état de l’isolation du système.<br/>                                 |
| [**INapSystemHealthAgentBinding :: Initialize**](inapsystemhealthagentbinding-initialize-method.md)                         | Initialise l’algorithme SHA et lie l’algorithme SHA au service NapAgent. <br/>                         |
| [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md)               | Appelée par l’SHA lorsque leur SoH change.<br/>                                                  |
| [**INapSystemHealthAgentBinding :: Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md)                     | Appelée par l’agent de niveau de l’agent pour obliger le NapAgent à libérer toutes ses références aux pointeurs SHA COM.<br/> |



 

## <a name="remarks"></a>Remarques

Toutes les API de cette interface renverront **RPC \_ E \_ Disconnected** si le NapAgent est arrêté. Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

