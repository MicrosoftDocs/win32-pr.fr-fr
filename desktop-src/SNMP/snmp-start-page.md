---
title: Service SNMP
description: L’implémentation Microsoft Windows du protocole SNMP (simple Network Management Protocol) est utilisée pour configurer des appareils distants, surveiller les performances du réseau, auditer l’utilisation du réseau et détecter les erreurs réseau ou un accès inapproprié. Important l’API Microsoft Windows SNMP ne prend en charge que les versions de protocole jusqu’à SNMPv2C. Elle ne prend pas en charge les versions ultérieures du protocole.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031737"
---
# <a name="snmp-service"></a><span data-ttu-id="9ab30-106">Service SNMP</span><span class="sxs-lookup"><span data-stu-id="9ab30-106">SNMP Service</span></span>

<span data-ttu-id="9ab30-107">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="9ab30-107">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ab30-108">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9ab30-108">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9ab30-109">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="9ab30-109">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

## <a name="purpose"></a><span data-ttu-id="9ab30-110">Objectif</span><span class="sxs-lookup"><span data-stu-id="9ab30-110">Purpose</span></span>

<span data-ttu-id="9ab30-111">L’implémentation Microsoft Windows du protocole SNMP (simple Network Management Protocol) est utilisée pour configurer des appareils distants, surveiller les performances du réseau, auditer l’utilisation du réseau et détecter les erreurs réseau ou un accès inapproprié.</span><span class="sxs-lookup"><span data-stu-id="9ab30-111">The Microsoft Windows implementation of the Simple Network Management Protocol (SNMP) is used to configure remote devices, monitor network performance, audit network usage, and detect network faults or inappropriate access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ab30-112">L’API Microsoft Windows SNMP ne prend en charge que les versions de protocole allant jusqu’à SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9ab30-112">The Microsoft Windows SNMP API only supports protocol versions up to SNMPv2C.</span></span> <span data-ttu-id="9ab30-113">Elle ne prend pas en charge les versions ultérieures du protocole.</span><span class="sxs-lookup"><span data-stu-id="9ab30-113">It does not support any later versions of the protocol.</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="9ab30-114">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="9ab30-114">Where applicable</span></span>

<span data-ttu-id="9ab30-115">SNMP utilise une architecture distribuée composée d’applications de gestion et d’applications d’agent.</span><span class="sxs-lookup"><span data-stu-id="9ab30-115">SNMP uses a distributed architecture consisting of management applications and agent applications.</span></span> <span data-ttu-id="9ab30-116">Le service SNMP implémente un agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="9ab30-116">The SNMP service implements an SNMP agent.</span></span> <span data-ttu-id="9ab30-117">Pour utiliser les informations fournies par le service SNMP, vous devez disposer d’au moins un ordinateur hôte exécutant une application de gestion SNMP.</span><span class="sxs-lookup"><span data-stu-id="9ab30-117">To use the information the SNMP service provides, you must have at least one host that is running an SNMP management application.</span></span> <span data-ttu-id="9ab30-118">Vous pouvez utiliser un logiciel de gestion SNMP tiers ou vous pouvez développer votre propre application de gestion SNMP.</span><span class="sxs-lookup"><span data-stu-id="9ab30-118">You can use third-party SNMP management software, or you can develop your own SNMP management software application.</span></span> <span data-ttu-id="9ab30-119">Les API suivantes sont disponibles à cet effet :</span><span class="sxs-lookup"><span data-stu-id="9ab30-119">The following APIs are available for this purpose:</span></span>

-   <span data-ttu-id="9ab30-120">API de gestion SNMP, un ensemble de fonctions qui peuvent être utilisées pour développer rapidement des systèmes de gestion SNMP de base</span><span class="sxs-lookup"><span data-stu-id="9ab30-120">SNMP Management API, a set of functions that can be used to quickly develop basic SNMP management systems</span></span>
-   <span data-ttu-id="9ab30-121">API WinSNMP, version 2,0, un ensemble de fonctions pour l’encodage, le décodage, l’envoi et la réception de messages SNMP</span><span class="sxs-lookup"><span data-stu-id="9ab30-121">WinSNMP API, version 2.0, a set of functions for encoding, decoding, sending, and receiving SNMP messages</span></span>

