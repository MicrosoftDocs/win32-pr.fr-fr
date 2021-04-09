---
title: Tronçons suivants
description: Les itinéraires sont associés à un ou plusieurs tronçons suivants.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028689"
---
# <a name="next-hops"></a><span data-ttu-id="46b09-103">Tronçons suivants</span><span class="sxs-lookup"><span data-stu-id="46b09-103">Next Hops</span></span>

<span data-ttu-id="46b09-104">Les itinéraires sont associés à un ou plusieurs tronçons suivants.</span><span class="sxs-lookup"><span data-stu-id="46b09-104">Routes have one or more next hops associated with them.</span></span> <span data-ttu-id="46b09-105">Si la destination n’est pas sur un réseau directement connecté, le tronçon suivant est l’adresse du routeur suivant (ou réseau) sur le réseau sortant qui peut mieux acheminer les données vers la destination.</span><span class="sxs-lookup"><span data-stu-id="46b09-105">If the destination is not on a directly connected network, the next hop is the address of the next router (or network) on the outgoing network that can best route data to the destination.</span></span> <span data-ttu-id="46b09-106">Le meilleur itinéraire est l’itinéraire qui a le coût le plus faible, en fonction de la stratégie de routage en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="46b09-106">The best route is the route that has the least cost, based on the routing policy in use.</span></span> <span data-ttu-id="46b09-107">Chaque tronçon suivant peut être utilisé pour transférer des données sur le chemin d’accès à la destination.</span><span class="sxs-lookup"><span data-stu-id="46b09-107">Each next hop can be used to forward data on the path to the destination.</span></span> <span data-ttu-id="46b09-108">Tous les itinéraires détenus par un client partagent un ensemble commun d’entrées de saut suivant qui ont été ajoutées par le client.</span><span class="sxs-lookup"><span data-stu-id="46b09-108">All routes owned by a client share a common set of next-hop entries that were added by the client.</span></span>

<span data-ttu-id="46b09-109">Chaque tronçon suivant est identifié de manière unique par l’adresse du tronçon suivant et l’index d’interface utilisé pour atteindre le tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="46b09-109">Each next hop is uniquely identified by the address of the next hop and the interface index used to reach the next hop.</span></span>

<span data-ttu-id="46b09-110">Si le tronçon suivant lui-même n’est pas directement connecté, il est marqué comme tronçon suivant « distant ».</span><span class="sxs-lookup"><span data-stu-id="46b09-110">If the next hop itself is not directly connected, it is marked as a "remote" next hop.</span></span> <span data-ttu-id="46b09-111">Dans ce cas, le redirecteur doit effectuer une autre recherche à l’aide de l’adresse réseau du tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="46b09-111">In this case, the forwarder must perform another lookup using the next hop's network address.</span></span> <span data-ttu-id="46b09-112">Cette recherche est nécessaire pour trouver le tronçon suivant « local » utilisé pour atteindre le tronçon suivant distant et la destination.</span><span class="sxs-lookup"><span data-stu-id="46b09-112">This lookup is necessary to find the "local" next hop used to reach the remote next hop and the destination.</span></span>

<span data-ttu-id="46b09-113">Une entrée de saut suivant dans la table de routage comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="46b09-113">A next-hop entry in the routing table includes:</span></span>

-   <span data-ttu-id="46b09-114">Adresse réseau du tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="46b09-114">The network address of the next hop</span></span>
-   <span data-ttu-id="46b09-115">Propriétaire du tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="46b09-115">The owner of the next hop</span></span>
-   <span data-ttu-id="46b09-116">Identificateur de l’interface sortante</span><span class="sxs-lookup"><span data-stu-id="46b09-116">The identifier of the outgoing interface</span></span>
-   <span data-ttu-id="46b09-117">État du tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="46b09-117">The state of the next hop</span></span>
-   <span data-ttu-id="46b09-118">Indicateurs associés au tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="46b09-118">Flags associated with the next hop</span></span>
-   <span data-ttu-id="46b09-119">Informations privées pour le propriétaire du tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="46b09-119">Information that is private to the owner of the next hop</span></span>
-   <span data-ttu-id="46b09-120">Handle vers la destination correspondant au tronçon suivant distant</span><span class="sxs-lookup"><span data-stu-id="46b09-120">A handle to the destination corresponding to the remote next hop</span></span>

 

 




