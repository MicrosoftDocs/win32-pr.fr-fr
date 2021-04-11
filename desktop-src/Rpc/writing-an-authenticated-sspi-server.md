---
title: Écriture d’un serveur SSPI authentifié
description: Avant que la communication authentifiée puisse avoir lieu entre les programmes client et serveur, le serveur doit enregistrer ses informations d’authentification.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- Appel de procédure distante RPC, tâches, écriture d’un serveur SSPI authentifié
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029161"
---
# <a name="writing-an-authenticated-sspi-server"></a><span data-ttu-id="6351d-104">Écriture d’un serveur SSPI authentifié</span><span class="sxs-lookup"><span data-stu-id="6351d-104">Writing an Authenticated SSPI Server</span></span>

<span data-ttu-id="6351d-105">Avant que la communication authentifiée puisse avoir lieu entre les programmes client et serveur, le serveur doit enregistrer ses informations d’authentification.</span><span class="sxs-lookup"><span data-stu-id="6351d-105">Before authenticated communication can take place between the client and server programs, the server must register its authentication information.</span></span> <span data-ttu-id="6351d-106">En particulier, le serveur doit inscrire son nom principal et spécifier le service d’authentification qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="6351d-106">In particular, the server must register its principal name and specify the authentication service it uses.</span></span> <span data-ttu-id="6351d-107">Pour plus d’informations sur les noms principaux, consultez [noms principaux](principal-names.md).</span><span class="sxs-lookup"><span data-stu-id="6351d-107">For more information on principal names, see [Principal Names](principal-names.md).</span></span> <span data-ttu-id="6351d-108">Pour plus d’informations sur les services d’authentification, consultez [services d’authentification](authentication-services.md).</span><span class="sxs-lookup"><span data-stu-id="6351d-108">For details about authentication services, see [Authentication Services](authentication-services.md).</span></span>

