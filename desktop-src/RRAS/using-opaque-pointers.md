---
title: Utilisation de pointeurs opaques
description: Les clients doivent souvent stocker des informations supplémentaires spécifiques au client sur les destinations.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840417"
---
# <a name="using-opaque-pointers"></a><span data-ttu-id="e14f7-103">Utilisation de pointeurs opaques</span><span class="sxs-lookup"><span data-stu-id="e14f7-103">Using Opaque Pointers</span></span>

<span data-ttu-id="e14f7-104">Les clients doivent souvent stocker des informations supplémentaires spécifiques au client sur les destinations.</span><span class="sxs-lookup"><span data-stu-id="e14f7-104">Clients often must store additional, client-specific information about destinations.</span></span> <span data-ttu-id="e14f7-105">Le gestionnaire de tables de routage permet aux clients de stocker ces informations dans les structures de destination dans la table de routage.</span><span class="sxs-lookup"><span data-stu-id="e14f7-105">The routing table manager enables clients to store this information in destination structures in the routing table.</span></span> <span data-ttu-id="e14f7-106">Les informations sont stockées et récupérées à l’aide de *pointeurs opaques*.</span><span class="sxs-lookup"><span data-stu-id="e14f7-106">The information is stored and retrieved by using *opaque pointers*.</span></span> <span data-ttu-id="e14f7-107">Les informations stockées sont privées et accessibles uniquement au client propriétaire du pointeur opaque.</span><span class="sxs-lookup"><span data-stu-id="e14f7-107">The information stored is private, and accessible only to the client that owns the opaque pointer.</span></span>

<span data-ttu-id="e14f7-108">Par exemple, le gestionnaire de groupe de multidiffusion conserve une liste des entrées de transfert de multidiffusion qui dépendent d’une destination particulière.</span><span class="sxs-lookup"><span data-stu-id="e14f7-108">For example, the multicast group manager keeps a list of multicast forwarding entries that are dependent on a particular destination.</span></span> <span data-ttu-id="e14f7-109">Le gestionnaire de groupe de multidiffusion utilise un pointeur opaque dans cette destination.</span><span class="sxs-lookup"><span data-stu-id="e14f7-109">The multicast group manager uses an opaque pointer in that destination.</span></span> <span data-ttu-id="e14f7-110">Dans un autre exemple, un protocole de routage qui publie une destination particulière peut conserver les informations relatives à sa propre publication de route de la destination à l’aide d’un pointeur opaque, même s’il ne possède pas le meilleur itinéraire.</span><span class="sxs-lookup"><span data-stu-id="e14f7-110">In another example, a routing protocol that advertises a particular destination can keep information related to its own route advertisement of the destination using an opaque pointer, even though it does not own the best route.</span></span>

<span data-ttu-id="e14f7-111">Le nombre de pointeurs opaques est limité ; ces pointeurs sont alloués aux clients sur la base du premier arrivé, premier servi.</span><span class="sxs-lookup"><span data-stu-id="e14f7-111">The number of opaque pointers is limited; these pointers are allocated to clients on a first-come, first-served basis.</span></span> <span data-ttu-id="e14f7-112">L’administrateur de routeur doit allouer le nombre correct de pointeurs pendant la configuration du routeur. par conséquent, les protocoles de routage et les autres clients doivent documenter leur utilisation de pointeurs opaques.</span><span class="sxs-lookup"><span data-stu-id="e14f7-112">The router administrator must allocate the correct number of pointers during the router configuration; therefore, routing protocols and other clients must document their use of opaque pointers.</span></span>

 

 




