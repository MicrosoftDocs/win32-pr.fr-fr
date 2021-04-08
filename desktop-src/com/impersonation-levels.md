---
title: Niveaux d’emprunt d’identité (COM)
description: Si l’emprunt d’identité s’effectue correctement, cela signifie que le client a accepté de laisser le serveur être le client dans une certaine mesure.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842750"
---
# <a name="impersonation-levels"></a><span data-ttu-id="21b66-103">Niveaux d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="21b66-103">Impersonation Levels</span></span>

<span data-ttu-id="21b66-104">Si l’emprunt d’identité s’effectue correctement, cela signifie que le client a accepté de laisser le serveur être le client dans une certaine mesure.</span><span class="sxs-lookup"><span data-stu-id="21b66-104">If impersonation succeeds, it means that the client has agreed to let the server be the client to some degree.</span></span> <span data-ttu-id="21b66-105">Les différents degrés d’emprunt d’identité sont appelés « *niveaux d’emprunt d’identité*» et indiquent la quantité d’autorité accordée au serveur lorsqu’il emprunte l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="21b66-105">The varying degrees of impersonation are called *impersonation levels*, and they indicate how much authority is given to the server when it is impersonating the client.</span></span>

<span data-ttu-id="21b66-106">Actuellement, il existe quatre niveaux d’emprunt d’identité : *anonyme*, *identifier*, *emprunter l’identité* et *déléguer*.</span><span class="sxs-lookup"><span data-stu-id="21b66-106">Currently, there are four impersonation levels: *anonymous*, *identify*, *impersonate*, and *delegate*.</span></span> <span data-ttu-id="21b66-107">La liste suivante décrit brièvement chaque niveau d’emprunt d’identité :</span><span class="sxs-lookup"><span data-stu-id="21b66-107">The following list briefly describes each impersonation level:</span></span>

<dl> <dt>

<span data-ttu-id="21b66-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>Anonyme (RPC \_ C \_ IMP \_ niveau \_ Anonymous)</span><span class="sxs-lookup"><span data-stu-id="21b66-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC\_C\_IMP\_LEVEL\_ANONYMOUS)</span></span>
</dt> <dd>

<span data-ttu-id="21b66-109">Le client est anonyme au serveur.</span><span class="sxs-lookup"><span data-stu-id="21b66-109">The client is anonymous to the server.</span></span> <span data-ttu-id="21b66-110">Le processus serveur peut emprunter l'identité du client, mais le jeton d'emprunt d'identité ne contient pas d'informations sur le client.</span><span class="sxs-lookup"><span data-stu-id="21b66-110">The server process can impersonate the client, but the impersonation token does not contain any information about the client.</span></span> <span data-ttu-id="21b66-111">Ce niveau est pris en charge uniquement sur le transport de communication interprocessus local.</span><span class="sxs-lookup"><span data-stu-id="21b66-111">This level is only supported over the local interprocess communication transport.</span></span> <span data-ttu-id="21b66-112">Tous les autres transports promeuvent silencieusement ce niveau pour identifier.</span><span class="sxs-lookup"><span data-stu-id="21b66-112">All other transports silently promote this level to identify.</span></span>

</dd> <dt>

<span data-ttu-id="21b66-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identifier ( \_ identification du \_ niveau d’IMP RPC C \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="21b66-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC\_C\_IMP\_LEVEL\_IDENTIFY)</span></span>
</dt> <dd>

<span data-ttu-id="21b66-114">Niveau par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="21b66-114">The system default level.</span></span> <span data-ttu-id="21b66-115">Le serveur peut obtenir l'identité du client et peut emprunter l'identité du client pour vérifier des listes ACL.</span><span class="sxs-lookup"><span data-stu-id="21b66-115">The server can obtain the client's identity, and the server can impersonate the client to do ACL checks.</span></span>

</dd> <dt>

<span data-ttu-id="21b66-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>Impersonate (RPC \_ C \_ IMP \_ niveau \_ Impersonate)</span><span class="sxs-lookup"><span data-stu-id="21b66-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC\_C\_IMP\_LEVEL\_IMPERSONATE)</span></span>
</dt> <dd>

<span data-ttu-id="21b66-117">Le serveur peut emprunter l'identité du contexte de sécurité du client tout en agissant au nom du client.</span><span class="sxs-lookup"><span data-stu-id="21b66-117">The server can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="21b66-118">Le serveur peut accéder aux ressources locales sous l'identité du client.</span><span class="sxs-lookup"><span data-stu-id="21b66-118">The server can access local resources as the client.</span></span> <span data-ttu-id="21b66-119">Si le serveur est local, il peut accéder aux ressources réseau en tant que client.</span><span class="sxs-lookup"><span data-stu-id="21b66-119">If the server is local, it can access network resources as the client.</span></span> <span data-ttu-id="21b66-120">Si le serveur est distant, il ne peut accéder qu’aux ressources qui se trouvent sur le même ordinateur que le serveur.</span><span class="sxs-lookup"><span data-stu-id="21b66-120">If the server is remote, it can access only resources that are on the same computer as the server.</span></span>

</dd> <dt>

<span data-ttu-id="21b66-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>délégué ( \_ délégué de \_ niveau IMP RPC c \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="21b66-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (RPC\_C\_IMP\_LEVEL\_DELEGATE)</span></span>
</dt> <dd>

