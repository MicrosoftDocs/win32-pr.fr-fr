---
title: Qualité de service (RPC)
description: Les programmes clients peuvent utiliser la fonction RpcBindingSetAuthInfoEx plutôt que la fonction RpcBindingSetAuthInfo pour créer une liaison authentifiée.
ms.assetid: bc3d47ba-3c1b-4aba-8fe3-b4501a621931
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee93b1aa376c9d6f4e2b3eedab73c91471d42498
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311462"
---
# <a name="quality-of-service-rpc"></a>Qualité de service (RPC)

Les programmes clients peuvent utiliser la fonction [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) plutôt que la fonction [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) pour créer une liaison authentifiée. Si c’est le cas, ils passent un pointeur vers une structure [**\_ \_ QoS de sécurité RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) comme paramètre final de **RpcBindingSetAuthInfoEx**. Cette structure contient des informations sur la qualité de service. Les programmes clients peuvent également spécifier le suivi des identités et sélectionner le type d’emprunt d’identité.

Utilisez les **fonctions** membres de la [**structure \_ \_ QoS de sécurité RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) pour définir les parties de l’application client/serveur qui doivent être authentifiées. Si la \_ \_ \_ \_ valeur par défaut des fonctionnalités de QoS RPC C est sélectionnée, la bibliothèque Runtime RPC authentifie le client ou le serveur en fonction de la valeur par défaut du fournisseur de services partagés. Par défaut, le SSP du protocole Kerberos authentifie à la fois le client et le serveur. La valeur par défaut pour tous les autres SSP fournis par Microsoft consiste à authentifier le client auprès du serveur, mais pas à authentifier le serveur auprès du client.

Si le client et le serveur doivent toujours s’authentifier entre eux, définissez le membre **capacités** de la structure [**\_ \_ QoS de sécurité RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) sur \_ fonctionnalités RPC C \_ QoS \_ \_ \_ authentification mutuelle. Certains fournisseurs de sécurité peuvent ne pas prendre en charge l’authentification mutuelle. Si \_ \_ \_ \_ l’authentification mutuelle des fonctionnalités QoS C RPC \_ est spécifiée pour ces fournisseurs de sécurité, une erreur est retournée lorsqu’un appel de procédure distante est effectué. Lors de l’utilisation du SSP SCHANNEL, il est possible de définir le membre **Capabilities** sur les \_ fonctionnalités de QoS C RPC, \_ \_ \_ quelle que soit l' \_ autorité. Cette constante spécifie que le SSP doit valider l’appel de procédure distante même si l’autorité de certification qui a émis le certificat d’authentification du client ne se trouve pas dans le magasin de certificats racine du fournisseur de services partagés. La valeur par défaut consiste à rejeter le certificat si le fournisseur de services partagés ne reconnaît pas l’autorité de certification. L’autorité de certification est une société ou organisation indépendante, telle que VeriSign, qui émet des certificats d’authentification.

Les applications peuvent également définir le suivi des identités utilisé par la bibliothèque Runtime RPC. Les programmes utilisent généralement le [*suivi statique des identités*](s-glos.md). Avec le suivi statique, les informations d’identification du client sont définies lors de l’appel de la fonction [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) . La bibliothèque Runtime RPC utilise ensuite ces informations d’identification pour tous les appels RPC sur la liaison, indépendamment des modifications apportées à l’identité du thread appelant ou au processus appelant. Les applications peuvent également sélectionner le [*suivi des identités dynamiques*](d-glos.md). Le suivi dynamique des identités indique à la bibliothèque Runtime RPC d’utiliser les informations d’identification du thread appelant au moment de chaque appel, plutôt que le handle de liaison. Le suivi d’identité par défaut est statique.

Si l’identité du client n’est pas modifiée, le suivi des identités statiques peut avoir de meilleures caractéristiques de performances et peut enregistrer la durée d’exécution du RPC à partir de chaque fois que l’identité sur le thread appelant est identique à l’identité donnée au système de sécurité. Si l’identité du thread appelant peut changer d’un appel à l’autre, et que le serveur doit reconnaître ces modifications, il est préférable de spécifier le suivi dynamique des identités : le temps d’exécution RPC est en silence et suivi efficacement de l’identité pour vous et, si l’identité change, gère cette modification en votre nom.

> [!Note]  
> Pour les appels **Ncalrpc** , le suivi des identités statiques et dynamiques présentent des caractéristiques de performances différentes et, selon les circonstances, elles peuvent être plus rapides.

 

Dans le cadre de la spécification QOS, le programme client peut également définir le type d’emprunt d’identité qu’un programme serveur peut effectuer en son nom. Pour plus d’informations, consultez [emprunt d’identité du client](client-impersonation.md).

Le champ du numéro de version de la structure [**\_ \_ QoS de sécurité RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) doit toujours être défini sur la \_ \_ version QoS de la sécurité C RPC \_ \_ .

 

 




