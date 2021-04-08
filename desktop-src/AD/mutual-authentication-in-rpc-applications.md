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
# <a name="mutual-authentication-in-rpc-applications"></a><span data-ttu-id="da097-105">Authentification mutuelle dans les applications RPC</span><span class="sxs-lookup"><span data-stu-id="da097-105">Mutual Authentication in RPC Applications</span></span>

<span data-ttu-id="da097-106">Les services RPC peuvent utiliser des points de connexion de service pour se publier eux-mêmes, ou ils peuvent utiliser les API de service de noms RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="da097-106">RPC services can use service connection points to publish themselves, or they can use the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="da097-107">Cette rubrique explique comment effectuer une authentification mutuelle avec un service RPC qui se publie lui-même à l’aide des API RpcNs (RPC Name Service).</span><span class="sxs-lookup"><span data-stu-id="da097-107">This topic discusses how to perform mutual authentication with an RPC service that publishes itself using the RPC name service (RpcNs) APIs.</span></span>

<span data-ttu-id="da097-108">**Pour inscrire un SPN dans le répertoire**</span><span class="sxs-lookup"><span data-stu-id="da097-108">**To register an SPN in the directory**</span></span>

1.  <span data-ttu-id="da097-109">Appelez la fonction [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) pour composer un nom de principal du service (SPN) pour le service.</span><span class="sxs-lookup"><span data-stu-id="da097-109">Call the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose a service principal name (SPN) for the service.</span></span>
2.  <span data-ttu-id="da097-110">Appelez la fonction [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) pour inscrire le SPN sur le compte de service ou le compte d’ordinateur dans le contexte duquel le service s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="da097-110">Call the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function to register the SPN on the service account or computer account in whose context the service will run.</span></span>

<span data-ttu-id="da097-111">**Pour inscrire un service auprès du service RPC Naming Service**</span><span class="sxs-lookup"><span data-stu-id="da097-111">**To register a service with the RPC naming service**</span></span>

1.  <span data-ttu-id="da097-112">Vérifiez que les SPN appropriés sont enregistrés sur le compte sous lequel le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="da097-112">Verify that the appropriate SPNs are registered on the account under which the service is running.</span></span> <span data-ttu-id="da097-113">Pour plus d’informations, consultez [tâches de maintenance de compte d’ouverture de session](logon-account-maintenance-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="da097-113">For more information, see [Logon Account Maintenance Tasks](logon-account-maintenance-tasks.md).</span></span>
2.  <span data-ttu-id="da097-114">Appelez la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) pour inscrire le SPN du service auprès du service d’authentification RPC, et spécifiez **RPC \_ C \_ Authn \_ GSS \_ Negotiate** comme service d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="da097-114">Call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function to register the service SPN with the RPC authentication service, and specify **RPC\_C\_AUTHN\_GSS\_NEGOTIATE** as the authentication service to use.</span></span>

