---
title: Services de sécurité MSMQ
description: Les messages RPC synchrones peuvent utiliser toutes les fonctionnalités de sécurité disponibles à partir de la durée d’exécution RPC. Pour plus d’informations, consultez sécurité.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011412"
---
# <a name="msmq-security-services"></a>Services de sécurité MSMQ

Les messages RPC synchrones peuvent utiliser toutes les fonctionnalités de sécurité disponibles à partir de la durée d’exécution RPC. Pour plus d’informations, consultez [sécurité](security.md) .

Les appels asynchrones de \[ [messages](/windows/desktop/Midl/message) \] ne peuvent pas utiliser la sécurité RPC, car il n’existe aucune négociation entre le client et le serveur. En fait, le serveur peut ne pas s’exécuter même au moment de l’appel. Pour accéder aux services de sécurité fournis par Message Queuinging services (MSMQ), l’application cliente doit appeler [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) pour contrôler le niveau d’authentification et de confidentialité pour ses appels au serveur.

L’application serveur peut appeler [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) à partir d’un appel de procédure distante pour déterminer le niveau de sécurité de cet appel. Le tableau suivant montre le mappage entre les constantes de sécurité RPC et la sécurité MSMQ.



| Niveau de sécurité RPC                | Description                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| \_niveau d’authentification \_ RPC \_ aucun           | L’appel n’est pas authentifié ou chiffré.                                                |
| \_ \_ intégrité PKT au niveau \_ de \_ l’authentification RPC | L’appel est authentifié à l’aide de la sécurité MSMQ.                                             |
| confidentialité du niveau d' \_ authentification RPC \_ \_ \_   | L’appel est authentifié et chiffré au fur et à mesure qu’il transite entre la file d’attente du client et du serveur. |



 

Le serveur peut également forcer l’authentification et le chiffrement de l’appel en appelant [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) et en définissant le niveau d’authentification RPC c MQ Authn, le niveau d’authentification et l’intégrité PKT du niveau d’authentification RPC c MQ \_ \_ \_ \_ \_ , \_ \_ \_ \_ \_ \_ ainsi que les \_ \_ \_ \_ indicateurs de confidentialité de niveau d’authentification RPC c MQ Authn \_ \_ dans la structure de la [**\_ stratégie RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) .

 

 