<span data-ttu-id="6351d-109">Pour enregistrer ses informations d’authentification, les serveurs appellent la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) .</span><span class="sxs-lookup"><span data-stu-id="6351d-109">To register its authentication information, servers call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function.</span></span> <span data-ttu-id="6351d-110">Transmettez un pointeur vers le nom principal en tant que valeur du premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="6351d-110">Pass a pointer to the principal name as the value of the first parameter.</span></span> <span data-ttu-id="6351d-111">Définissez le deuxième paramètre sur une constante indiquant le service d’authentification que l’application utilisera.</span><span class="sxs-lookup"><span data-stu-id="6351d-111">Set the second parameter to a constant indicating the authentication service that the application will use.</span></span> <span data-ttu-id="6351d-112">Pour obtenir une description des services d’authentification, consultez la rubrique relative [aux constantes de service d’authentification](authentication-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6351d-112">For a description of authentication services, see [Authentication-Service Constants](authentication-service-constants.md).</span></span>

<span data-ttu-id="6351d-113">Le serveur peut également passer l’adresse d’une fonction d’acquisition de clé comme valeur du troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="6351d-113">The server may also pass the address of a key acquisition function as the value of the third parameter.</span></span> <span data-ttu-id="6351d-114">Consultez [fonctions d’acquisition de clés](key-acquisition-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6351d-114">See [Key Acquisition Functions](key-acquisition-functions.md).</span></span> <span data-ttu-id="6351d-115">Pour utiliser la fonction d’acquisition de clé par défaut pour le service d’authentification sélectionné, définissez le troisième paramètre sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6351d-115">To use the default key acquisition function for the selected authentication service, set the third parameter to **NULL**.</span></span> <span data-ttu-id="6351d-116">Le dernier paramètre de la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) est une donnée de pointeur à passer à la fonction d’acquisition de clé, si vous fournissez une fonction d’acquisition de clé.</span><span class="sxs-lookup"><span data-stu-id="6351d-116">The last parameter to the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function is a pointer data to pass to the key acquisition function, if you provide a key acquisition function.</span></span> <span data-ttu-id="6351d-117">Un appel à **RpcServerRegisterAuthInfo** est indiqué dans le fragment de code suivant.</span><span class="sxs-lookup"><span data-stu-id="6351d-117">A call to **RpcServerRegisterAuthInfo** is shown in the following code fragment.</span></span>


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



<span data-ttu-id="6351d-118">En outre, le serveur peut fournir la bibliothèque Runtime RPC avec une fonction d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="6351d-118">In addition, the server may provide the RPC run-time library with an authorization function.</span></span> <span data-ttu-id="6351d-119">Pour définir une fonction d’autorisation, appelez la fonction [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) .</span><span class="sxs-lookup"><span data-stu-id="6351d-119">To set an authorization function, call the [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) function.</span></span>

<span data-ttu-id="6351d-120">La partie serveur d’une application distribuée peut appeler la fonction [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) ou [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) pour interroger un handle de liaison afin d’obtenir des informations d’authentification.</span><span class="sxs-lookup"><span data-stu-id="6351d-120">The server portion of a distributed application can call the function [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to query a binding handle for authentication information.</span></span>

<span data-ttu-id="6351d-121">Si votre serveur s’inscrit auprès d’un fournisseur de support de sécurité, les appels clients avec des informations d’identification non valides ne seront pas distribués.</span><span class="sxs-lookup"><span data-stu-id="6351d-121">If your server registers with a security support provider, client calls with invalid credentials will not be dispatched.</span></span> <span data-ttu-id="6351d-122">Toutefois, les appels sans informations d’identification seront distribués.</span><span class="sxs-lookup"><span data-stu-id="6351d-122">However, calls with no credentials will be dispatched.</span></span> <span data-ttu-id="6351d-123">Il existe trois façons d’éviter ce problème :</span><span class="sxs-lookup"><span data-stu-id="6351d-123">There are three ways to prevent this from happening:</span></span>

-   <span data-ttu-id="6351d-124">Inscrire l’interface à l’aide de [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), avec une fonction de rappel de sécurité ; en conséquence, la bibliothèque Runtime RPC rejette automatiquement les appels non authentifiés à cette interface.</span><span class="sxs-lookup"><span data-stu-id="6351d-124">Register the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), with a security callback function; this will cause the RPC run-time library to automatically reject unauthenticated calls to that interface.</span></span> <span data-ttu-id="6351d-125">L’inscription d’une fonction de rappel est compatible avec d’autres méthodes de vérification des informations d’identification d’accès ; la fonction de rappel peut elle-même appeler les fonctions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)ou [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) , ou d’autres.</span><span class="sxs-lookup"><span data-stu-id="6351d-125">Registering a callback function is compatible with other methods of checking access credentials; the callback function can itself call the [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient), or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) functions, or others.</span></span> <span data-ttu-id="6351d-126">Toutefois, ces fonctions ne peuvent pas utiliser les arguments passés à la fonction, car ils ne sont pas démarshalés à ce stade.</span><span class="sxs-lookup"><span data-stu-id="6351d-126">However, these functions cannot use the arguments passed to the function, as they are not unmarshalled at that point.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6351d-127">L’inscription de l’interface à l’aide de [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) avec une fonction de rappel de sécurité est la méthode la plus fortement recommandée pour vérifier les informations d’identification du client.</span><span class="sxs-lookup"><span data-stu-id="6351d-127">Registering the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) with a security callback function is the most heavily recommended method of checking client credentials.</span></span>

 

-   <span data-ttu-id="6351d-128">Appelez [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) pour déterminer le niveau de sécurité utilisé par le client.</span><span class="sxs-lookup"><span data-stu-id="6351d-128">Call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) to determine the security level that the client is using.</span></span> <span data-ttu-id="6351d-129">Votre stub peut ensuite retourner une erreur si le client n’est pas authentifié.</span><span class="sxs-lookup"><span data-stu-id="6351d-129">Your stub can then return an error if the client is unauthenticated.</span></span>

 

 