<span data-ttu-id="9ab30-122">En outre, l’API de l’agent d’extension SNMP définit l’interface entre le service SNMP et les dll d’agent d’extension SNMP tierces.</span><span class="sxs-lookup"><span data-stu-id="9ab30-122">Additionally, the SNMP Extension Agent API defines the interface between the SNMP service and third-party SNMP extension agent DLLs.</span></span> <span data-ttu-id="9ab30-123">Les fonctions de l’API de l’utilitaire SNMP peuvent être utilisées pour simplifier le traitement des messages SNMP.</span><span class="sxs-lookup"><span data-stu-id="9ab30-123">The SNMP Utility API functions can be used to simplify the processing of SNMP messages.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9ab30-124">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="9ab30-124">Developer audience</span></span>

<span data-ttu-id="9ab30-125">Les API répertoriées dans la section précédente sont conçues pour être utilisées par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="9ab30-125">The APIs listed in the preceding section are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="9ab30-126">Vous devez vous familiariser avec SNMP et SNMPv2C, ainsi que pour connaître les concepts de gestion de réseau et de réseau.</span><span class="sxs-lookup"><span data-stu-id="9ab30-126">Familiarity with SNMP and SNMPv2C, as well as a working knowledge of networking and network management concepts, are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9ab30-127">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="9ab30-127">Run-time requirements</span></span>

<span data-ttu-id="9ab30-128">Pour plus d’informations sur le système d’exploitation requis pour utiliser une fonction particulière, consultez la section Configuration requise de la page de référence pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="9ab30-128">For more information about the operating system required to use a particular function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9ab30-129">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="9ab30-129">In this section</span></span>



| <span data-ttu-id="9ab30-130">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9ab30-130">Topic</span></span>                                                                                                | <span data-ttu-id="9ab30-131">Description</span><span class="sxs-lookup"><span data-stu-id="9ab30-131">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ab30-132">Nouveautés dans SNMP</span><span class="sxs-lookup"><span data-stu-id="9ab30-132">New in SNMP</span></span>](new-in-snmp.md)<br/>                                                            | <span data-ttu-id="9ab30-133">Informations sur les mises à jour de SNMP.</span><span class="sxs-lookup"><span data-stu-id="9ab30-133">Information on updates to SNMP.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="9ab30-134">Simple Network Management Protocol (SNMP)</span><span class="sxs-lookup"><span data-stu-id="9ab30-134">Simple Network Management Protocol (SNMP)</span></span>](simple-network-management-protocol-snmp-.md)<br/> | <span data-ttu-id="9ab30-135">Informations et informations de référence sur l’API pour SNMP, y compris l’API de gestion SNMP, l’API de l’agent d’extension SNMP et les fonctions de l’API de l’utilitaire SNMP.</span><span class="sxs-lookup"><span data-stu-id="9ab30-135">Information and API reference for SNMP, including the SNMP Management API, SNMP Extension Agent API, and SNMP Utility API functions.</span></span><br/> |
| [<span data-ttu-id="9ab30-136">API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="9ab30-136">WinSNMP API</span></span>](snmp-reference.md)<br/>                                                         | <span data-ttu-id="9ab30-137">Informations et informations de référence sur l’API pour l’interface de programmation d’applications SNMP Microsoft Windows (API WinSNMP).</span><span class="sxs-lookup"><span data-stu-id="9ab30-137">Information and API reference for the Microsoft Windows SNMP Application Programming Interface (WinSNMP API).</span></span> <br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="9ab30-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ab30-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ab30-139">Protocole DHCP (Dynamic Host Configuration Protocol)</span><span class="sxs-lookup"><span data-stu-id="9ab30-139">Dynamic Host Configuration Protocol (DHCP)</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="9ab30-140">Gestion du réseau</span><span class="sxs-lookup"><span data-stu-id="9ab30-140">Network Management</span></span>](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[<span data-ttu-id="9ab30-141">Service de routage et d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="9ab30-141">Routing and Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

