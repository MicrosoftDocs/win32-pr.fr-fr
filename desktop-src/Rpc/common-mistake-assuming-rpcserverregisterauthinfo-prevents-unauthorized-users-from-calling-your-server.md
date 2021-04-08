---
title: Erreur courante en supposant que RpcServerRegisterAuthInfo empêche les utilisateurs non autorisés d’appeler votre serveur
description: Lorsque des fournisseurs de sécurité sont inscrits sur le serveur avec la fonction RpcServerRegisterAuthInfo, une option est ajoutée, et non une exigence.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675093"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a><span data-ttu-id="2fd24-103">Erreur courante : en supposant que RpcServerRegisterAuthInfo empêche les utilisateurs non autorisés d’appeler votre serveur</span><span class="sxs-lookup"><span data-stu-id="2fd24-103">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>

<span data-ttu-id="2fd24-104">Lorsque des fournisseurs de sécurité sont inscrits sur le serveur avec la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) , une option est ajoutée, et non une exigence.</span><span class="sxs-lookup"><span data-stu-id="2fd24-104">When security providers are registered on the server with the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function, an option is added, not a requirement.</span></span> <span data-ttu-id="2fd24-105">Cela signifie que les inscriptions précédentes avec **RpcServerRegisterAuthInfo** ne sont pas remplacées.</span><span class="sxs-lookup"><span data-stu-id="2fd24-105">This means previous registrations with **RpcServerRegisterAuthInfo** are not replaced.</span></span> <span data-ttu-id="2fd24-106">Cela signifie également que les clients non authentifiés peuvent toujours se connecter.</span><span class="sxs-lookup"><span data-stu-id="2fd24-106">This also means unauthenticated clients still can connect.</span></span> <span data-ttu-id="2fd24-107">En appelant la fonction **RpcServerRegisterAuthInfo** , les clients non authentifiés ne sont pas autorisés à se connecter ; ils peuvent toujours se connecter, mais les appels de fonction, tels que [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) et [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) , échouent.</span><span class="sxs-lookup"><span data-stu-id="2fd24-107">By calling the **RpcServerRegisterAuthInfo** function, unauthenticated clients are not disallowed from connecting; they can still connect, but function calls such as [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) will fail.</span></span> <span data-ttu-id="2fd24-108">Ainsi, lorsque la fonction **RpcServerRegisterAuthInfo** est appelée, les attaquants potentiels n’ont pas été désinstallés. les clients qui devraient avoir accès ont la possibilité de prouver leur identité.</span><span class="sxs-lookup"><span data-stu-id="2fd24-108">So when the **RpcServerRegisterAuthInfo** function is called, potential attackers have not been weeded out—rather, clients that ought to have access are given a chance to prove their identity.</span></span> <span data-ttu-id="2fd24-109">Les vérifications doivent toujours être en place pour déterminer si des attaquants potentiels tentent de se connecter.</span><span class="sxs-lookup"><span data-stu-id="2fd24-109">Checks must still be in place to determine whether potential attackers are attempting to connect.</span></span>

 

 




