---
description: Un ensemble d’outils de débogage reposant sur l’API WSDAPI (Web Services on Devices) est disponible dans le SDK Windows et le kit WDK (Windows Driver Kit).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Outils de débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115707"
---
# <a name="debugging-tools"></a><span data-ttu-id="56982-103">Outils de débogage</span><span class="sxs-lookup"><span data-stu-id="56982-103">Debugging Tools</span></span>

<span data-ttu-id="56982-104">Un ensemble d’outils de débogage reposant sur l’API WSDAPI (Web Services on Devices) est disponible dans le SDK Windows et le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="56982-104">A debugging toolset built on Web Services on Devices API (WSDAPI) is available in the Windows SDK and the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="56982-105">Ces outils peuvent être utilisés pour tester les fonctionnalités des applications personnalisées écrites sur WSDAPI, ou sur les périphériques et les clients écrits à l’aide d’autres piles Device Profile for Web Services (DPWS).</span><span class="sxs-lookup"><span data-stu-id="56982-105">These tools can be used to test the functionality of custom applications written on WSDAPI, or devices and clients written using other Device Profile for Web Services (DPWS) stacks.</span></span>

<span data-ttu-id="56982-106">Les outils de débogage WSD (wsddebug \_host.exe) et client de débogage WSD (wsddebug \_client.exe) peuvent être utilisés pour inspecter les caractéristiques des ordinateurs hôtes ou des clients DPWS.</span><span class="sxs-lookup"><span data-stu-id="56982-106">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools can be used to inspect the characteristics of DPWS clients or hosts.</span></span> <span data-ttu-id="56982-107">Elles peuvent également être utilisées pour résoudre les problèmes de connectivité ou de configuration.</span><span class="sxs-lookup"><span data-stu-id="56982-107">They can also be used to troubleshoot connectivity or configuration problems.</span></span> <span data-ttu-id="56982-108">Pour plus d’informations, consultez le [Guide de résolution des problèmes wsdapi](wsdapi-troubleshooting-guide.md).</span><span class="sxs-lookup"><span data-stu-id="56982-108">For more information, see [WSDAPI Troubleshooting Guide](wsdapi-troubleshooting-guide.md).</span></span> <span data-ttu-id="56982-109">Ces outils sont uniquement disponibles dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="56982-109">These tools are only available in the SDK.</span></span> <span data-ttu-id="56982-110">Les outils du kit de développement logiciel se trouvent dans le répertoire suivant : <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="56982-110">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="56982-111">L' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) peut être utilisé pour tester l’interopérabilité au niveau du transport ou au niveau du protocole SOAP (c’est-à-dire s’assurer que les messages sont correctement formés).</span><span class="sxs-lookup"><span data-stu-id="56982-111">The [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) can be used to test SOAP-level or transport-level interoperability (that is, ensuring messages are well-formed).</span></span> <span data-ttu-id="56982-112">Cet outil est disponible uniquement dans le kit WDK.</span><span class="sxs-lookup"><span data-stu-id="56982-112">This tool is only available in the WDK.</span></span>

## <a name="the-wsd-debug-client"></a><span data-ttu-id="56982-113">Client de débogage WSD</span><span class="sxs-lookup"><span data-stu-id="56982-113">The WSD Debug Client</span></span>

<span data-ttu-id="56982-114">Le client de débogage WSD (wsddebug \_client.exe) fournit une console interactive qui peut être utilisée pour envoyer et recevoir des messages WS-Discovery et pour obtenir des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="56982-114">The WSD Debug Client (wsddebug\_client.exe) provides an interactive console that can be used to send and receive WS-Discovery messages, and to obtain metadata.</span></span> <span data-ttu-id="56982-115">Il peut également être utilisé pour générer et consommer des messages de multidiffusion bruts.</span><span class="sxs-lookup"><span data-stu-id="56982-115">It can also be used to generate and consume raw multicast messages.</span></span>

<span data-ttu-id="56982-116">Le client de débogage WSD fonctionne dans l’un des trois modes suivants : multidiffusion, Discovery et Metadata.</span><span class="sxs-lookup"><span data-stu-id="56982-116">The WSD Debug Client operates in one of three modes: multicast, discovery, and metadata.</span></span>



