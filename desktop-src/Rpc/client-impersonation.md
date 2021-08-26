---
title: Emprunt d’identité du client (RPC)
description: L’emprunt d’identité est utile dans un environnement informatique distribué lorsque les serveurs doivent transmettre les demandes des clients à d’autres processus serveur ou au système d’exploitation.
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73061a35c61a22a4d238e902c3dcb298e3ac0affaf4b0929c83311145a684f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022822"
---
# <a name="client-impersonation"></a>Emprunt d'identité de client

L’emprunt d’identité est utile dans un environnement informatique distribué lorsque les serveurs doivent transmettre les demandes des clients à d’autres processus serveur ou au système d’exploitation. Dans ce cas, un serveur emprunte l’identité du contexte de sécurité du client. D’autres processus serveur peuvent ensuite traiter la demande comme si le client d’origine l’a effectuée.

![le serveur emprunte l’identité d’un client appelant lors des appels suivants au nom du client](images/impr.png)

Par exemple, un client envoie une demande au serveur A. Si le serveur A doit interroger le serveur B pour terminer la demande, le serveur A emprunte l’identité du contexte de sécurité du client et effectue la demande au serveur B pour le compte du client. Le serveur B utilise le contexte de sécurité du client d’origine, au lieu de l’identité de sécurité du serveur A, pour déterminer s’il faut terminer la tâche.

Le serveur appelle [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) pour remplacer la sécurité du thread de serveur par le contexte de sécurité du client. Une fois la tâche terminée, le serveur appelle [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) ou [**RpcRevertToSelfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) pour restaurer le contexte de sécurité défini pour le thread serveur.

Lors de la liaison, le client peut spécifier des informations de qualité de service sur la sécurité, qui spécifie comment le serveur peut emprunter l’identité du client. Par exemple, l’un des paramètres permet au client de spécifier que le serveur n’est pas autorisé à emprunter l’identité du serveur. Pour plus d’informations, consultez [qualité de service](quality-of-service.md).

La possibilité d’appeler d’autres serveurs tout en empruntant l’identité du client d’origine est appelée *délégation*. Quand la délégation est utilisée, un serveur qui emprunte l’identité d’un client peut appeler un autre serveur et peut effectuer des appels réseau avec les informations d’identification du client. Autrement dit, du point de vue du deuxième serveur, les demandes provenant du premier serveur ne sont pas différenciées des demandes provenant du client. Tous les fournisseurs de sécurité ne prennent pas en charge la délégation. Microsoft ne fournit qu’un seul fournisseur de sécurité qui prend en charge la délégation : Kerberos.

La délégation peut être une fonctionnalité dangereuse en raison des privilèges que le client donne au serveur lors d’un appel de procédure distante. C’est la raison pour laquelle Kerberos autorise les appels avec le niveau d’emprunt d’identité de délégation uniquement si une authentification mutuelle est demandée. Les administrateurs de domaine peuvent limiter les ordinateurs auxquels des appels avec un niveau d’emprunt d’identité de délégation sont effectués pour empêcher les clients insoupçonnés d’effectuer des appels à des serveurs qui pourraient abuser de leurs informations d’identification.

Il existe une exception à la règle de délégation : appels à l’aide de [**Ncalrpc**](/windows/desktop/Midl/ncalrpc). Lorsque ces appels sont rendus, le serveur obtient des droits de délégation, même si un niveau d’emprunt d’identité d’emprunt d’identité est spécifié. Autrement dit, un serveur peut appeler d’autres serveurs pour le compte du client. Cela fonctionne pour un seul appel à distance. Par exemple, si le client A appelle le serveur local LB à l’aide de **Ncalrpc** local, le serveur local lb peut emprunter l’identité et appeler le serveur distant RB. Le RB peut agir pour le compte du client A, mais uniquement sur l’ordinateur distant sur lequel le RB s’exécute. Il ne peut pas effectuer un autre appel réseau vers l’ordinateur distant C à moins que LB ne spécifie un niveau d’emprunt d’identité de délégué lorsqu’il a appelé RB.

> [!Note]  
> Le terme *emprunt d’identité* représente deux significations qui se chevauchent. La première signification de l’emprunt d’identité est le processus général d’action pour le compte d’un client. La deuxième signification est le niveau d’emprunt d’identité spécifique appelé emprunt d’identité. Le contexte du texte clarifie généralement la signification.

 

 

 