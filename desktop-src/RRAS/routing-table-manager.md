---
title: Gestionnaire de table de routage
description: Le gestionnaire de tables de routage est le référentiel central des informations de routage pour tous les protocoles de routage qui fonctionnent sous le service de routage et d’accès à distance (RRAS).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511812"
---
# <a name="routing-table-manager"></a><span data-ttu-id="b3532-103">Gestionnaire de table de routage</span><span class="sxs-lookup"><span data-stu-id="b3532-103">Routing Table Manager</span></span>

<span data-ttu-id="b3532-104">Le gestionnaire de tables de routage est le référentiel central des informations de routage pour tous les protocoles de routage qui fonctionnent sous le service de routage et d’accès à distance (RRAS).</span><span class="sxs-lookup"><span data-stu-id="b3532-104">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="b3532-105">Elle avertit les clients lorsque des modifications ont eu lieu et permet aux clients d’échanger des informations privées.</span><span class="sxs-lookup"><span data-stu-id="b3532-105">It notifies clients when changes have occurred, and allows clients to exchange private information.</span></span>

<span data-ttu-id="b3532-106">Le gestionnaire de tables de routage fournit des informations de routage à tous les clients concernés, tels que les protocoles de routage, les programmes de gestion et les programmes de surveillance.</span><span class="sxs-lookup"><span data-stu-id="b3532-106">The routing table manager provides routing information to all interested clients, such as routing protocols, management programs, and monitoring programs.</span></span> <span data-ttu-id="b3532-107">Le gestionnaire de tables de routage détermine également le meilleur itinéraire vers chaque réseau de destination connu des protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="b3532-107">The routing table manager also determines the best route to each destination network that is known to the routing protocols.</span></span> <span data-ttu-id="b3532-108">Le gestionnaire de tables de routage détermine cet itinéraire en fonction des priorités de protocole de routage et des métriques associées aux itinéraires.</span><span class="sxs-lookup"><span data-stu-id="b3532-108">The routing table manager determines this route based on routing protocol priorities and on the metrics associated with the routes.</span></span> <span data-ttu-id="b3532-109">La personne qui administre le routeur peut configurer des priorités de protocole de routage à l’aide de la console de gestion RRAS.</span><span class="sxs-lookup"><span data-stu-id="b3532-109">The person administering the router can configure routing protocol priorities using the RRAS management console.</span></span>

<span data-ttu-id="b3532-110">Le gestionnaire de tables de routage transmet les informations les plus bonnes aux redirecteurs (une par famille d’adresses, ou une par interface) et à tous les clients intéressés.</span><span class="sxs-lookup"><span data-stu-id="b3532-110">The routing table manager passes the best-route information to the forwarders (one per address family, or one per interface) and to all interested clients.</span></span>

<span data-ttu-id="b3532-111">Chaque client s’inscrit auprès du gestionnaire de tables de routage et, en retour, il reçoit un descripteur utilisé par le client pour ajouter ou supprimer des itinéraires.</span><span class="sxs-lookup"><span data-stu-id="b3532-111">Each client registers with the routing table manager, and in return receives a handle that the client uses to add or delete routes.</span></span> <span data-ttu-id="b3532-112">Les clients peuvent récupérer les informations stockées dans la table de routage.</span><span class="sxs-lookup"><span data-stu-id="b3532-112">Clients can retrieve information stored in the routing table.</span></span> <span data-ttu-id="b3532-113">En outre, les clients peuvent s’inscrire auprès du gestionnaire de tables de routage pour recevoir la notification des modifications apportées au meilleur itinéraire vers une destination.</span><span class="sxs-lookup"><span data-stu-id="b3532-113">Additionally, clients can register with the routing table manager to receive notification of changes to the best route to a destination.</span></span>

 

 




