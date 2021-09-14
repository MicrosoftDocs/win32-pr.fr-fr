---
title: Écriture d’un client SSPI authentifié
description: Écriture d’un client SSPI authentifié et d’un appel de procédure distante (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- Appel de procédure distante RPC, tâches, écriture d’un client SSPI authentifié
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013824"
---
# <a name="writing-an-authenticated-sspi-client"></a>Écriture d’un client SSPI authentifié

Toutes les sessions client/serveur RPC nécessitent une liaison entre le client et le serveur. Pour ajouter la sécurité aux applications client/serveur, les programmes doivent utiliser une liaison authentifiée. Cette section décrit le processus de création d’une liaison authentifiée entre le client et le serveur.

-   [Création de handles de liaison côté client](#creating-client-side-binding-handles)
-   [Fournir les informations d’identification du client au serveur](#providing-client-credentials-to-the-server)

Pour obtenir des informations connexes, consultez [procédures utilisées avec la plupart des packages de sécurité et des protocoles](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) dans le kit de développement logiciel (SDK) de la plateforme.

## <a name="creating-client-side-binding-handles"></a>Création de handles de liaison côté client

Pour créer une session authentifiée avec un programme serveur, les applications clientes doivent fournir des informations d’authentification avec leur handle de liaison. Pour configurer un handle de liaison authentifié, les clients appellent la fonction [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) . Ces deux fonctions sont presque identiques. La seule différence réside dans le fait que le client peut spécifier la qualité de service avec la fonction **RpcBindingSetAuthInfoEx** .

Le fragment de code suivant montre comment un appel à [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) peut se présenter.


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



Une fois que le client a correctement appelé les fonctions [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) , la bibliothèque Runtime RPC authentifie automatiquement tous les appels RPC sur la liaison. Le niveau de sécurité et d’authentification que le client sélectionne s’applique uniquement à ce handle de liaison. Les handles de contexte dérivés du descripteur de liaison utiliseront les mêmes informations de sécurité, mais les modifications ultérieures apportées au handle de liaison ne seront pas reflétées dans les handles de contexte. Pour plus d’informations, consultez [Handles de contexte](context-handles.md).

Le niveau d’authentification reste effectif jusqu’à ce que le client choisisse un autre niveau ou jusqu’à ce que le processus se termine. La plupart des applications ne nécessitent pas de modification du niveau de sécurité. Le client peut interroger un handle de liaison pour obtenir ses informations d’autorisation en appelant [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) et en lui passant le handle de liaison.

## <a name="providing-client-credentials-to-the-server"></a>Fournir les informations d’identification du client au serveur

Les serveurs utilisent les informations de liaison du client pour assurer la sécurité. Les clients passent toujours un handle de liaison en tant que premier paramètre d’un appel de procédure distante. Toutefois, les serveurs ne peuvent pas utiliser le descripteur sauf s’ils sont déclarés en tant que premier paramètre des procédures distantes dans le fichier IDL ou dans le fichier de configuration d’application (ACF) du serveur. Vous pouvez choisir de répertorier le descripteur de liaison dans le fichier IDL, mais cela oblige tous les clients à déclarer et à manipuler le handle de liaison au lieu d’utiliser une liaison automatique ou implicite. Pour plus d’informations, consultez [les fichiers IDL et ACF](the-idl-and-acf-files.md).

Une autre méthode consiste à conserver les handles de liaison hors du fichier IDL et à placer l’attribut de **\_ handle explicite** dans le ACF du serveur. De cette façon, le client peut utiliser le type de liaison le mieux adapté à l’application, tandis que le serveur utilise le handle de liaison comme s’il avait été déclaré explicitement.

Le processus d’extraction des informations d’identification du client à partir du handle de liaison s’effectue comme suit :

-   Les clients RPC appellent [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) et incluent leurs informations d’authentification dans le cadre des informations de liaison transmises au serveur.
-   En règle générale, le serveur appelle [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) pour se comporter comme s’il s’agissait du client. Si le handle de liaison n’est pas authentifié, l’appel échoue avec RPC \_ S \_ aucun \_ contexte \_ disponible. pour obtenir le nom d’utilisateur du client, appelez [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) pendant l’emprunt d’identité, ou sur Windows XP ou les versions ultérieures de Windows, appelez [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) pour obtenir le contexte d’autorisation, puis utilisez les fonctions auth pour récupérer le nom.
-   Le serveur appellera normalement [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) pour créer des objets avec des ACL. Une fois cette étape accomplie, les contrôles de sécurité ultérieurs deviennent automatiques.

 

 