---
title: Équilibrage de charge RPC
description: Équilibrage de charge RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028653"
---
# <a name="rpc-load-balancing"></a><span data-ttu-id="eaa67-103">Équilibrage de charge RPC</span><span class="sxs-lookup"><span data-stu-id="eaa67-103">RPC Load Balancing</span></span>

<span data-ttu-id="eaa67-104">L’équilibrage de charge Microsoft RPC est destiné à fournir une solution évolutive pour les scénarios qui exigent une charge élevée de [RPC sur](remote-procedure-calls-using-rpc-over-http.md) le trafic http.</span><span class="sxs-lookup"><span data-stu-id="eaa67-104">Microsoft RPC Load Balancing is intended to provide a scalable solution for scenarios which demand a high load of [RPC over HTTP](remote-procedure-calls-using-rpc-over-http.md) traffic.</span></span> <span data-ttu-id="eaa67-105">L’objectif principal du Load Balancer RPC est de garantir que le trafic RPC/HTTP peut être assuré par une batterie de serveurs pour améliorer l’évolutivité.</span><span class="sxs-lookup"><span data-stu-id="eaa67-105">The RPC Load Balancer’s primary purpose is to ensure RPC/HTTP traffic can be serviced by a server farm to improve scalability.</span></span> <span data-ttu-id="eaa67-106">Pour ce faire, RPC doit s’assurer que toutes les connexions à partir d’un processus client sont traitées par le même point de terminaison de serveur dans la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="eaa67-106">To achieve this, RPC must ensure that all connections from a client process are serviced by the same server endpoint in the server farm.</span></span> <span data-ttu-id="eaa67-107">La Load Balancer RPC est implémentée en tant que service qui s’exécute conjointement avec le service proxy RPC sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="eaa67-107">The RPC Load Balancer is implemented as a service which runs in conjunction with the RPC over HTTP Proxy service.</span></span>

<span data-ttu-id="eaa67-108">Pour activer l’équilibrage de charge, le service d’équilibrage de charge RPC s’exécutant sur chacun des serveurs communique les uns avec les autres pour déterminer le serveur préféré pour la connexion cliente initiale.</span><span class="sxs-lookup"><span data-stu-id="eaa67-108">To enable load balancing, the RPC Load Balancing service running on each of the servers communicates with each other to determine the preferred server for the initial client connection.</span></span> <span data-ttu-id="eaa67-109">Ce processus est appelé arbitrage et se produit au moment de la connexion initiale du client.</span><span class="sxs-lookup"><span data-stu-id="eaa67-109">This process is called arbitration and it occurs at the time of the initial client connection.</span></span> <span data-ttu-id="eaa67-110">Pour réduire le trafic entre serveurs, le service d’équilibrage de charge RPC choisit le point de terminaison local pour traiter la connexion si le client n’est pas déjà associé à un serveur.</span><span class="sxs-lookup"><span data-stu-id="eaa67-110">To reduce cross server traffic, the RPC Load Balancing service chooses the local endpoint to service the connection if the client is not already associated with a server.</span></span> <span data-ttu-id="eaa67-111">Pour une connexion client donnée, le résultat de l’arbitrage est l’une des deux possibilités suivantes :</span><span class="sxs-lookup"><span data-stu-id="eaa67-111">For a given client connection, the outcome of arbitration is one of two possibilities:</span></span>

-   <span data-ttu-id="eaa67-112">Si le client a déjà établi une connexion, le serveur qui reçoit d’abord la connexion traitera les connexions suivantes.</span><span class="sxs-lookup"><span data-stu-id="eaa67-112">If the client has already made a connection, the server to first receive the connection will handle the subsequent connections.</span></span>
-   <span data-ttu-id="eaa67-113">S’il s’agit de la première connexion du client, l’arbitrage se traduira par le serveur local qui gère la connexion et, par conséquent, par toutes les connexions du client.</span><span class="sxs-lookup"><span data-stu-id="eaa67-113">If this is the first connection from the client, arbitration will result in the local server handling the connection, and thus all connections from the client.</span></span> <span data-ttu-id="eaa67-114">Cette information, une fois déterminée, est validée dans les autres services de Load Balancer RPC de la batterie de serveurs, en les informant du serveur qui gère toutes les demandes du client.</span><span class="sxs-lookup"><span data-stu-id="eaa67-114">This information, once determined, will be committed to the other RPC Load Balancer services in the server farm, thus informing them of the server handling all of the client’s requests.</span></span>

<span data-ttu-id="eaa67-115">Cette section fournit une vue d’ensemble de l’équilibrage de charge RPC dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="eaa67-115">This section provides an overview of RPC Load Balancing in the following topics:</span></span>

-   [<span data-ttu-id="eaa67-116">Déploiement de l’équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="eaa67-116">Deploying Load Balancing</span></span>](deploying-load-balancing.md)
-   [<span data-ttu-id="eaa67-117">Configuration de l’équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="eaa67-117">Configuring Load Balancing</span></span>](configuring-load-balancing.md)
-   [<span data-ttu-id="eaa67-118">Meilleures pratiques relatives à l’équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="eaa67-118">Load Balancing Best Practices</span></span>](load-balancing-best-practices.md)

## <a name="requirements"></a><span data-ttu-id="eaa67-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaa67-119">Requirements</span></span>

<span data-ttu-id="eaa67-120">Le service équilibrage de charge RPC est pris en charge sur les serveurs exécutant Windows Server 2008 R2 ou version ultérieure et sur les clients qui exécutent Windows 7 ou versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="eaa67-120">The RPC Load Balancing service is supported on servers running Windows Server 2008 R2 or later and clients running Windows 7 or later versions of Windows.</span></span>

<span data-ttu-id="eaa67-121">Le service de proxy RPC, le service d’équilibrage de charge RPC et les points de terminaison de serveur doivent tous être en cours d’exécution sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="eaa67-121">The RPC Proxy service, the RPC Load Balancing service and the server endpoints must all be running on the same machine.</span></span> <span data-ttu-id="eaa67-122">En outre, tous les serveurs de la batterie de serveurs doivent pouvoir traiter le point de terminaison demandé.</span><span class="sxs-lookup"><span data-stu-id="eaa67-122">Additionally, all servers in the server farm must be capable of servicing the requested endpoint.</span></span> <span data-ttu-id="eaa67-123">Pour plus d’informations sur la configuration du service de proxy RPC et du service d’équilibrage de charge RPC, consultez [Configuration des ordinateurs pour RPC sur http](configuring-computers-for-rpc-over-http.md) et configuration de l' [équilibrage de charge](configuring-load-balancing.md), respectivement.</span><span class="sxs-lookup"><span data-stu-id="eaa67-123">For information on configuring the RPC Proxy service and the RPC Load Balancing service, see [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) and [Configuring Load Balancing](configuring-load-balancing.md), respectively.</span></span>

## <a name="limitations"></a><span data-ttu-id="eaa67-124">Limites</span><span class="sxs-lookup"><span data-stu-id="eaa67-124">Limitations</span></span>

<span data-ttu-id="eaa67-125">À ce stade, l’équilibrage de charge RPC ne prend en charge qu’une seule batterie de serveurs par ressource.</span><span class="sxs-lookup"><span data-stu-id="eaa67-125">At this time, RPC Load Balancing supports only one server farm per resource.</span></span> <span data-ttu-id="eaa67-126">Tous les serveurs de toutes les batteries de serveurs doivent également être en mesure de traiter toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="eaa67-126">All servers in all server farms must be capable of servicing all resources as well.</span></span>

 

 




