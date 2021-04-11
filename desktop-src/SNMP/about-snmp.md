---
title: À propos de SNMP
description: SNMP utilise une architecture distribuée composée de gestionnaires et d’agents.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031684"
---
# <a name="about-snmp"></a><span data-ttu-id="c8a2d-104">À propos de SNMP</span><span class="sxs-lookup"><span data-stu-id="c8a2d-104">About SNMP</span></span>

<span data-ttu-id="c8a2d-105">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c8a2d-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c8a2d-107">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="c8a2d-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="c8a2d-108">SNMP utilise une architecture distribuée composée de gestionnaires et d’agents.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-108">SNMP uses a distributed architecture consisting of managers and agents.</span></span> <span data-ttu-id="c8a2d-109">Un agent est une application SNMP qui répond aux requêtes des applications du gestionnaire SNMP.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-109">An agent is an SNMP application that responds to queries from SNMP manager applications.</span></span> <span data-ttu-id="c8a2d-110">L’agent SNMP est chargé de récupérer et de mettre à jour les informations de gestion locales en fonction des demandes du gestionnaire SNMP.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-110">The SNMP agent is responsible for retrieving and updating local management information based on the requests of the SNMP manager.</span></span> <span data-ttu-id="c8a2d-111">L’agent notifie également les gestionnaires inscrits en cas d’événements ou d’interruptions importants.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-111">The agent also notifies registered managers when significant events or traps occur.</span></span> <span data-ttu-id="c8a2d-112">Un gestionnaire est une application SNMP qui génère des requêtes pour les applications de l’agent SNMP et reçoit des interruptions des applications de l’agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-112">A manager is an SNMP application that generates queries to SNMP agent applications and receives traps from SNMP agent applications.</span></span>

<span data-ttu-id="c8a2d-113">Sur les ordinateurs exécutant Microsoft Windows XP/Windows 2000/Windows NT, l’agent SNMP est implémenté par le service SNMP (SNMP.EXE).</span><span class="sxs-lookup"><span data-stu-id="c8a2d-113">On computers running Microsoft Windows XP/Windows 2000/Windows NT, the SNMP agent is implemented by the SNMP service (SNMP.EXE).</span></span> <span data-ttu-id="c8a2d-114">Le gestionnaire SNMP est généralement une application de console de gestion SNMP tierce.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-114">The SNMP manager is typically a third-party SNMP management console application.</span></span> <span data-ttu-id="c8a2d-115">L’application console de gestion n’a pas besoin de s’exécuter sur le même hôte que l’agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-115">The management console application does not need to run on the same host as the SNMP agent.</span></span> <span data-ttu-id="c8a2d-116">Pour utiliser les informations fournies par le service SNMP de Microsoft, vous avez besoin d’au moins une application de console de gestion SNMP.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-116">To use the information the Microsoft SNMP service provides, you need at least one SNMP management console application.</span></span> <span data-ttu-id="c8a2d-117">Le système inclut des bibliothèques qui prennent en charge les applications de console de gestion SNMP, mais il n’inclut pas d’application de console de gestion SNMP pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="c8a2d-117">The system includes libraries that support SNMP management console applications, but it does not include an SNMP management console application at this time.</span></span>

 

 