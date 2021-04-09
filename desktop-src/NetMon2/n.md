---
description: Glossaire des termes Moniteur réseau qui commencent par la lettre N.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54404640b13bff3b098b9d223e656e8f1905c055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867018"
---
# <a name="n-network-monitor"></a><span data-ttu-id="49d96-103">N (Moniteur réseau)</span><span class="sxs-lookup"><span data-stu-id="49d96-103">N (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="49d96-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span><span class="sxs-lookup"><span data-stu-id="49d96-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span></span>
</dt> <dd>

<span data-ttu-id="49d96-105">Voir spécification de l’interface du pilote réseau.</span><span class="sxs-lookup"><span data-stu-id="49d96-105">See network driver interface specification.</span></span>

</dd> <dt>

<span data-ttu-id="49d96-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**NDIS (Network Driver Interface Specification)**</span><span class="sxs-lookup"><span data-stu-id="49d96-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**network driver interface specification (NDIS)**</span></span>
</dt> <dd>

<span data-ttu-id="49d96-107">Spécification de l’interface entre les pilotes de périphérique et un réseau.</span><span class="sxs-lookup"><span data-stu-id="49d96-107">The specification for the interface between device drivers and a network.</span></span> <span data-ttu-id="49d96-108">Tous les transports appellent l’interface NDIS pour accéder à et utiliser des cartes d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="49d96-108">All transports call the NDIS interface to access and work with network interface cards.</span></span>

</dd> <dt>

<span data-ttu-id="49d96-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Agent de Moniteur réseau**</span><span class="sxs-lookup"><span data-stu-id="49d96-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Network Monitor agent**</span></span>
</dt> <dd>

<span data-ttu-id="49d96-110">Composant Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="49d96-110">A Network Monitor component.</span></span> <span data-ttu-id="49d96-111">L’agent permet à un ordinateur distant de capturer des données à partir du réseau.</span><span class="sxs-lookup"><span data-stu-id="49d96-111">The agent enables a remote computer to capture data from the network.</span></span> <span data-ttu-id="49d96-112">Lorsqu’une installation Moniteur réseau se connecte à distance à l’agent Moniteur réseau et lance une capture, les statistiques de la capture sont transférées sur le réseau vers l’ordinateur de gestion.</span><span class="sxs-lookup"><span data-stu-id="49d96-112">When a Network Monitor installation connects remotely to the Network Monitor agent and initiates a capture, statistics from the capture are transferred over the network to the managing computer.</span></span> <span data-ttu-id="49d96-113">Le transfert se poursuit à intervalles spécifiés lorsque la connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="49d96-113">The transfer proceeds at intervals specified when the connection is made.</span></span>

</dd> <dt>

<span data-ttu-id="49d96-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**fournisseur de paquets réseau (NPP)**</span><span class="sxs-lookup"><span data-stu-id="49d96-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**network packet provider (NPP)**</span></span>
</dt> <dd>

<span data-ttu-id="49d96-115">Le composant Moniteur réseau qui collecte le trafic réseau dans les trames, puis transmet les trames à un expert et à une application NPP.</span><span class="sxs-lookup"><span data-stu-id="49d96-115">The Network Monitor component that collects network traffic in frames, and then passes the frames to an expert, and NPP application.</span></span> <span data-ttu-id="49d96-116">Un NPP utilise le pilote de système de Moniteur réseau (Nmnt.sys) pour récupérer les trames collectées sur le réseau et fournit plusieurs interfaces COM qui transmettent les trames à un expert, une analyse et une application de fournisseur de paquets réseau (NPP) où elles peuvent être affichées et analysées.</span><span class="sxs-lookup"><span data-stu-id="49d96-116">An NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network, and provides several COM interfaces that pass the frames to an expert, monitor, and network packet provider (NPP) application where they can be displayed and analyzed.</span></span>

</dd> <dt>

<span data-ttu-id="49d96-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span><span class="sxs-lookup"><span data-stu-id="49d96-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span></span>
</dt> <dd>

<span data-ttu-id="49d96-118">Consultez fournisseur de paquets réseau.</span><span class="sxs-lookup"><span data-stu-id="49d96-118">See network packet provider.</span></span>

</dd> <dt>

<span data-ttu-id="49d96-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**Application NPP**</span><span class="sxs-lookup"><span data-stu-id="49d96-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**NPP application**</span></span>
</dt> <dd>

<span data-ttu-id="49d96-120">Une application qui contourne à la fois l’Moniteur réseau l’outil de contrôle de l’interface utilisateur et du contrôle d’analyse et se connecte directement au fournisseur de paquets réseau (NPP).</span><span class="sxs-lookup"><span data-stu-id="49d96-120">An application that bypasses both the Network Monitor UI and Monitor Control Tool, and connects directly to the network packet provider (NPP).</span></span> <span data-ttu-id="49d96-121">Une application NPP peut se connecter au composant NPP avec l’une des cinq interfaces COM NPP.</span><span class="sxs-lookup"><span data-stu-id="49d96-121">An NPP application can connect to the NPP component with any of the five NPP COM interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="49d96-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**Recherche NPP**</span><span class="sxs-lookup"><span data-stu-id="49d96-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP Finder**</span></span>
</dt> <dd>

<span data-ttu-id="49d96-123">Composant Moniteur réseau qui communique avec NPPs.</span><span class="sxs-lookup"><span data-stu-id="49d96-123">The Network Monitor component that communicates with NPPs.</span></span>

</dd> </dl>

 

 



