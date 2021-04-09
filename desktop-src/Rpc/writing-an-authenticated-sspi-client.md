---
title: Écriture d’un client SSPI authentifié
description: Écriture d’un client SSPI authentifié et d’un appel de procédure distante (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- Appel de procédure distante RPC, tâches, écriture d’un client SSPI authentifié
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102028"
---
# <a name="writing-an-authenticated-sspi-client"></a><span data-ttu-id="b064f-104">Écriture d’un client SSPI authentifié</span><span class="sxs-lookup"><span data-stu-id="b064f-104">Writing an Authenticated SSPI Client</span></span>

<span data-ttu-id="b064f-105">Toutes les sessions client/serveur RPC nécessitent une liaison entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b064f-105">All RPC client/server sessions require a binding between the client and the server.</span></span> <span data-ttu-id="b064f-106">Pour ajouter la sécurité aux applications client/serveur, les programmes doivent utiliser une liaison authentifiée.</span><span class="sxs-lookup"><span data-stu-id="b064f-106">To add security to client/server applications, the programs must use an authenticated binding.</span></span> <span data-ttu-id="b064f-107">Cette section décrit le processus de création d’une liaison authentifiée entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b064f-107">This section describes the process of creating an authenticated binding between the client and the server.</span></span>

-   [<span data-ttu-id="b064f-108">Création de handles de liaison côté client</span><span class="sxs-lookup"><span data-stu-id="b064f-108">Creating Client-side Binding Handles</span></span>](#creating-client-side-binding-handles)
-   [<span data-ttu-id="b064f-109">Fournir les informations d’identification du client au serveur</span><span class="sxs-lookup"><span data-stu-id="b064f-109">Providing Client Credentials to the Server</span></span>](#providing-client-credentials-to-the-server)

<span data-ttu-id="b064f-110">Pour obtenir des informations connexes, consultez [procédures utilisées avec la plupart des packages de sécurité et des protocoles](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="b064f-110">For related information, see [Procedures Used with Most Security Packages and Protocols](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) in the Platform Software Development Kit (SDK).</span></span>

## <a name="creating-client-side-binding-handles"></a><span data-ttu-id="b064f-111">Création de handles de liaison côté client</span><span class="sxs-lookup"><span data-stu-id="b064f-111">Creating Client-side Binding Handles</span></span>

<span data-ttu-id="b064f-112">Pour créer une session authentifiée avec un programme serveur, les applications clientes doivent fournir des informations d’authentification avec leur handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="b064f-112">To create an authenticated session with a server program, client applications must provide authentication information with their binding handle.</span></span> <span data-ttu-id="b064f-113">Pour configurer un handle de liaison authentifié, les clients appellent la fonction [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="b064f-113">To set up an authenticated binding handle, clients invoke the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function.</span></span> <span data-ttu-id="b064f-114">Ces deux fonctions sont presque identiques.</span><span class="sxs-lookup"><span data-stu-id="b064f-114">These two functions are nearly identical.</span></span> <span data-ttu-id="b064f-115">La seule différence réside dans le fait que le client peut spécifier la qualité de service avec la fonction **RpcBindingSetAuthInfoEx** .</span><span class="sxs-lookup"><span data-stu-id="b064f-115">The only difference between them is that the client can specify the quality of service with the **RpcBindingSetAuthInfoEx** function.</span></span>

<span data-ttu-id="b064f-116">Le fragment de code suivant montre comment un appel à [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) peut se présenter.</span><span class="sxs-lookup"><span data-stu-id="b064f-116">The following code fragment shows how a call to [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) might look.</span></span>


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



<span data-ttu-id="b064f-117">Une fois que le client a correctement appelé les fonctions [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) , la bibliothèque Runtime RPC authentifie automatiquement tous les appels RPC sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="b064f-117">After the client successfully calls the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) functions, the RPC run-time library automatically authenticates all RPC calls on the binding.</span></span> <span data-ttu-id="b064f-118">Le niveau de sécurité et d’authentification que le client sélectionne s’applique uniquement à ce handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="b064f-118">The level of security and authentication that the client selects applies only to that binding handle.</span></span> <span data-ttu-id="b064f-119">Les handles de contexte dérivés du descripteur de liaison utiliseront les mêmes informations de sécurité, mais les modifications ultérieures apportées au handle de liaison ne seront pas reflétées dans les handles de contexte.</span><span class="sxs-lookup"><span data-stu-id="b064f-119">Context handles derived from the binding handle will use the same security information, but subsequent modifications to the binding handle will not be reflected in the context handles.</span></span> <span data-ttu-id="b064f-120">Pour plus d’informations, consultez [Handles de contexte](context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="b064f-120">For more information, see [Context Handles](context-handles.md).</span></span>

<span data-ttu-id="b064f-121">Le niveau d’authentification reste effectif jusqu’à ce que le client choisisse un autre niveau ou jusqu’à ce que le processus se termine.</span><span class="sxs-lookup"><span data-stu-id="b064f-121">The authentication level stays in effect until the client chooses another level, or until the process terminates.</span></span> <span data-ttu-id="b064f-122">La plupart des applications ne nécessitent pas de modification du niveau de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b064f-122">Most applications will not require a change in the security level.</span></span> <span data-ttu-id="b064f-123">Le client peut interroger un handle de liaison pour obtenir ses informations d’autorisation en appelant [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) et en lui passant le handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="b064f-123">The client can query any binding handle to obtain its authorization information by invoking [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) and passing it the binding handle.</span></span>

## <a name="providing-client-credentials-to-the-server"></a><span data-ttu-id="b064f-124">Fournir les informations d’identification du client au serveur</span><span class="sxs-lookup"><span data-stu-id="b064f-124">Providing Client Credentials to the Server</span></span>

<span data-ttu-id="b064f-125">Les serveurs utilisent les informations de liaison du client pour assurer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="b064f-125">Servers use the client's binding information to enforce security.</span></span> <span data-ttu-id="b064f-126">Les clients passent toujours un handle de liaison en tant que premier paramètre d’un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="b064f-126">Clients always pass a binding handle as the first parameter of a remote procedure call.</span></span> <span data-ttu-id="b064f-127">Toutefois, les serveurs ne peuvent pas utiliser le descripteur sauf s’ils sont déclarés en tant que premier paramètre des procédures distantes dans le fichier IDL ou dans le fichier de configuration d’application (ACF) du serveur.</span><span class="sxs-lookup"><span data-stu-id="b064f-127">However, servers cannot use the handle unless it is declared as the first parameter to remote procedures in either the IDL file or in the server's application configuration file (ACF).</span></span> <span data-ttu-id="b064f-128">Vous pouvez choisir de répertorier le descripteur de liaison dans le fichier IDL, mais cela oblige tous les clients à déclarer et à manipuler le handle de liaison au lieu d’utiliser une liaison automatique ou implicite.</span><span class="sxs-lookup"><span data-stu-id="b064f-128">You can choose to list the binding handle in the IDL file, but this forces all clients to declare and manipulate the binding handle rather than using automatic or implicit binding.</span></span> <span data-ttu-id="b064f-129">Pour plus d’informations, consultez [les fichiers IDL et ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="b064f-129">For further information, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="b064f-130">Une autre méthode consiste à conserver les handles de liaison hors du fichier IDL et à placer l’attribut de **\_ handle explicite** dans le ACF du serveur.</span><span class="sxs-lookup"><span data-stu-id="b064f-130">Another method is to leave the binding handles out of the IDL file and to place the **explicit\_handle** attribute into the server's ACF.</span></span> <span data-ttu-id="b064f-131">De cette façon, le client peut utiliser le type de liaison le mieux adapté à l’application, tandis que le serveur utilise le handle de liaison comme s’il avait été déclaré explicitement.</span><span class="sxs-lookup"><span data-stu-id="b064f-131">In this way, the client can use the type of binding best suited to the application, while the server uses the binding handle as though it were declared explicitly.</span></span>

<span data-ttu-id="b064f-132">Le processus d’extraction des informations d’identification du client à partir du handle de liaison s’effectue comme suit :</span><span class="sxs-lookup"><span data-stu-id="b064f-132">The process of extracting the client credentials from the binding handle occurs as follows:</span></span>

-   <span data-ttu-id="b064f-133">Les clients RPC appellent [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) et incluent leurs informations d’authentification dans le cadre des informations de liaison transmises au serveur.</span><span class="sxs-lookup"><span data-stu-id="b064f-133">RPC clients call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) and include their authentication information as part of the binding information passed to the server.</span></span>
-   <span data-ttu-id="b064f-134">En règle générale, le serveur appelle [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) pour se comporter comme s’il s’agissait du client.</span><span class="sxs-lookup"><span data-stu-id="b064f-134">Usually, the server calls [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) in order to behave as though it were the client.</span></span> <span data-ttu-id="b064f-135">Si le handle de liaison n’est pas authentifié, l’appel échoue avec RPC \_ S \_ aucun \_ contexte \_ disponible.</span><span class="sxs-lookup"><span data-stu-id="b064f-135">If the binding handle is not authenticated, the call fails with RPC\_S\_NO\_CONTEXT\_AVAILABLE.</span></span> <span data-ttu-id="b064f-136">Pour obtenir le nom d’utilisateur du client, appelez [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) lors de l’emprunt d’identité, ou sous Windows XP ou versions ultérieures de Windows, appelez [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) pour obtenir le contexte d’autorisation, puis utilisez les fonctions auth pour récupérer le nom.</span><span class="sxs-lookup"><span data-stu-id="b064f-136">To obtain the client's user name, call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) while impersonating, or on Windows XP or later versions of Windows, call [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) to get the authorization context, then use Authz functions to retrieve the name.</span></span>
-   <span data-ttu-id="b064f-137">Le serveur appellera normalement [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) pour créer des objets avec des ACL.</span><span class="sxs-lookup"><span data-stu-id="b064f-137">The server will normally call [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) to create objects with ACLs.</span></span> <span data-ttu-id="b064f-138">Une fois cette étape accomplie, les contrôles de sécurité ultérieurs deviennent automatiques.</span><span class="sxs-lookup"><span data-stu-id="b064f-138">After this is accomplished, later security checks become automatic.</span></span>

 

 