<span data-ttu-id="da097-115">Pour plus d’informations sur l’exécution d’une authentification mutuelle dans un service RPC, voir [écriture d’un serveur SSPI authentifié](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span><span class="sxs-lookup"><span data-stu-id="da097-115">For more information about performing mutual authentication in an RPC service, see [Writing an Authenticated SSPI Server](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span></span>

<span data-ttu-id="da097-116">**Pour authentifier le service à partir du client**</span><span class="sxs-lookup"><span data-stu-id="da097-116">**To authenticate the service from the client**</span></span>

1.  <span data-ttu-id="da097-117">Extrayez le nom d’hôte de la liaison RPC.</span><span class="sxs-lookup"><span data-stu-id="da097-117">Extract the host name from the RPC Binding.</span></span>
2.  <span data-ttu-id="da097-118">Composez le SPN pour le service en appelant la fonction [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) avec la classe de service, le nom d’hôte DNS et le nom de service. Il s’agit du nom unique du point de connexion dans le cas de RpcNs.</span><span class="sxs-lookup"><span data-stu-id="da097-118">Compose the SPN for the service by calling the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function with the service class, the DNS host name, and the service name; that is the distinguished name of the connection point in the case of RpcNs.</span></span>

    <span data-ttu-id="da097-119">Pour plus d’informations sur la composition d’un SPN pour un service RpcNs, consultez [composition de SPN pour un service RpcNs](composing-spns-for-an-rpcns-service.md).</span><span class="sxs-lookup"><span data-stu-id="da097-119">For more information about composing an SPN for an RpcNs service, see [Composing SPNs for an RpcNs Service](composing-spns-for-an-rpcns-service.md).</span></span>

3.  <span data-ttu-id="da097-120">Configurez une structure [**\_ \_ QoS de sécurité RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) pour demander une authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="da097-120">Set up an [**RPC\_SECURITY\_QOS**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) structure to request mutual authentication.</span></span>
4.  <span data-ttu-id="da097-121">Appelez la fonction [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) pour définir les données d’authentification de la liaison RPC.</span><span class="sxs-lookup"><span data-stu-id="da097-121">Call the [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function to set the authentication data for the RPC binding.</span></span> <span data-ttu-id="da097-122">Le client doit demander au moins **\_ \_ \_ \_ \_ l’intégrité PKT du niveau d’authentification RPC C** pour s’assurer que les communications n’ont pas été falsifiées.</span><span class="sxs-lookup"><span data-stu-id="da097-122">The client must request at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY** to ensure that communications have not been tampered.</span></span> <span data-ttu-id="da097-123">Pour une sécurité accrue, le client doit spécifier la **\_ \_ \_ \_ \_ confidentialité du niveau Authn C RPC** pour demander le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="da097-123">For increased security, the client should specify **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** to request encryption.</span></span>
5.  <span data-ttu-id="da097-124">Exécutez l’appel RPC.</span><span class="sxs-lookup"><span data-stu-id="da097-124">Perform the RPC call.</span></span>

<span data-ttu-id="da097-125">Pour plus d’informations sur l’exécution de l’authentification mutuelle dans un client RPC, voir [écriture d’un client SSPI authentifié](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span><span class="sxs-lookup"><span data-stu-id="da097-125">For more information about performing mutual authentication in an RPC client, see [Writing an Authenticated SSPI Client](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span></span>

<span data-ttu-id="da097-126">**Pour authentifier le client à partir du service**</span><span class="sxs-lookup"><span data-stu-id="da097-126">**To authenticate the client from the service**</span></span>

1.  <span data-ttu-id="da097-127">Appelez la fonction [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) pour vérifier les paramètres d’authentification spécifiés par le client.</span><span class="sxs-lookup"><span data-stu-id="da097-127">Call the [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) function to verify the authentication parameters specified by the client.</span></span> <span data-ttu-id="da097-128">Si le client n’a pas demandé le niveau d’authentification souhaité, refusez l’appel.</span><span class="sxs-lookup"><span data-stu-id="da097-128">If the client has not requested the desired level of authentication, reject the call.</span></span> <span data-ttu-id="da097-129">N’oubliez pas qu’un service RPC doit vérifier le niveau d’authentification, le service d’authentification et l’identité du client à chaque appel pour s’assurer que le client a été correctement authentifié.</span><span class="sxs-lookup"><span data-stu-id="da097-129">Be aware that an RPC service must verify the authentication level, authentication service, and client identity on every call to ensure that the client has been properly authenticated.</span></span>
2.  <span data-ttu-id="da097-130">Appelez la fonction [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) pour emprunter l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="da097-130">Call the [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) function to impersonate the client.</span></span>
3.  <span data-ttu-id="da097-131">Exécutez l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="da097-131">Perform the requested operation.</span></span>
4.  <span data-ttu-id="da097-132">Appelez la fonction [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) pour rétablir le contexte de sécurité du service.</span><span class="sxs-lookup"><span data-stu-id="da097-132">Call the [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) function to revert to the service security context.</span></span>

<span data-ttu-id="da097-133">Pour plus d’informations sur l’emprunt d’identité du client RPC, consultez [emprunt d’identité du client](/windows/desktop/Rpc/client-impersonation).</span><span class="sxs-lookup"><span data-stu-id="da097-133">For more information about RPC client impersonation, see [Client Impersonation](/windows/desktop/Rpc/client-impersonation).</span></span>

<span data-ttu-id="da097-134">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="da097-134">For more information, see:</span></span>

-   [<span data-ttu-id="da097-135">Publication avec le service de noms RPC (RpcNs)</span><span class="sxs-lookup"><span data-stu-id="da097-135">Publishing with the RPC Name Service (RpcNs)</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="da097-136">Notions fondamentales de la sécurité RPC</span><span class="sxs-lookup"><span data-stu-id="da097-136">RPC Security Essentials</span></span>](/windows/desktop/Rpc/rpc-security-essentials)

 

 