<span data-ttu-id="21b66-122">Niveau d'emprunt d'identité le plus puissant.</span><span class="sxs-lookup"><span data-stu-id="21b66-122">The most powerful impersonation level.</span></span> <span data-ttu-id="21b66-123">Quand ce niveau est sélectionné, le serveur (local ou distant) peut emprunter l’identité du contexte de sécurité du client tout en agissant au nom du client.</span><span class="sxs-lookup"><span data-stu-id="21b66-123">When this level is selected, the server (whether local or remote) can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="21b66-124">Pendant l’emprunt d’identité, les informations d’identification du client (locales et réseau) peuvent être transmises à un nombre quelconque d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="21b66-124">During impersonation, the client's credentials (both local and network) can be passed to any number of computers.</span></span>

<span data-ttu-id="21b66-125">Pour que l’emprunt d’identité fonctionne au niveau du délégué, les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="21b66-125">For impersonation to work at the delegate level, the following requirements must be met:</span></span>

-   <span data-ttu-id="21b66-126">Le client doit définir le niveau d’emprunt d’identité sur \_ le \_ délégué de niveau IMP RPC C \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="21b66-126">The client must set the impersonation level to RPC\_C\_IMP\_LEVEL\_DELEGATE.</span></span>
-   <span data-ttu-id="21b66-127">Le compte client ne doit pas être marqué « le compte est sensible et ne peut pas être délégué » dans le service Active Directory.</span><span class="sxs-lookup"><span data-stu-id="21b66-127">The client account must not be marked "Account is sensitive and cannot be delegated" in the Active Directory Service.</span></span>
-   <span data-ttu-id="21b66-128">Le compte de serveur doit être marqué avec l’attribut « approuvé pour la délégation » dans le service Active Directory.</span><span class="sxs-lookup"><span data-stu-id="21b66-128">The server account must be marked with the "Trusted for delegation" attribute in the Active Directory Service.</span></span>
-   <span data-ttu-id="21b66-129">Les ordinateurs qui hébergent le client, le serveur et tous les serveurs « en aval » doivent tous être en cours d’exécution dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="21b66-129">The computers hosting the client, the server, and any "downstream" servers must all be running in a domain.</span></span>

</dd> </dl>

<span data-ttu-id="21b66-130">En choisissant le niveau d’emprunt d’identité, le client indique au serveur la manière dont il peut emprunter l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="21b66-130">By choosing the impersonation level, the client tells the server how far it can go in impersonating the client.</span></span> <span data-ttu-id="21b66-131">Le client définit le niveau d’emprunt d’identité sur le proxy qu’il utilise pour communiquer avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="21b66-131">The client sets the impersonation level on the proxy it uses to communicate with the server.</span></span>

## <a name="setting-the-impersonation-level"></a><span data-ttu-id="21b66-132">Définition du niveau d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="21b66-132">Setting the Impersonation Level</span></span>

<span data-ttu-id="21b66-133">Il existe deux façons de définir le niveau d’emprunt d’identité :</span><span class="sxs-lookup"><span data-stu-id="21b66-133">There are two ways to set the impersonation level:</span></span>

-   <span data-ttu-id="21b66-134">Le client peut le définir échelle, à l’aide d’un appel à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="21b66-134">The client can set it processwide, through a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="21b66-135">Un client peut définir la sécurité au niveau du proxy sur une interface d’un objet distant par le biais d’un appel à [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (ou à la fonction d’assistance [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span><span class="sxs-lookup"><span data-stu-id="21b66-135">A client can set proxy-level security on an interface of a remote object through a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (or the helper function [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span></span>

<span data-ttu-id="21b66-136">Vous définissez le niveau d’emprunt d’identité en passant une \_ \_ valeur de niveau d’IMP RPC appropriée \_ \_ à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) via le paramètre *dwImpLevel* .</span><span class="sxs-lookup"><span data-stu-id="21b66-136">You set the impersonation level by passing an appropriate RPC\_C\_IMP\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwImpLevel* parameter.</span></span>

<span data-ttu-id="21b66-137">Les différents services d’authentification prennent en charge l’emprunt d’identité au niveau du délégué sur des étendues différentes.</span><span class="sxs-lookup"><span data-stu-id="21b66-137">Different authentication services support delegate-level impersonation to different extents.</span></span> <span data-ttu-id="21b66-138">Par exemple, NTLMSSP prend en charge l’emprunt d’identité au niveau du délégué inter-threads et interprocessus, mais pas entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="21b66-138">For instance, NTLMSSP supports cross-thread and cross-process delegate-level impersonation, but not cross-computer.</span></span> <span data-ttu-id="21b66-139">En revanche, le protocole Kerberos prend en charge l’emprunt d’identité au niveau du délégué au-delà des limites de l’ordinateur, tandis que Schannel ne prend pas en charge l’emprunt d’identité au niveau du délégué.</span><span class="sxs-lookup"><span data-stu-id="21b66-139">On the other hand, the Kerberos protocol supports delegate-level impersonation across computer boundaries, while Schannel does not support any impersonation at the delegate level.</span></span> <span data-ttu-id="21b66-140">Si vous avez un proxy à un niveau d’emprunt d’identité et que vous souhaitez définir le niveau d’emprunt d’identité à déléguer, vous devez appeler [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) à l’aide des constantes par défaut pour chaque paramètre, à l’exception du niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="21b66-140">If you have a proxy at impersonate level and you want to set the impersonation level to delegate, you should call [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) using the default constants for every parameter except the impersonation level.</span></span> <span data-ttu-id="21b66-141">COM choisit NTLM localement et le protocole Kerberos à distance (lorsque le protocole Kerberos fonctionne).</span><span class="sxs-lookup"><span data-stu-id="21b66-141">COM will choose NTLM locally and the Kerberos protocol remotely (when the Kerberos protocol will work).</span></span>

## <a name="related-topics"></a><span data-ttu-id="21b66-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="21b66-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21b66-143">Délégation et emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="21b66-143">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> </dl>

 

 