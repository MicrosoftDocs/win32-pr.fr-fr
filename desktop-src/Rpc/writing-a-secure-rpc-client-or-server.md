---
title: Écriture d’un client ou d’un serveur RPC sécurisé
description: Cette section présente les meilleures pratiques recommandées pour l’écriture d’un client ou d’un serveur RPC sécurisé.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- Appel de procédure distante RPC, meilleures pratiques, écriture d’un client ou d’un serveur sécurisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031603"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Écriture d’un client ou d’un serveur RPC sécurisé

Cette section présente les meilleures pratiques recommandées pour l’écriture d’un client ou d’un serveur RPC sécurisé.

Les informations contenues dans cette section s’appliquent à Windows 2000 et Windows XP. Cette section s’applique à toutes les séquences de protocole, y compris [**Ncalrpc**](/windows/desktop/Midl/ncalrpc). Les développeurs ont tendance à penser que **Ncalrpc** n’est pas une cible probable pour une attaque, ce qui n’est pas le cas sur un serveur Terminal Server où des centaines d’utilisateurs peuvent accéder à un service, et compromettre ou même arrêter un service peut aboutir à l’obtention d’un accès supplémentaire.

Cette section est composée des rubriques suivantes :

-   [Le fournisseur de sécurité à utiliser](which-security-provider-to-use.md)
-   [Contrôle de l’authentification du client](controlling-client-authentication.md)
-   [Choix d’un niveau d’authentification](choosing-an-authentication-level.md)
-   [Choix des options de QOS de sécurité](choosing-security-qos-options.md)
-   [Erreur courante : en supposant que RpcServerRegisterAuthInfo empêche les utilisateurs non autorisés d’appeler votre serveur](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Rappels](callbacks.md)
-   [Sessions null](null-sessions.md)
-   [Utiliser l’indicateur/Robust](use-the-robust-flag.md)
-   [Techniques IDL pour une meilleure conception d’interface et de méthode](idl-techniques-for-better-interface-and-method-design.md)
-   [Handles de contexte strict et strict](strict-and-type-strict-context-handles.md)
-   [Ne pas faire confiance à votre homologue](do-not-trust-your-peer.md)
-   [Ne pas utiliser la sécurité du point de terminaison](do-not-use-endpoint-security.md)
-   [Méfiez-vous des autres points de terminaison RPC s’exécutant dans le même processus](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Vérifier que le serveur est bien celui qu’il prétend être](verify-the-server-is-who-it-claims-to-be.md)
-   [Utiliser des séquences de protocole courantes](use-mainstream-protocol-sequences.md)
-   [Quelle est la sécurité de mon serveur RPC maintenant ?](how-secure-is-my-rpc-server-now.md)

 

 