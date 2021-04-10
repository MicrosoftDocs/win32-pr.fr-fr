---
title: Itinéraires statiques et statiques
description: En règle générale, les itinéraires vers des réseaux distants sont obtenus de manière dynamique via des protocoles de routage.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940245"
---
# <a name="static-and-autostatic-routes"></a><span data-ttu-id="ff75d-103">Itinéraires statiques et statiques</span><span class="sxs-lookup"><span data-stu-id="ff75d-103">Static and Autostatic Routes</span></span>

<span data-ttu-id="ff75d-104">En règle générale, les itinéraires vers des réseaux distants sont obtenus de manière dynamique via des protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="ff75d-104">Typically, routes to remote networks are obtained dynamically through routing protocols.</span></span> <span data-ttu-id="ff75d-105">Toutefois, l’administrateur peut également *amorcer* la table de routage en fournissant des itinéraires manuellement.</span><span class="sxs-lookup"><span data-stu-id="ff75d-105">However, the administrator can also *seed* the routing table by providing routes manually.</span></span> <span data-ttu-id="ff75d-106">Ces itinéraires sont appelés *statiques*.</span><span class="sxs-lookup"><span data-stu-id="ff75d-106">These routes are referred to as *static*.</span></span> <span data-ttu-id="ff75d-107">Un itinéraire statique est associé à une interface qui représente le réseau distant.</span><span class="sxs-lookup"><span data-stu-id="ff75d-107">A static route is associated with an interface that represents the remote network.</span></span> <span data-ttu-id="ff75d-108">Contrairement aux itinéraires dynamiques, les itinéraires statiques sont conservés même si le routeur est redémarré ou si l’interface est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ff75d-108">Unlike dynamic routes, static routes are retained even if the router is restarted or the interface is disabled.</span></span>

<span data-ttu-id="ff75d-109">Un itinéraire *autostatique* est obtenu via un protocole de routage, mais une fois obtenu se comporte comme un itinéraire statique.</span><span class="sxs-lookup"><span data-stu-id="ff75d-109">An *autostatic* route is obtained through a routing protocol, but once obtained behaves like a static route.</span></span> <span data-ttu-id="ff75d-110">Le processus d’obtention des itinéraires autostatiques est le suivant : le gestionnaire de routeur IPX ou IP émet une demande selon laquelle un protocole de routage met à jour les informations de routage pour une interface spécifique.</span><span class="sxs-lookup"><span data-stu-id="ff75d-110">The process for obtaining autostatic routes is as follows: The IP or IPX router manager issues a request that a routing protocol update the routing information for a specific interface.</span></span> <span data-ttu-id="ff75d-111">Les résultats de la mise à jour sont ensuite convertis en itinéraires statiques.</span><span class="sxs-lookup"><span data-stu-id="ff75d-111">The results of the update are then converted into static routes.</span></span> <span data-ttu-id="ff75d-112">Notez que seuls certains protocoles de routage prennent en charge les demandes de mises à jour d’itinéraires autostatiques.</span><span class="sxs-lookup"><span data-stu-id="ff75d-112">Note that only certain routing protocols support requests for autostatic route updates.</span></span>

 

 




