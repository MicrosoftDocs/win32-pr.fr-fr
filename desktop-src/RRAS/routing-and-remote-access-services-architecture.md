---
title: Architecture des services de routage et d’accès à distance
description: L’illustration suivante présente une vue architecturale générale du routeur Windows 2000.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- Routage et accès à distance service RRAS, architecture des services de routage et d’accès à distance RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462343"
---
# <a name="routing-and-remote-access-services-architecture"></a><span data-ttu-id="93e7d-104">Architecture des services de routage et d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="93e7d-104">Routing and Remote Access Services Architecture</span></span>

<span data-ttu-id="93e7d-105">L’illustration suivante présente une vue architecturale générale du routeur Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="93e7d-105">The following illustration presents a general architectural view of the Windows 2000 router.</span></span>

<span data-ttu-id="93e7d-106">Les composants spécifiques à la famille de protocoles IP sont affichés en gris clair.</span><span class="sxs-lookup"><span data-stu-id="93e7d-106">Components that are specific to the IP protocol family are shown in light gray.</span></span> <span data-ttu-id="93e7d-107">Les composants spécifiques à la famille de protocoles IPX sont affichés en gris foncé.</span><span class="sxs-lookup"><span data-stu-id="93e7d-107">Components that are specific to the IPX protocol family are shown in dark gray.</span></span> <span data-ttu-id="93e7d-108">Les composants généraux de toutes les familles de protocoles ne sont pas ombrés.</span><span class="sxs-lookup"><span data-stu-id="93e7d-108">Components that are general to all protocol families are unshaded.</span></span>

<span data-ttu-id="93e7d-109">Le service Routage et accès distant fournit des API pour l’administration et la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="93e7d-109">The Routing and Remote Access Service provides APIs for administering and configuring the service.</span></span> <span data-ttu-id="93e7d-110">Ces API incluent des agents SNMP pour IP et IPX.</span><span class="sxs-lookup"><span data-stu-id="93e7d-110">These APIs include SNMP agents for both IP and IPX.</span></span>

<span data-ttu-id="93e7d-111">RRAS comprend des protocoles de routage pour IP et IPX.</span><span class="sxs-lookup"><span data-stu-id="93e7d-111">RRAS includes routing protocols for both IP and IPX.</span></span> <span data-ttu-id="93e7d-112">Pour l’adresse IP, le service RRAS fournit les protocoles de routage RIP (Routing Information Protocol) et OSPF (Open Shortest Path First).</span><span class="sxs-lookup"><span data-stu-id="93e7d-112">For IP, RRAS provides the Routing Information Protocol (RIP) and Open Shortest Path First (OSPF) routing protocols.</span></span> <span data-ttu-id="93e7d-113">Pour IPX, RRAS fournit le protocole SAP RIP et service Advertising Protocol (SAP).</span><span class="sxs-lookup"><span data-stu-id="93e7d-113">For IPX, RRAS provides IPX RIP and Service Advertising Protocol (SAP).</span></span>

<span data-ttu-id="93e7d-114">RRAS utilise un gestionnaire de tables de routage (RTM) pour les protocoles IP et IPX.</span><span class="sxs-lookup"><span data-stu-id="93e7d-114">RRAS uses one Routing Table Manager (RTM) for both IP and IPX.</span></span> <span data-ttu-id="93e7d-115">Toutefois, chaque famille de protocoles a son propre gestionnaire de routeurs.</span><span class="sxs-lookup"><span data-stu-id="93e7d-115">However, each protocol family has its own Router Manager.</span></span> <span data-ttu-id="93e7d-116">RRAS possède également un composant séparé pour la gestion des groupes de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="93e7d-116">RRAS also has separate component for managing Multicast Groups.</span></span>

<span data-ttu-id="93e7d-117">Interfaces DIM (Dynamic interface Manager) avec les services PPP et TAPI afin de gérer les interfaces PPP utilisées par certains itinéraires.</span><span class="sxs-lookup"><span data-stu-id="93e7d-117">The Dynamic Interface Manager (DIM) interfaces with PPP and TAPI services in order to manage PPP interfaces used by some routes.</span></span>

![vue architecturale générale du routeur Windows 2000](images/rtarch.png)

 

 




