---
title: Serveurs DNS
description: Un serveur DNS est un ordinateur qui termine le processus de résolution de noms dans DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Serveurs DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674361"
---
# <a name="dns-servers"></a><span data-ttu-id="dbaed-104">Serveurs DNS</span><span class="sxs-lookup"><span data-stu-id="dbaed-104">DNS Servers</span></span>

<span data-ttu-id="dbaed-105">Un *serveur DNS* est un ordinateur qui termine le processus de résolution de noms dans DNS.</span><span class="sxs-lookup"><span data-stu-id="dbaed-105">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="dbaed-106">Les serveurs DNS contiennent des [*fichiers de zone*](z-gly.md) qui leur permettent de résoudre les noms en adresses IP et adresses IP en noms.</span><span class="sxs-lookup"><span data-stu-id="dbaed-106">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="dbaed-107">Lorsqu’il est interrogé, un serveur DNS répond de l’une des trois façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbaed-107">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="dbaed-108">Le serveur retourne les données de résolution de noms ou de résolution IP demandées.</span><span class="sxs-lookup"><span data-stu-id="dbaed-108">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="dbaed-109">Le serveur retourne un pointeur vers un autre serveur DNS qui peut traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="dbaed-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="dbaed-110">Le serveur indique qu’il n’a pas les données demandées.</span><span class="sxs-lookup"><span data-stu-id="dbaed-110">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="dbaed-111">Les serveurs DNS peuvent, au cours de la préparation, renvoyer les données de résolution demandées, interroger d’autres serveurs DNS, mais au-delà, les serveurs DNS n’effectuent aucune autre opération.</span><span class="sxs-lookup"><span data-stu-id="dbaed-111">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="dbaed-112">Il existe trois types principaux de serveurs DNS : les serveurs principaux, les serveurs secondaires et les serveurs de mise en cache.</span><span class="sxs-lookup"><span data-stu-id="dbaed-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="dbaed-113">Serveur principal</span><span class="sxs-lookup"><span data-stu-id="dbaed-113">Primary Server</span></span>

<span data-ttu-id="dbaed-114">Le *serveur principal* est le serveur faisant autorité pour la zone.</span><span class="sxs-lookup"><span data-stu-id="dbaed-114">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="dbaed-115">Toutes les tâches d’administration associées à la zone (telles que la création de sous-domaines dans la zone, ou d’autres tâches d’administration similaires) doivent être effectuées sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="dbaed-115">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="dbaed-116">En outre, toute modification associée à la zone, ou toute modification ou ajout à des RR dans les fichiers de zone, doit être effectuée sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="dbaed-116">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="dbaed-117">Pour une zone donnée, il y a un serveur principal, sauf lorsque vous intégrez Active Directory Services et le serveur DNS Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dbaed-117">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="dbaed-118">Serveurs secondaires</span><span class="sxs-lookup"><span data-stu-id="dbaed-118">Secondary Servers</span></span>

<span data-ttu-id="dbaed-119">Les *serveurs secondaires* sont des serveurs DNS de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="dbaed-119">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="dbaed-120">Les serveurs secondaires reçoivent tous leurs fichiers de zone des fichiers de zone du serveur principal dans un transfert de zone.</span><span class="sxs-lookup"><span data-stu-id="dbaed-120">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="dbaed-121">Plusieurs serveurs secondaires peuvent exister pour une zone donnée, autant que nécessaire pour assurer l' [*équilibrage*](l-gly.md)de la charge, la [*tolérance aux pannes*](f-gly.md)et la réduction du trafic.</span><span class="sxs-lookup"><span data-stu-id="dbaed-121">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="dbaed-122">En outre, tout serveur DNS donné peut être un serveur secondaire pour plusieurs zones.</span><span class="sxs-lookup"><span data-stu-id="dbaed-122">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="dbaed-123">Outre les serveurs DNS principal et secondaire, des rôles de serveur DNS supplémentaires peuvent être utilisés lorsque ces serveurs sont appropriés pour une infrastructure DNS.</span><span class="sxs-lookup"><span data-stu-id="dbaed-123">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="dbaed-124">Ces serveurs supplémentaires mettent en cache les serveurs et les [*redirecteurs*](f-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dbaed-124">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="dbaed-125">Serveurs de mise en cache</span><span class="sxs-lookup"><span data-stu-id="dbaed-125">Caching Servers</span></span>

<span data-ttu-id="dbaed-126">Les [*serveurs de mise en cache*](c-gly.md), également appelés serveurs avec mise en cache uniquement, s’exécutent comme leur nom. ils fournissent uniquement un service de requête mis en cache pour les réponses DNS.</span><span class="sxs-lookup"><span data-stu-id="dbaed-126">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="dbaed-127">Plutôt que de gérer des fichiers de zone comme d’autres serveurs secondaires, la mise en cache des serveurs DNS effectue des requêtes, met en cache les réponses et retourne les résultats au client d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="dbaed-127">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="dbaed-128">La principale différence entre la mise en cache de serveurs et d’autres serveurs secondaires réside dans le fait que les autres serveurs secondaires gèrent les fichiers de zone (et effectuent les transferts de zone le cas échéant, générant ainsi le trafic réseau associé au transfert), pas les serveurs de mise en cache.</span><span class="sxs-lookup"><span data-stu-id="dbaed-128">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




