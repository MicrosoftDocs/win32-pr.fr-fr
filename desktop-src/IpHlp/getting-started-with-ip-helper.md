---
description: Voici un guide pas à pas de la programmation à l’aide de l’interface de programmation d’applications (API) d’assistance IP. Il est conçu pour vous permettre de comprendre les fonctions d’assistance IP de base et les structures de données, et comment elles fonctionnent ensemble.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Prise en main avec l’assistance IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869069"
---
# <a name="getting-started-with-ip-helper"></a><span data-ttu-id="2b8e8-104">Prise en main avec l’assistance IP</span><span class="sxs-lookup"><span data-stu-id="2b8e8-104">Getting Started with IP Helper</span></span>

<span data-ttu-id="2b8e8-105">Voici un guide pas à pas de la programmation à l’aide de l’interface de programmation d’applications (API) d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-105">The following is a step-by-step guide to getting started programming using the IP Helper application programming interface (API).</span></span> <span data-ttu-id="2b8e8-106">Il est conçu pour vous permettre de comprendre les fonctions d’assistance IP de base et les structures de données, et comment elles fonctionnent ensemble.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-106">It is designed to provide an understanding of basic IP Helper functions and data structures, and how they work together.</span></span>

<span data-ttu-id="2b8e8-107">L’application utilisée pour l’illustration est une application d’assistance IP très basique.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-107">The application that is used for illustration is a very basic IP Helper application.</span></span> <span data-ttu-id="2b8e8-108">Des exemples de code plus avancés sont inclus dans les exemples inclus dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-108">More advanced code examples are included in the samples included with the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="2b8e8-109">La première étape est la même pour la plupart des applications d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-109">The first step is the same for most IP Helper applications.</span></span>

-   [<span data-ttu-id="2b8e8-110">Création d’une application d’assistance IP de base</span><span class="sxs-lookup"><span data-stu-id="2b8e8-110">Creating a Basic IP Helper Application</span></span>](creating-a-basic-ip-helper-application.md)

<span data-ttu-id="2b8e8-111">Les sections suivantes décrivent les étapes restantes pour créer cette application d’assistance IP de base.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-111">The following sections describe the remaining steps for creating this basic IP Helper application.</span></span>

