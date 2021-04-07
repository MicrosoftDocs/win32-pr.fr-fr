---
title: Publication de service
description: Les services se publient eux-mêmes à l’aide d’objets stockés dans Active Directory Domain Services.
ms.assetid: 69e9256f-40ee-4aed-8213-1bbda0e508af
ms.tgt_platform: multiple
keywords:
- Publication de service Active Directory
- Active Directory, utilisation, publication de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437d9f4aa5184c53f2962d7b2640e933107501f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028588"
---
# <a name="service-publication"></a><span data-ttu-id="db320-105">Publication de service</span><span class="sxs-lookup"><span data-stu-id="db320-105">Service Publication</span></span>

<span data-ttu-id="db320-106">Les services se publient eux-mêmes à l’aide d’objets stockés dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="db320-106">Services advertise themselves using objects stored in Active Directory Domain Services.</span></span> <span data-ttu-id="db320-107">C’est ce que l’on appelle la *publication de service*.</span><span class="sxs-lookup"><span data-stu-id="db320-107">This is known as *service publication*.</span></span> <span data-ttu-id="db320-108">Les clients interrogent le répertoire pour localiser les services.</span><span class="sxs-lookup"><span data-stu-id="db320-108">Clients query the directory to locate services.</span></span> <span data-ttu-id="db320-109">C’est ce que l’on appelle le *Rendezvous client-service*.</span><span class="sxs-lookup"><span data-stu-id="db320-109">This is called *client-service rendezvous*.</span></span> <span data-ttu-id="db320-110">Cette section décrit les types d’objets d’annuaire utilisés pour la publication de service et explique comment ils sont utilisés pour le rendezvous client-service.</span><span class="sxs-lookup"><span data-stu-id="db320-110">This section discusses the types of directory objects used for service publication and explains how they are used for client-service rendezvous.</span></span>

<span data-ttu-id="db320-111">Cette section aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="db320-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="db320-112">Vue d’ensemble de la publication de service</span><span class="sxs-lookup"><span data-stu-id="db320-112">An overview of service publication</span></span>](about-service-publication.md)
-   [<span data-ttu-id="db320-113">Problèmes de sécurité pour la publication de service</span><span class="sxs-lookup"><span data-stu-id="db320-113">Security issues for service publication</span></span>](security-issues-for-service-publication.md)
-   [<span data-ttu-id="db320-114">Objets point de connexion</span><span class="sxs-lookup"><span data-stu-id="db320-114">Connection point objects</span></span>](connection-points.md)
-   [<span data-ttu-id="db320-115">Publication avec des points de connexion de service (SCP)</span><span class="sxs-lookup"><span data-stu-id="db320-115">Publishing with service connection points (SCPs)</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="db320-116">Informations à stocker dans un point de connexion de service</span><span class="sxs-lookup"><span data-stu-id="db320-116">What information to store in a service connection point</span></span>](service-connection-point-properties.md)
-   [<span data-ttu-id="db320-117">Où créer un point de connexion de service</span><span class="sxs-lookup"><span data-stu-id="db320-117">Where to create a service connection point</span></span>](where-to-create-a-service-connection-point.md)
-   [<span data-ttu-id="db320-118">Publication de services de base de données, basés sur l’hôte et réplicables à l’aide de points de connexion de service</span><span class="sxs-lookup"><span data-stu-id="db320-118">How to publish replicable, host-based, and database services using service connection points</span></span>](service-connection-points-for-replicated-host-based-and-database-services.md)
-   [<span data-ttu-id="db320-119">Création et gestion d’un point de connexion de service</span><span class="sxs-lookup"><span data-stu-id="db320-119">Creating and maintaining a service connection point</span></span>](creating-and-maintaining-a-service-connection-point.md)
-   [<span data-ttu-id="db320-120">Comment un client interroge un SCP et l’utilise pour établir une liaison avec une instance de service</span><span class="sxs-lookup"><span data-stu-id="db320-120">How a client queries for an SCP and uses it to bind to a service instance</span></span>](how-clients-find-and-use-a-service-connection-point.md)
-   [<span data-ttu-id="db320-121">Utilisation des API RpcNs (RPC Name Service) pour publier un service RPC</span><span class="sxs-lookup"><span data-stu-id="db320-121">Using the RPC name service (RpcNs) APIs to publish an RPC service</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="db320-122">Inscription et résolution Windows Sockets (RnR) pour publier un service Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="db320-122">Windows Sockets registration and resolution (RnR) to publish a Windows Sockets service</span></span>](publishing-with-windows-sockets-registration-and-resolution.md)
-   [<span data-ttu-id="db320-123">Publication de services COM dans le magasin de classes COM+</span><span class="sxs-lookup"><span data-stu-id="db320-123">Publication of COM-based services in the COM+ class store</span></span>](publishing-com-services.md)

<span data-ttu-id="db320-124">Pour plus d’informations sur la façon dont les services et les clients s’authentifient mutuellement, consultez [authentification mutuelle à l’aide de Kerberos](mutual-authentication-using-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="db320-124">For more information about how services and clients authenticate each other, see [Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md).</span></span> <span data-ttu-id="db320-125">Pour plus d’informations sur les contextes de sécurité de service et les comptes d’ouverture de session, consultez [comptes d’ouverture de session de service](service-logon-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="db320-125">For more information about service security contexts and logon accounts, see [Service Logon Accounts](service-logon-accounts.md).</span></span>

 

 




