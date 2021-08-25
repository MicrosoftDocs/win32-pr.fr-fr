---
title: Interface INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
description: L’SHA utilise pour communiquer avec le NapAgent. | Interface INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- NAP de l’interface INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c42db59c23826855ca6cda7529eb9dcbbadfb2a1ee2a5aa93d9bd45587c45a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780929"
---
# <a name="inapsystemhealthagentbinding2-interface"></a>Interface INapSystemHealthAgentBinding2

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

**INapSystemHealthAgentBinding2** fournit des méthodes que l’SHA utilise pour communiquer avec NapAgent.

> [!Note]  
> Cette interface hérite de toutes les méthodes de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) et doit être utilisée à la place.

 

## <a name="members"></a>Membres

L’interface **INapSystemHealthAgentBinding2** hérite de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md). **INapSystemHealthAgentBinding2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapSystemHealthAgentBinding2** possède ces méthodes.



| Méthode                                                                                                                    | Description                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | Appelée par l’SHA pour déterminer l’état d’isolement du système et l’état d’isolement étendu.<br/> |



 

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

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

 





