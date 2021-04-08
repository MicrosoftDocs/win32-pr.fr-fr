---
title: Nouveautés dans SNMP
description: SNMP prend en charge l’utilisation D’ipv6 à partir de Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729781"
---
# <a name="new-in-snmp"></a><span data-ttu-id="71de3-103">Nouveautés dans SNMP</span><span class="sxs-lookup"><span data-stu-id="71de3-103">New in SNMP</span></span>

<span data-ttu-id="71de3-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="71de3-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="71de3-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="71de3-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="71de3-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="71de3-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="71de3-107">SNMP prend en charge l’utilisation D’ipv6 à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="71de3-107">SNMP supports the use of IPv6 starting with Windows Vista.</span></span> <span data-ttu-id="71de3-108">Toutefois, SNMP prend en charge IPv6 uniquement pour les réseaux qui exécutent Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="71de3-108">However, SNMP supports IPv6 only for networks running Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="71de3-109">Cela est dû au fait que SNMP requiert la mise à jour de la pile de protocole disponible dans ces systèmes d’exploitation pour sa prise en charge IPv6.</span><span class="sxs-lookup"><span data-stu-id="71de3-109">This is because SNMP requires the updated protocol stack available in these operating systems for its IPv6 support.</span></span>

<span data-ttu-id="71de3-110">À moins que votre réseau ne soit qu’un réseau Windows Server 2008, les communications IPv6 échouent, même si une pile de protocole IPv6 est installée séparément sur les ordinateurs qui exécutent des versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="71de3-110">Unless your network is solely a Windows Server 2008 network, IPv6 communications will fail, even if an IPv6 protocol stack is separately installed on those computers that run earlier versions of Windows.</span></span> <span data-ttu-id="71de3-111">Par exemple, les agents SNMP qui s’exécutent sur Windows Server 2003, Windows XP ou Windows 2000, répondent uniquement aux requêtes effectuées sur leurs adresses IPv4.</span><span class="sxs-lookup"><span data-stu-id="71de3-111">For example, SNMP agents that run on Windows Server 2003, or Windows XP, or Windows 2000, respond only to queries that are made to their IPv4 addresses.</span></span>

 

 