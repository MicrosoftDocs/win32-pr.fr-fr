---
title: Déploiement de l’équilibrage de charge
description: Déploiement de l’équilibrage de charge
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196565"
---
# <a name="deploying-load-balancing"></a><span data-ttu-id="c24ae-103">Déploiement de l’équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="c24ae-103">Deploying Load Balancing</span></span>

<span data-ttu-id="c24ae-104">L’environnement de déploiement classique et le cas d’usage sont utilisés par l’équilibrage de charge RPC, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="c24ae-104">The typical deployment environment and use case is which the RPC Load balancer is utilized is shown below:</span></span>![équilibrage de charge RPC](images/rpc-load-balancing.png)

1.  <span data-ttu-id="c24ae-106">Le client RPC établit une connexion RPC/HTTP à la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="c24ae-106">The RPC client makes an RPC/HTTP connection to the server farm.</span></span>
2.  <span data-ttu-id="c24ae-107">La connexion est transférée via le réseau vers un équilibreur de charge frontale</span><span class="sxs-lookup"><span data-stu-id="c24ae-107">The connection is forwarded through the network to a front end load balancer</span></span>
3.  <span data-ttu-id="c24ae-108">L’équilibreur de charge frontal choisit un serveur pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="c24ae-108">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="c24ae-109">Dans cet exemple, l’équilibreur de charge frontale transmet la connexion au serveur 1.</span><span class="sxs-lookup"><span data-stu-id="c24ae-109">In this example, the front end load balancer forwards the connection to Server 1.</span></span>
4.  <span data-ttu-id="c24ae-110">Le service d’équilibrage de charge RPC arbitre la connexion.</span><span class="sxs-lookup"><span data-stu-id="c24ae-110">The RPC Load balancer service arbitrates the connection.</span></span> <span data-ttu-id="c24ae-111">Il détermine qu’il s’agit de la première connexion du client et associe la connexion au serveur local, le serveur 1.</span><span class="sxs-lookup"><span data-stu-id="c24ae-111">It determines that this is the first connection from the client and associates the connection with the local server, Server 1.</span></span>
5.  <span data-ttu-id="c24ae-112">Le client effectue une deuxième requête RPC/HTTP.</span><span class="sxs-lookup"><span data-stu-id="c24ae-112">The client makes a second RPC/HTTP request.</span></span>
6.  <span data-ttu-id="c24ae-113">La demande est transférée via le réseau à l’équilibreur de charge frontal.</span><span class="sxs-lookup"><span data-stu-id="c24ae-113">The request is forwarded through the network to the front end load balancer.</span></span>
7.  <span data-ttu-id="c24ae-114">L’équilibreur de charge frontal choisit un serveur pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="c24ae-114">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="c24ae-115">Dans ce cas, l’équilibreur de charge frontal choisit le serveur 2 pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="c24ae-115">In this case, the front end load balancer chooses Server 2 to service the request.</span></span>
8.  <span data-ttu-id="c24ae-116">Le service de Load Balancer RPC arbitre la connexion.</span><span class="sxs-lookup"><span data-stu-id="c24ae-116">The RPC Load Balancer service arbitrates the connection.</span></span> <span data-ttu-id="c24ae-117">Il reconnaît que les connexions à partir de ce client sont servies par le serveur 1.</span><span class="sxs-lookup"><span data-stu-id="c24ae-117">It recognizes that connections from this client is being serviced by Server 1.</span></span>
9.  <span data-ttu-id="c24ae-118">La connexion est transférée vers le serveur 1.</span><span class="sxs-lookup"><span data-stu-id="c24ae-118">The connection is forwarded to Server 1.</span></span>

 

 




