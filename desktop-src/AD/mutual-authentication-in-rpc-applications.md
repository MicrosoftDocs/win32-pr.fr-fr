---
title: Authentification mutuelle dans les applications RPC
description: Les services RPC peuvent utiliser des points de connexion de service pour se publier eux-mêmes, ou ils peuvent utiliser les API de service de noms RPC (RpcNs).
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Authentification mutuelle dans AD applications RPC
- Active Directory, utilisation de, authentification mutuelle, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842058"
---
# <a name="mutual-authentication-in-rpc-applications"></a>Authentification mutuelle dans les applications RPC

Les services RPC peuvent utiliser des points de connexion de service pour se publier eux-mêmes, ou ils peuvent utiliser les API de service de noms RPC (RpcNs). Cette rubrique explique comment effectuer une authentification mutuelle avec un service RPC qui se publie lui-même à l’aide des API RpcNs (RPC Name Service).

**Pour inscrire un SPN dans le répertoire**

1.  Appelez la fonction [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) pour composer un nom de principal du service (SPN) pour le service.
2.  Appelez la fonction [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) pour inscrire le SPN sur le compte de service ou le compte d’ordinateur dans le contexte duquel le service s’exécutera.

**Pour inscrire un service auprès du service RPC Naming Service**

1.  Vérifiez que les SPN appropriés sont enregistrés sur le compte sous lequel le service est en cours d’exécution. Pour plus d’informations, consultez [tâches de maintenance de compte d’ouverture de session](logon-account-maintenance-tasks.md).
2.  Appelez la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) pour inscrire le SPN du service auprès du service d’authentification RPC, et spécifiez **RPC \_ C \_ Authn \_ GSS \_ Negotiate** comme service d’authentification à utiliser.

Pour plus d’informations sur l’exécution d’une authentification mutuelle dans un service RPC, voir [écriture d’un serveur SSPI authentifié](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).

**Pour authentifier le service à partir du client**

1.  Extrayez le nom d’hôte de la liaison RPC.
2.  Composez le SPN pour le service en appelant la fonction [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) avec la classe de service, le nom d’hôte DNS et le nom de service. Il s’agit du nom unique du point de connexion dans le cas de RpcNs.

    Pour plus d’informations sur la composition d’un SPN pour un service RpcNs, consultez [composition de SPN pour un service RpcNs](composing-spns-for-an-rpcns-service.md).

3.  Configurez une structure [**\_ \_ QoS de sécurité RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) pour demander une authentification mutuelle.
4.  Appelez la fonction [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) pour définir les données d’authentification de la liaison RPC. Le client doit demander au moins **\_ \_ \_ \_ \_ l’intégrité PKT du niveau d’authentification RPC C** pour s’assurer que les communications n’ont pas été falsifiées. Pour une sécurité accrue, le client doit spécifier la **\_ \_ \_ \_ \_ confidentialité du niveau Authn C RPC** pour demander le chiffrement.
5.  Exécutez l’appel RPC.

Pour plus d’informations sur l’exécution de l’authentification mutuelle dans un client RPC, voir [écriture d’un client SSPI authentifié](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).

**Pour authentifier le client à partir du service**

1.  Appelez la fonction [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) pour vérifier les paramètres d’authentification spécifiés par le client. Si le client n’a pas demandé le niveau d’authentification souhaité, refusez l’appel. N’oubliez pas qu’un service RPC doit vérifier le niveau d’authentification, le service d’authentification et l’identité du client à chaque appel pour s’assurer que le client a été correctement authentifié.
2.  Appelez la fonction [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) pour emprunter l’identité du client.
3.  Exécutez l’opération demandée.
4.  Appelez la fonction [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) pour rétablir le contexte de sécurité du service.

Pour plus d’informations sur l’emprunt d’identité du client RPC, consultez [emprunt d’identité du client](/windows/desktop/Rpc/client-impersonation).

Pour plus d’informations, consultez :

-   [Publication avec le service de noms RPC (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md)
-   [Notions fondamentales de la sécurité RPC](/windows/desktop/Rpc/rpc-security-essentials)

 

 