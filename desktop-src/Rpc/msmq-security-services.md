---
title: Services de sécurité MSMQ
description: Les messages RPC synchrones peuvent utiliser toutes les fonctionnalités de sécurité disponibles à partir de la durée d’exécution RPC. Pour plus d’informations, consultez sécurité.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101985"
---
# <a name="msmq-security-services"></a><span data-ttu-id="b2343-104">Services de sécurité MSMQ</span><span class="sxs-lookup"><span data-stu-id="b2343-104">MSMQ Security Services</span></span>

<span data-ttu-id="b2343-105">Les messages RPC synchrones peuvent utiliser toutes les fonctionnalités de sécurité disponibles à partir de la durée d’exécution RPC.</span><span class="sxs-lookup"><span data-stu-id="b2343-105">Synchronous RPC messages can use any of the security features available from the RPC run time.</span></span> <span data-ttu-id="b2343-106">Pour plus d’informations, consultez [sécurité](security.md) .</span><span class="sxs-lookup"><span data-stu-id="b2343-106">See [Security](security.md) for more details.</span></span>

<span data-ttu-id="b2343-107">Les appels asynchrones de \[ [messages](/windows/desktop/Midl/message) \] ne peuvent pas utiliser la sécurité RPC, car il n’existe aucune négociation entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b2343-107">Asynchronous \[ [message](/windows/desktop/Midl/message)\] calls cannot use RPC security because there is no handshake between client and server.</span></span> <span data-ttu-id="b2343-108">En fait, le serveur peut ne pas s’exécuter même au moment de l’appel.</span><span class="sxs-lookup"><span data-stu-id="b2343-108">In fact, the server may not even be running at the time of the call.</span></span> <span data-ttu-id="b2343-109">Pour accéder aux services de sécurité fournis par Message Queuinging services (MSMQ), l’application cliente doit appeler [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) pour contrôler le niveau d’authentification et de confidentialité pour ses appels au serveur.</span><span class="sxs-lookup"><span data-stu-id="b2343-109">To access the security services provided by Message Queuing Services (MSMQ), the client application should call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) to control the level of authentication and privacy for its calls to the server.</span></span>

<span data-ttu-id="b2343-110">L’application serveur peut appeler [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) à partir d’un appel de procédure distante pour déterminer le niveau de sécurité de cet appel.</span><span class="sxs-lookup"><span data-stu-id="b2343-110">The server application can call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) from within a remote procedure call to determine the security level for that call.</span></span> <span data-ttu-id="b2343-111">Le tableau suivant montre le mappage entre les constantes de sécurité RPC et la sécurité MSMQ.</span><span class="sxs-lookup"><span data-stu-id="b2343-111">The mapping between RPC security constants and MSMQ security is shown in the following table.</span></span>



| <span data-ttu-id="b2343-112">Niveau de sécurité RPC</span><span class="sxs-lookup"><span data-stu-id="b2343-112">RPC security level</span></span>                | <span data-ttu-id="b2343-113">Description</span><span class="sxs-lookup"><span data-stu-id="b2343-113">Description</span></span>                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2343-114">\_niveau d’authentification \_ RPC \_ aucun</span><span class="sxs-lookup"><span data-stu-id="b2343-114">RPC\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="b2343-115">L’appel n’est pas authentifié ou chiffré.</span><span class="sxs-lookup"><span data-stu-id="b2343-115">The call is not authenticated or encrypted.</span></span>                                                |
| <span data-ttu-id="b2343-116">\_ \_ intégrité PKT au niveau \_ de \_ l’authentification RPC</span><span class="sxs-lookup"><span data-stu-id="b2343-116">RPC\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="b2343-117">L’appel est authentifié à l’aide de la sécurité MSMQ.</span><span class="sxs-lookup"><span data-stu-id="b2343-117">The call is authenticated using MSMQ security.</span></span>                                             |
| <span data-ttu-id="b2343-118">confidentialité du niveau d' \_ authentification RPC \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2343-118">RPC\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="b2343-119">L’appel est authentifié et chiffré au fur et à mesure qu’il transite entre la file d’attente du client et du serveur.</span><span class="sxs-lookup"><span data-stu-id="b2343-119">The call is authenticated and encrypted as it travels between the client and server queue.</span></span> |



 

<span data-ttu-id="b2343-120">Le serveur peut également forcer l’authentification et le chiffrement de l’appel en appelant [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) et en définissant le niveau d’authentification RPC c MQ Authn, le niveau d’authentification et l’intégrité PKT du niveau d’authentification RPC c MQ \_ \_ \_ \_ \_ , \_ \_ \_ \_ \_ \_ ainsi que les \_ \_ \_ \_ indicateurs de confidentialité de niveau d’authentification RPC c MQ Authn \_ \_ dans la structure de la [**\_ stratégie RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) .</span><span class="sxs-lookup"><span data-stu-id="b2343-120">The server can also force call authentication and encryption by calling [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) and setting the RPC\_C\_MQ\_AUTHN\_LEVEL\_NONE, RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_INTEGRITY and RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_PRIVACY flags in the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure.</span></span>

 

 