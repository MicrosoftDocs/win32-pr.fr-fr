---
title: Routage
description: Les API de routage permettent de créer des applications pour administrer les fonctionnalités de routage du système d’exploitation.
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- Routage RAS
- Routage RAS, page de démarrage
- RAS RRAS
- RAS RRAS, voir routage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e3b2a92a6c54f47693d657315ec0a48e660061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842669"
---
# <a name="routing"></a><span data-ttu-id="5cb13-107">Routage</span><span class="sxs-lookup"><span data-stu-id="5cb13-107">Routing</span></span>

## <a name="purpose"></a><span data-ttu-id="5cb13-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="5cb13-108">Purpose</span></span>

<span data-ttu-id="5cb13-109">Les API de routage permettent de créer des applications pour administrer les fonctionnalités de routage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5cb13-109">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5cb13-110">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="5cb13-110">Where applicable</span></span>

<span data-ttu-id="5cb13-111">Le routage permet à un ordinateur de fonctionner en tant que routeur réseau.</span><span class="sxs-lookup"><span data-stu-id="5cb13-111">Routing makes it possible for a computer to function as a network router.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5cb13-112">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="5cb13-112">Developer audience</span></span>

<span data-ttu-id="5cb13-113">Les API de routage sont conçues pour être utilisées par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="5cb13-113">The Routing APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="5cb13-114">Les programmeurs doivent également être familiarisés avec les concepts de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="5cb13-114">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5cb13-115">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="5cb13-115">Run-time requirements</span></span>

<span data-ttu-id="5cb13-116">Le routage est une technologie serveur.</span><span class="sxs-lookup"><span data-stu-id="5cb13-116">Routing is a server-based technology.</span></span> <span data-ttu-id="5cb13-117">Toutes les fonctionnalités du routage sont intégrées à Windows 2000 Server et à Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5cb13-117">All the functionality of Routing is incorporated into Windows 2000 Server and the Windows Server 2003.</span></span> <span data-ttu-id="5cb13-118">Les applications de routage ne peuvent pas s’exécuter sur Windows NT Workstation 4,0 ou sur des systèmes d’exploitation clients, tels que Windows 95.</span><span class="sxs-lookup"><span data-stu-id="5cb13-118">Routing applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="5cb13-119">Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous aux sections relatives à la configuration requise dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="5cb13-119">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5cb13-120">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="5cb13-120">In this section</span></span>



| <span data-ttu-id="5cb13-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5cb13-121">Topic</span></span>                                                                                               | <span data-ttu-id="5cb13-122">Description</span><span class="sxs-lookup"><span data-stu-id="5cb13-122">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cb13-123">Gestion de routeur</span><span class="sxs-lookup"><span data-stu-id="5cb13-123">Router Management</span></span>](about-router-management.md)<br/>                                         | <span data-ttu-id="5cb13-124">L’API d’administration de routeur permet aux développeurs de créer des applications pour gérer le service de routeur sur un ordinateur exécutant Windows 2000 Server et des systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="5cb13-124">The router administration API allows developers to create applications to manage the router service on a computer running Windows 2000 Server and later operating systems.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="5cb13-125">Bases d’informations de gestion et gestionnaires de routeur</span><span class="sxs-lookup"><span data-stu-id="5cb13-125">Router Managers and Management Information Base</span></span>](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | <span data-ttu-id="5cb13-126">Les API MIB (Management Information base) pour la gestion de routeur permettent d’interroger et de définir les valeurs des variables MIB exportées par l’un des gestionnaires de routeur ou l’un des protocoles de routage utilisés par le service gestionnaires de routeur.</span><span class="sxs-lookup"><span data-stu-id="5cb13-126">The Management Information Base (MIB) APIs for router management makes it possible to query and set the values of MIB variables exported by one of the router managers or any of the routing protocols that the router managers service.</span></span> <span data-ttu-id="5cb13-127">À l’aide de cette API, le routeur prend en charge le protocole SNMP (simple Network Management Protocol).</span><span class="sxs-lookup"><span data-stu-id="5cb13-127">By using this API, the router supports the Simple Network Management Protocol (SNMP).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5cb13-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5cb13-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cb13-129">Fonctions de l’assistance IP</span><span class="sxs-lookup"><span data-stu-id="5cb13-129">IP Helper Functions</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="5cb13-130">Accès à distance</span><span class="sxs-lookup"><span data-stu-id="5cb13-130">Remote Access</span></span>](remote-access-start-page.md)
</dt> <dt>

[<span data-ttu-id="5cb13-131">Protocoles de routage</span><span class="sxs-lookup"><span data-stu-id="5cb13-131">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