-   [<span data-ttu-id="2b8e8-112">Récupération d’informations à l’aide de GetNetworkParams</span><span class="sxs-lookup"><span data-stu-id="2b8e8-112">Retrieving Information Using GetNetworkParams</span></span>](retrieving-information-using-getnetworkparams.md)
-   [<span data-ttu-id="2b8e8-113">Gestion des cartes réseau à l’aide de GetAdaptersInfo</span><span class="sxs-lookup"><span data-stu-id="2b8e8-113">Managing Network Adapters Using GetAdaptersInfo</span></span>](managing-network-adapters-using-getadaptersinfo.md)
-   [<span data-ttu-id="2b8e8-114">Gestion des interfaces à l’aide de GetInterfaceInfo</span><span class="sxs-lookup"><span data-stu-id="2b8e8-114">Managing Interfaces Using GetInterfaceInfo</span></span>](managing-interfaces-using-getinterfaceinfo.md)
-   [<span data-ttu-id="2b8e8-115">Gestion des adresses IP à l’aide de GetIpAddrTable</span><span class="sxs-lookup"><span data-stu-id="2b8e8-115">Managing IP Addresses Using GetIpAddrTable</span></span>](managing-ip-addresses-using-getipaddrtable.md)
-   [<span data-ttu-id="2b8e8-116">Gestion des baux DHCP à l’aide de IpReleaseAddress et IpRenewAddress</span><span class="sxs-lookup"><span data-stu-id="2b8e8-116">Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress</span></span>](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [<span data-ttu-id="2b8e8-117">Gestion des adresses IP à l’aide de AddIPAddress et DeleteIPAddress</span><span class="sxs-lookup"><span data-stu-id="2b8e8-117">Managing IP Addresses Using AddIPAddress and DeleteIPAddress</span></span>](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [<span data-ttu-id="2b8e8-118">Récupération d’informations à l’aide de GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="2b8e8-118">Retrieving Information Using GetIpStatistics</span></span>](retrieving-information-using-getipstatistics.md)
-   [<span data-ttu-id="2b8e8-119">Récupération d’informations à l’aide de GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="2b8e8-119">Retrieving Information Using GetTcpStatistics</span></span>](retrieving-information-using-gettcpstatistics.md)

<span data-ttu-id="2b8e8-120">Le code source complet de cet exemple d’assistance IP de base.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-120">The complete source code for this basic IP Helper example.</span></span>

-   [<span data-ttu-id="2b8e8-121">Code source complet de l’application d’assistance IP</span><span class="sxs-lookup"><span data-stu-id="2b8e8-121">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a><span data-ttu-id="2b8e8-122">Exemples avancés d’assistance IP</span><span class="sxs-lookup"><span data-stu-id="2b8e8-122">Advanced IP Helper Samples</span></span>

<span data-ttu-id="2b8e8-123">Plusieurs exemples plus avancés d’assistance IP sont inclus dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-123">Several more advanced IP Helper samples are included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2b8e8-124">Par défaut, l’exemple de code source du programme d’assistance IP est installé par la SDK Windows publiée pour Windows 7 dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="2b8e8-124">By default, the IP Helper sample source code is installed by the Windows SDK released for Windows 7 in the following directory:</span></span>

<span data-ttu-id="2b8e8-125">*C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ NetDs \\ IPHelp*</span><span class="sxs-lookup"><span data-stu-id="2b8e8-125">*C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\IPHelp*</span></span>

<span data-ttu-id="2b8e8-126">Les exemples plus avancés répertoriés ci-dessous se trouvent dans les répertoires suivants :</span><span class="sxs-lookup"><span data-stu-id="2b8e8-126">The more advanced samples listed below are found in the following directories:</span></span>

-   <span data-ttu-id="2b8e8-127">EnableRouter</span><span class="sxs-lookup"><span data-stu-id="2b8e8-127">EnableRouter</span></span>

    <span data-ttu-id="2b8e8-128">Ce répertoire contient un exemple qui montre comment utiliser les fonctions d’assistance IP [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) et [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) pour activer et désactiver le transfert IPv4 sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-128">This directory contains a sample that demonstrates how to use the [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) and [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP Helper functions to enable and disable IPv4 forwarding on the local computer.</span></span>

-   <span data-ttu-id="2b8e8-129">iparp</span><span class="sxs-lookup"><span data-stu-id="2b8e8-129">iparp</span></span>

    <span data-ttu-id="2b8e8-130">Ce répertoire contient un exemple de programme qui montre comment utiliser les fonctions d’assistance IP pour afficher et manipuler des entrées dans la table ARP IPv4 sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-130">This directory contains a sample program that demonstrates how to use the IP Helper functions to display and manipulate entries in the IPv4 ARP table on the local computer.</span></span>

-   <span data-ttu-id="2b8e8-131">ipchange</span><span class="sxs-lookup"><span data-stu-id="2b8e8-131">ipchange</span></span>

    <span data-ttu-id="2b8e8-132">Ce répertoire contient un exemple de programme qui montre comment utiliser les fonctions d’assistance IP pour modifier par programmation une adresse IP pour une carte réseau spécifique sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-132">This directory contains a sample program that demonstrates how to use IP Helper functions to programmatically change an IP address for a specific network adapter on your machine.</span></span> <span data-ttu-id="2b8e8-133">Ce programme montre également comment récupérer les informations de configuration IP d’une carte réseau existante.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-133">This program also demonstrates how to retrieve existing network adapter IP configuration information.</span></span>

-   <span data-ttu-id="2b8e8-134">IPConfig</span><span class="sxs-lookup"><span data-stu-id="2b8e8-134">IPConfig</span></span>

    <span data-ttu-id="2b8e8-135">Ce répertoire contient un exemple de programme qui montre comment récupérer par programme des informations de configuration IPv4 similaires à l’utilitaire IPCONFIG.EXE.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-135">This directory contains a sample program that demonstrates how to programmatically retrieve IPv4 configuration information similar to the IPCONFIG.EXE utility.</span></span> <span data-ttu-id="2b8e8-136">Il montre comment utiliser les fonctions [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) et [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="2b8e8-136">It demonstrates how to use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) and [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) functions.</span></span> <span data-ttu-id="2b8e8-137">Notez que la fonction **GetAdaptersInfo** récupère uniquement les informations IPv4.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-137">Note that the **GetAdaptersInfo** function only retrieves IPv4 information.</span></span>

-   <span data-ttu-id="2b8e8-138">IPRenew</span><span class="sxs-lookup"><span data-stu-id="2b8e8-138">IPRenew</span></span>

    <span data-ttu-id="2b8e8-139">Ce répertoire contient un exemple de programme qui montre comment libérer par programmation et renouveler des adresses IPv4 obtenues par le biais de DHCP.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-139">This directory contains a sample program that demonstrates how to programmatically release and renew IPv4 addresses obtained through DHCP.</span></span> <span data-ttu-id="2b8e8-140">Ce programme montre également comment récupérer des informations de configuration de carte réseau existantes.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-140">This program also demonstrates how to retrieve existing network adapter configuration information.</span></span>

-   <span data-ttu-id="2b8e8-141">IPRoute</span><span class="sxs-lookup"><span data-stu-id="2b8e8-141">IPRoute</span></span>

    <span data-ttu-id="2b8e8-142">Ce répertoire contient un exemple de programme qui montre comment utiliser les fonctions d’assistance IP pour manipuler la table de routage IPv4.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-142">This directory contains a sample program that demonstrates how to use the IP Helper functions to manipulate the IPv4 routing table.</span></span>

-   <span data-ttu-id="2b8e8-143">ipstat</span><span class="sxs-lookup"><span data-stu-id="2b8e8-143">ipstat</span></span>

    <span data-ttu-id="2b8e8-144">Ce répertoire contient un exemple de programme qui montre comment utiliser les fonctions d’assistance IP pour afficher les connexions IPv4 pour un protocole.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-144">This directory contains a sample program that demonstrates how to use the IP Helper functions to show IPv4 connections for a protocol.</span></span> <span data-ttu-id="2b8e8-145">Par défaut, les statistiques sont indiquées pour IP, ICMP, TCP et UDP.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-145">By default, statistics are shown for IP, ICMP, TCP and UDP.</span></span>

-   <span data-ttu-id="2b8e8-146">NetInfo</span><span class="sxs-lookup"><span data-stu-id="2b8e8-146">Netinfo</span></span>

    <span data-ttu-id="2b8e8-147">Ce répertoire contient un exemple de programme qui montre comment utiliser les nouvelles API d’assistance IP introduites sur Windows Vista et versions ultérieures pour afficher/modifier les informations d’adresse et d’interface pour IPv4 et IPv6.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-147">This directory contains a sample program that demonstrates how to the use the new IP Helper APIs introduced on Windows Vista and later to display/change address and interface information for IPv4 and IPv6.</span></span>

 

 



