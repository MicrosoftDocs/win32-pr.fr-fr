---
description: Dans l’infrastructure WMI, le service WMI (WinMgmt) est le composant du système d’exploitation qui agit en tant que médiateur entre les applications de gestion et les fournisseurs de données WMI. Le référentiel WMI est une zone de stockage pour les données statiques relatives à WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infrastructure WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529772"
---
# <a name="wmi-infrastructure"></a><span data-ttu-id="a8544-104">Infrastructure WMI</span><span class="sxs-lookup"><span data-stu-id="a8544-104">WMI Infrastructure</span></span>

<span data-ttu-id="a8544-105">Dans l’infrastructure WMI, le service WMI (WinMgmt) est le composant du système d’exploitation qui agit en tant que médiateur entre les applications de gestion et les [*fournisseurs*](gloss-p.md)de données WMI.</span><span class="sxs-lookup"><span data-stu-id="a8544-105">In the WMI infrastructure, the WMI service (Winmgmt) is the operating system component that acts as the mediator between management applications and WMI data [*providers*](gloss-p.md).</span></span> <span data-ttu-id="a8544-106">Le [*référentiel WMI*](gloss-w.md) est une zone de stockage pour les données statiques relatives à WMI.</span><span class="sxs-lookup"><span data-stu-id="a8544-106">The [*WMI repository*](gloss-w.md) is a storage area for WMI-related static data.</span></span>

<span data-ttu-id="a8544-107">Le service WMI est implémenté en tant que processus de service au sein d’un processus hôte de service partagé (SVCHOST).</span><span class="sxs-lookup"><span data-stu-id="a8544-107">The WMI service is implemented as a service process within a shared service host process (SVCHOST).</span></span> <span data-ttu-id="a8544-108">Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="a8544-108">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="a8544-109">Le service WMI démarre lorsque la première application ou le script de gestion effectue un appel pour se connecter à un espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="a8544-109">The WMI service starts when the first management application or script makes a call to connect to a WMI namespace.</span></span> <span data-ttu-id="a8544-110">Selon la configuration, le service WMI peut s’arrêter ou passer à un profil de mémoire insuffisante lorsqu’il n’est pas appelé par une application de gestion.</span><span class="sxs-lookup"><span data-stu-id="a8544-110">Depending on the setup, the WMI service may shut down or go into a low memory profile when not being called by a management application.</span></span>

<span data-ttu-id="a8544-111">Le service WMI interagit avec les applications de gestion par le biais de l’interface COM.</span><span class="sxs-lookup"><span data-stu-id="a8544-111">The WMI service interacts with management applications through the COM interface.</span></span> <span data-ttu-id="a8544-112">Lorsqu’une application effectue une requête via l’interface, WMI détermine si la requête concerne des données statiques ou dynamiques.</span><span class="sxs-lookup"><span data-stu-id="a8544-112">When an application makes a request through the interface, WMI determines whether the request is for static or dynamic data.</span></span> <span data-ttu-id="a8544-113">Si la requête implique des données statiques, telles que le nom d’un objet géré, WMI récupère les données du référentiel.</span><span class="sxs-lookup"><span data-stu-id="a8544-113">If the request involves static data, such as the name of a managed object, WMI retrieves the data from the repository.</span></span> <span data-ttu-id="a8544-114">Si la requête implique des données dynamiques, telles que la quantité de mémoire qu’un objet managé utilise actuellement, WMI transmet la demande à un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a8544-114">If the request involves dynamic data, such as the amount of memory a managed object is currently using, WMI passes the request on to a provider.</span></span>

<span data-ttu-id="a8544-115">Les fournisseurs inscrivent leur emplacement auprès du service WMI, qui permet à WMI d’acheminer les demandes de données.</span><span class="sxs-lookup"><span data-stu-id="a8544-115">Providers register their location with the WMI service, which allows WMI to route data requests.</span></span> <span data-ttu-id="a8544-116">Un fournisseur enregistre également la prise en charge de certaines opérations, telles que la récupération de données, la modification, la suppression, l’énumération ou le traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="a8544-116">A provider also registers support for particular operations, such as data retrieval, modification, deletion, enumeration, or query processing.</span></span> <span data-ttu-id="a8544-117">Le service WMI utilise les informations d’inscription du fournisseur pour faire correspondre les demandes d’application avec le fournisseur approprié.</span><span class="sxs-lookup"><span data-stu-id="a8544-117">The WMI service uses the provider registration information to match application requests with the appropriate provider.</span></span> <span data-ttu-id="a8544-118">WMI utilise également les informations d’inscription pour charger et décharger les fournisseurs, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a8544-118">WMI also uses the registration information to load and unload providers, as necessary.</span></span> <span data-ttu-id="a8544-119">Lorsqu’un fournisseur termine le traitement d’une demande, le fournisseur renvoie le résultat au service WMI.</span><span class="sxs-lookup"><span data-stu-id="a8544-119">When a provider finishes processing a request, the provider returns the result back to the WMI service.</span></span> <span data-ttu-id="a8544-120">WMI transmet ensuite le résultat à l’application par le biais de l’interface COM.</span><span class="sxs-lookup"><span data-stu-id="a8544-120">WMI then forwards the result on to the application through the COM interface.</span></span> <span data-ttu-id="a8544-121">Pour plus d’informations, consultez [fourniture de données à WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a8544-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="a8544-122">WMI utilise [le suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) pour enregistrer l’activité du service WMI.</span><span class="sxs-lookup"><span data-stu-id="a8544-122">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) to record WMI service activity.</span></span>

<span data-ttu-id="a8544-123">Étant donné que l’infrastructure gère tout le trafic entre les fournisseurs et les applications de gestion, l’infrastructure fournit les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8544-123">Because the infrastructure handles all traffic between the providers and the management applications, the infrastructure provides the following features:</span></span>

-   <span data-ttu-id="a8544-124">Prise en charge des notifications d’événements</span><span class="sxs-lookup"><span data-stu-id="a8544-124">Event Notification Support</span></span>

    <span data-ttu-id="a8544-125">Pour plus d’informations, consultez [surveillance des événements](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="a8544-125">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="a8544-126">Prise en charge du langage de requête</span><span class="sxs-lookup"><span data-stu-id="a8544-126">Query Language Support</span></span>

    <span data-ttu-id="a8544-127">Pour plus d’informations, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="a8544-127">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

-   <span data-ttu-id="a8544-128">Support sécurité</span><span class="sxs-lookup"><span data-stu-id="a8544-128">Security Support</span></span>

    <span data-ttu-id="a8544-129">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="a8544-129">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

-   <span data-ttu-id="a8544-130">Écriture de scripts pour l’accès aux données des compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="a8544-130">Scripting Access to Performance Counter Data</span></span>

    <span data-ttu-id="a8544-131">Pour plus d’informations, consultez [analyse des données de performances](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="a8544-131">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8544-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8544-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8544-133">Architecture WMI</span><span class="sxs-lookup"><span data-stu-id="a8544-133">WMI Architecture</span></span>](wmi-architecture.md)
</dt> </dl>

 

 
