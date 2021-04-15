---
title: Handles entièrement et partiellement liés
description: Lorsque vous utilisez des points de terminaison dynamiques, les bibliothèques Runtime obtiennent les informations de point de terminaison telles qu’elles en ont besoin.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462247"
---
# <a name="fully-and-partially-bound-handles"></a><span data-ttu-id="b58cc-103">Handles entièrement et partiellement liés</span><span class="sxs-lookup"><span data-stu-id="b58cc-103">Fully and Partially Bound Handles</span></span>

<span data-ttu-id="b58cc-104">Lorsque vous utilisez des points de terminaison dynamiques, les bibliothèques Runtime obtiennent les informations de point de terminaison telles qu’elles en ont besoin.</span><span class="sxs-lookup"><span data-stu-id="b58cc-104">When you use dynamic endpoints, the run-time libraries obtain endpoint information as they need it.</span></span> <span data-ttu-id="b58cc-105">Les bibliothèques Runtime font la distinction entre un *handle entièrement lié* (un qui inclut des informations de point de terminaison) et un *handle partiellement lié* (un qui n’inclut pas d’informations de point de terminaison).</span><span class="sxs-lookup"><span data-stu-id="b58cc-105">The run-time libraries make the distinction between a *fully bound handle* (one that includes endpoint information) and a *partially bound handle* (one that does not include endpoint information).</span></span>

<span data-ttu-id="b58cc-106">La bibliothèque Runtime cliente doit convertir le handle partiellement lié en un handle entièrement lié avant que le client puisse effectuer une liaison au serveur.</span><span class="sxs-lookup"><span data-stu-id="b58cc-106">The client run-time library must convert the partially bound handle to a fully bound handle before the client can bind to the server.</span></span> <span data-ttu-id="b58cc-107">La bibliothèque Runtime cliente tente de convertir le handle partiellement lié pour l’application cliente en obtenant les informations de point de terminaison comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="b58cc-107">The client run-time library tries to convert the partially bound handle for the client application by obtaining the endpoint information as shown:</span></span>

-   <span data-ttu-id="b58cc-108">À partir de la spécification de l’interface du client</span><span class="sxs-lookup"><span data-stu-id="b58cc-108">From the client's interface specification</span></span>
-   <span data-ttu-id="b58cc-109">À partir d’un service de mappage de point de terminaison s’exécutant sur le serveur</span><span class="sxs-lookup"><span data-stu-id="b58cc-109">From an endpoint-mapping service running on the server</span></span>

<span data-ttu-id="b58cc-110">Si le client essaie d’utiliser un handle partiellement lié lorsque les informations de point de terminaison ne sont pas disponibles dans la spécification d’interface et que le mappeur de point de terminaison du serveur n’a pas d’informations sur le point de terminaison de serveur, le client ne disposera pas de suffisamment d’informations pour effectuer son appel de procédure distante et cet appel échouera.</span><span class="sxs-lookup"><span data-stu-id="b58cc-110">If the client tries to use a partially bound handle when the endpoint information is not available in the interface specification and the server's endpoint-mapper does not have information about the server endpoint, the client will not have enough information to make its remote procedure call and that call will fail.</span></span> <span data-ttu-id="b58cc-111">Pour éviter cela, vous devez inscrire le point de terminaison dans le mappeur de point de terminaison lorsque votre application distribuée utilise des handles partiellement liés.</span><span class="sxs-lookup"><span data-stu-id="b58cc-111">To prevent this, you must register the endpoint in the endpoint mapper when your distributed application uses partially bound handles.</span></span> <span data-ttu-id="b58cc-112">Pour plus d’informations sur le mappeur de point de terminaison, consultez [spécification de points de terminaison dynamiques](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="b58cc-112">For more information about the endpoint mapper, see [Specifying Dynamic Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="b58cc-113">En cas d’échec d’un appel de procédure distante, l’application cliente peut appeler [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) pour supprimer les informations de point de terminaison obsolètes.</span><span class="sxs-lookup"><span data-stu-id="b58cc-113">When a remote procedure call fails, the client application can call [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) to remove out-of-date endpoint information.</span></span> <span data-ttu-id="b58cc-114">Lorsque le client essaie d’appeler la procédure distante, la bibliothèque Runtime cliente tente à nouveau de convertir le handle entièrement lié en handle partiellement lié.</span><span class="sxs-lookup"><span data-stu-id="b58cc-114">When the client tries to call the remote procedure, the client run-time library again tries to convert the fully bound handle to a partially bound handle.</span></span> <span data-ttu-id="b58cc-115">Cela est utile lorsque le serveur a été arrêté et redémarré à l’aide d’un point de terminaison dynamique différent.</span><span class="sxs-lookup"><span data-stu-id="b58cc-115">This is useful when the server has been stopped and restarted using a different dynamic endpoint.</span></span>

 

 




