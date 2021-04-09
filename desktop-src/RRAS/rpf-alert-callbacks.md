---
title: Rappels d’alerte RPF
description: Une fois que le gestionnaire de groupe de multidiffusion a reçu la notification d’un paquet provenant d’une nouvelle source ou d’un paquet destiné à un nouveau groupe, le gestionnaire de groupe de multidiffusion recherche l’itinéraire vers la source dans la vue multidiffusion de la table de routage.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675977"
---
# <a name="rpf-alert-callbacks"></a><span data-ttu-id="2268a-103">Rappels d’alerte RPF</span><span class="sxs-lookup"><span data-stu-id="2268a-103">RPF Alert Callbacks</span></span>

<span data-ttu-id="2268a-104">Une fois que le gestionnaire de groupe de multidiffusion a reçu la notification d’un paquet provenant d’une nouvelle source ou d’un paquet destiné à un nouveau groupe, le gestionnaire de groupe de multidiffusion recherche l’itinéraire vers la source dans la vue multidiffusion de la table de routage.</span><span class="sxs-lookup"><span data-stu-id="2268a-104">After the multicast group manager receives notification of a packet from a new source or of a packet that is destined for a new group, the multicast group manager looks up the route to the source in the multicast view of the routing table.</span></span> <span data-ttu-id="2268a-105">Le gestionnaire de groupe de multidiffusion appelle ensuite le rappel de [**\_ \_ rappel PMGM RPF**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) au protocole propriétaire de l’interface sur laquelle les données sont arrivées.</span><span class="sxs-lookup"><span data-stu-id="2268a-105">The multicast group manager then invokes the [**PMGM\_RPF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) callback to the protocol that owns the interface the data arrived on.</span></span>

<span data-ttu-id="2268a-106">Une fois ce rappel appelé, le protocole de routage peut modifier l’interface entrante si le protocole de routage doit recevoir les données du groupe sur une autre interface.</span><span class="sxs-lookup"><span data-stu-id="2268a-106">After this callback is invoked, the routing protocol can change the incoming interface if the routing protocol must receive the data for the group on a different interface.</span></span>

 

 




