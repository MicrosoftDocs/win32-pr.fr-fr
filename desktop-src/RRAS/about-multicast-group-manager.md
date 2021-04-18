---
title: À propos du gestionnaire de groupe de multidiffusion
description: Cette documentation décrit la technologie du gestionnaire de groupe de multidiffusion (MGM).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- Gestionnaire de groupe de multidiffusion RRAS
- Gestionnaire de groupe de multidiffusion RRAS, Description
- Routage et accès à distance service RRAS, gestionnaire de groupe de multidiffusion
- Routage et accès à distance service RRAS, gestionnaire de groupe de multidiffusion, décrit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512668"
---
# <a name="about-multicast-group-manager"></a><span data-ttu-id="0003d-107">À propos du gestionnaire de groupe de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="0003d-107">About Multicast Group Manager</span></span>

<span data-ttu-id="0003d-108">Cette documentation décrit la technologie du gestionnaire de groupe de multidiffusion (MGM).</span><span class="sxs-lookup"><span data-stu-id="0003d-108">This documentation describes the Multicast Group Manager (MGM) technology.</span></span>

<span data-ttu-id="0003d-109">La multidiffusion permet à un hôte d’envoyer des données uniquement aux destinations qui demandent spécifiquement de recevoir les données.</span><span class="sxs-lookup"><span data-stu-id="0003d-109">Multicasting allows a host to send data to only those destinations that specifically request to receive the data.</span></span> <span data-ttu-id="0003d-110">De cette façon, la multidiffusion diffère de l’envoi des données de diffusion, car les données de diffusion sont envoyées à tous les ordinateurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="0003d-110">In this way, multicasting differs from sending broadcast data, since broadcast data is sent to all hosts.</span></span>

<span data-ttu-id="0003d-111">La multidiffusion économise la bande passante réseau, car les données de multidiffusion ne sont reçues que par les hôtes qui demandent les données, et les données transitent sur n’importe quel lien une seule fois.</span><span class="sxs-lookup"><span data-stu-id="0003d-111">Multicasting saves network bandwidth because multicast data is only received by those hosts that request the data, and the data travels over any link only once.</span></span> <span data-ttu-id="0003d-112">La multidiffusion économise la bande passante du serveur, car un serveur ne doit envoyer qu’un seul message de multidiffusion par réseau au lieu d’un message de monodiffusion par récepteur.</span><span class="sxs-lookup"><span data-stu-id="0003d-112">Multicasting saves server bandwidth because a server has to send only one multicast message per network instead of one unicast message per receiver.</span></span> <span data-ttu-id="0003d-113">Les réunions en ligne et la radio Internet sont des exemples d’applications de multidiffusion populaires.</span><span class="sxs-lookup"><span data-stu-id="0003d-113">Examples of popular multicast applications are online meetings and Internet radio.</span></span>

<span data-ttu-id="0003d-114">L’API MGM permet aux développeurs d’écrire des protocoles de routage multidiffusion qui interagissent avec les routeurs exécutant le gestionnaire de groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="0003d-114">The MGM API enables developers to write multicast routing protocols that interoperate with routers running the multicast group manager.</span></span>

<span data-ttu-id="0003d-115">Lorsque plusieurs protocoles de routage multidiffusion sont activés sur un routeur, le gestionnaire de groupe de multidiffusion coordonne les opérations entre tous les protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="0003d-115">When more than one multicast routing protocol is enabled on a router, the multicast group manager coordinates operations between all routing protocols.</span></span> <span data-ttu-id="0003d-116">Le gestionnaire de groupe de multidiffusion informe chaque protocole de routage lorsque des modifications d’appartenance au groupe se produisent, et lorsque des données de multidiffusion provenant d’une nouvelle source ou qui sont destinées à un nouveau groupe sont reçues.</span><span class="sxs-lookup"><span data-stu-id="0003d-116">The multicast group manager informs each routing protocol when group membership changes occur, and when multicast data from a new source or destined to a new group is received.</span></span>

<span data-ttu-id="0003d-117">L’API MGM offre les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="0003d-117">The MGM API provides the following features:</span></span>

-   <span data-ttu-id="0003d-118">Inscription de protocole</span><span class="sxs-lookup"><span data-stu-id="0003d-118">Protocol registration</span></span>
-   <span data-ttu-id="0003d-119">Gestion des groupes</span><span class="sxs-lookup"><span data-stu-id="0003d-119">Group management</span></span>
-   <span data-ttu-id="0003d-120">Énumération de l’entrée de transfert multidiffusion (MFE)</span><span class="sxs-lookup"><span data-stu-id="0003d-120">Multicast forwarding entry (MFE) enumeration</span></span>
-   <span data-ttu-id="0003d-121">Définitions de rappel pour les protocoles de routage de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="0003d-121">Callback definitions for multicast routing protocols</span></span>

<span data-ttu-id="0003d-122">Cette vue d’ensemble décrit les composants de l’architecture de multidiffusion, les scénarios clients utilisés pour interagir avec le gestionnaire de groupe de multidiffusion, ainsi que les considérations en matière de programmation pour l’utilisation de l’API MGM.</span><span class="sxs-lookup"><span data-stu-id="0003d-122">This overview describes the components of the multicast architecture, the client scenarios that are used to interoperate with the multicast group manager, and programming considerations for using the MGM API.</span></span>

 

 




