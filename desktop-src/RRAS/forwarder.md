---
title: Redirecteur
description: Le redirecteur est le composant en mode noyau du routeur qui est responsable du transfert des données d’une interface de routeur vers les autres.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029258"
---
# <a name="forwarder"></a><span data-ttu-id="2e201-103">Redirecteur</span><span class="sxs-lookup"><span data-stu-id="2e201-103">Forwarder</span></span>

<span data-ttu-id="2e201-104">Le redirecteur est le composant en mode noyau du routeur qui est responsable du transfert des données d’une interface de routeur vers les autres.</span><span class="sxs-lookup"><span data-stu-id="2e201-104">The forwarder is the kernel-mode component of the router that is responsible for forwarding data from one router interface to the others.</span></span> <span data-ttu-id="2e201-105">Le redirecteur décide également si un paquet est destiné à une remise locale, s’il est destiné à être transféré hors d’une autre interface, ou les deux à la fois.</span><span class="sxs-lookup"><span data-stu-id="2e201-105">The forwarder also decides whether a packet is destined for local delivery, whether it is destined to be forwarded out of another interface, or both.</span></span>

<span data-ttu-id="2e201-106">Il existe deux redirecteurs en mode noyau : monodiffusion et multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="2e201-106">There are two kernel-mode forwarders: unicast and multicast.</span></span>

<span data-ttu-id="2e201-107">Le gestionnaire de routeur obtient les meilleurs itinéraires vers toutes les destinations du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="2e201-107">The router manager obtains the best routes to all destinations from the routing table manager.</span></span> <span data-ttu-id="2e201-108">Ces itinéraires sont passés au redirecteur de monodiffusion.</span><span class="sxs-lookup"><span data-stu-id="2e201-108">These routes are passed to the unicast forwarder.</span></span> <span data-ttu-id="2e201-109">Le redirecteur de monodiffusion utilise ces itinéraires pour effectuer le transfert réel des données de monodiffusion.</span><span class="sxs-lookup"><span data-stu-id="2e201-109">The unicast forwarder uses these routes to perform the actual forwarding of unicast data.</span></span> <span data-ttu-id="2e201-110">De cette façon, le redirecteur de monodiffusion gère un cache des meilleurs itinéraires dans la vue de monodiffusion de la table de routage.</span><span class="sxs-lookup"><span data-stu-id="2e201-110">In this manner, the unicast forwarder maintains a cache of the best routes in the unicast view of the routing table.</span></span>

<span data-ttu-id="2e201-111">Le gestionnaire de groupe de multidiffusion utilise les informations de la vue multidiffusion de la table de routage pour ajouter des entrées de transfert de multidiffusion au redirecteur de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="2e201-111">The multicast group manager uses information from the multicast view of the routing table to add multicast forwarding entries to the multicast forwarder.</span></span>

 

 