| <span data-ttu-id="56982-117">Mode</span><span class="sxs-lookup"><span data-stu-id="56982-117">Mode</span></span>      | <span data-ttu-id="56982-118">Description</span><span class="sxs-lookup"><span data-stu-id="56982-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56982-119">Multidiffusion</span><span class="sxs-lookup"><span data-stu-id="56982-119">Multicast</span></span> | <span data-ttu-id="56982-120">En mode de multidiffusion, le client de débogage WSD envoie et reçoit des messages de multidiffusion non mis en forme sur le port UDP 3702, comme défini dans WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="56982-120">In Multicast mode, the WSD Debug Client sends and receives unformatted multicast messages on UDP port 3702, as defined in WS-Discovery.</span></span> <span data-ttu-id="56982-121">L’utilisateur peut enregistrer ces messages SOAP dans un fichier texte et peut modifier et rediffuser les messages avec le client de débogage WSD.</span><span class="sxs-lookup"><span data-stu-id="56982-121">The user may save these SOAP messages in a text file, and may modify and rebroadcast the messages with the WSD Debug Client.</span></span>                                                                                                                                 |
| <span data-ttu-id="56982-122">Découverte</span><span class="sxs-lookup"><span data-stu-id="56982-122">Discovery</span></span> | <span data-ttu-id="56982-123">En mode détection, le client de débogage WSD envoie et reçoit des messages WS-Discovery mis en forme.</span><span class="sxs-lookup"><span data-stu-id="56982-123">In Discovery mode, the WSD Debug Client sends and receives formatted WS-Discovery messages.</span></span> <span data-ttu-id="56982-124">Il peut afficher les messages [Hello](hello-message.md), [Bye](bye-message.md), [messages ProbeMatches](probematches-message.md)et [ResolveMatches](resolvematches-message.md) reçus.</span><span class="sxs-lookup"><span data-stu-id="56982-124">It can display received [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md) messages.</span></span> <span data-ttu-id="56982-125">Il peut envoyer des messages de [sonde](probe-message.md) via UDP ou http et [résoudre](resolve-message.md) les messages via UDP.</span><span class="sxs-lookup"><span data-stu-id="56982-125">It can send [Probe](probe-message.md) messages over UDP or HTTP, and [Resolve](resolve-message.md) messages over UDP.</span></span> |
| <span data-ttu-id="56982-126">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="56982-126">Metadata</span></span>  | <span data-ttu-id="56982-127">En plus d’implémenter toutes les fonctionnalités du mode de découverte, le mode métadonnées tente également de récupérer les métadonnées des appareils.</span><span class="sxs-lookup"><span data-stu-id="56982-127">In addition to implementing all of the features of Discovery mode, Metadata mode also attempts to retrieve metadata from devices.</span></span>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="56982-128">Pour plus d’informations, consultez [utilisation d’un hôte et d’un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md), [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md)et [utilisation du client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="56982-128">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md), and [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

## <a name="the-wsd-debug-host"></a><span data-ttu-id="56982-129">Hôte de débogage WSD</span><span class="sxs-lookup"><span data-stu-id="56982-129">The WSD Debug Host</span></span>

<span data-ttu-id="56982-130">L’hôte de débogage WSD (wsddebug \_host.exe) fournit une console interactive utilisée pour annoncer l’hôte, répondre aux demandes des clients et imprimer les informations de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="56982-130">The WSD Debug Host (wsddebug\_host.exe) provides an interactive console used to announce the host, respond to client requests, and print diagnostic information.</span></span>

<span data-ttu-id="56982-131">L’hôte de débogage WSD fonctionne dans l’un des deux modes suivants : découverte et métadonnées.</span><span class="sxs-lookup"><span data-stu-id="56982-131">The WSD Debug Host operates in one of two modes: discovery and metadata.</span></span>



| <span data-ttu-id="56982-132">Mode</span><span class="sxs-lookup"><span data-stu-id="56982-132">Mode</span></span>      | <span data-ttu-id="56982-133">Description</span><span class="sxs-lookup"><span data-stu-id="56982-133">Description</span></span>                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56982-134">Découverte</span><span class="sxs-lookup"><span data-stu-id="56982-134">Discovery</span></span> | <span data-ttu-id="56982-135">En mode détection, l’hôte de débogage WSD imprime les messages mis en forme WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="56982-135">In Discovery mode, the WSD Debug Host prints formatted WS-Discovery messages.</span></span> <span data-ttu-id="56982-136">Il envoie également des messages de [salutation](hello-message.md) et de [Bye](bye-message.md) , et répond automatiquement aux messages de [sondage](probe-message.md) et de [résolution](resolve-message.md) .</span><span class="sxs-lookup"><span data-stu-id="56982-136">It also sends [Hello](hello-message.md) and [Bye](bye-message.md) messages, and automatically responds to [Probe](probe-message.md) and [Resolve](resolve-message.md) messages.</span></span> |
| <span data-ttu-id="56982-137">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="56982-137">Metadata</span></span>  | <span data-ttu-id="56982-138">En plus d’implémenter toutes les fonctionnalités du mode de découverte, le mode métadonnées publie un service de métadonnées et permet aux clients de se connecter et d’effectuer l’échange de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="56982-138">In addition to implementing all of the features of Discovery mode, Metadata mode advertises a metadata service and allows clients to connect and perform metadata exchange.</span></span>                                                                                       |



 

<span data-ttu-id="56982-139">Pour plus d’informations, consultez [utilisation d’un hôte et d’un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md) et [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="56982-139">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) and [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56982-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56982-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56982-141">Développement d’applications WSD sur Windows</span><span class="sxs-lookup"><span data-stu-id="56982-141">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="56982-142">Outils de développement WSDAPI</span><span class="sxs-lookup"><span data-stu-id="56982-142">WSDAPI Development Tools</span></span>](wsdapi-development-tools.md)
</dt> <dt>

[<span data-ttu-id="56982-143">Guide de résolution des problèmes WSDAPI</span><span class="sxs-lookup"><span data-stu-id="56982-143">WSDAPI Troubleshooting Guide</span></span>](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



