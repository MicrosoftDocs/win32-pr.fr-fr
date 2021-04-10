---
title: Niveaux de prise en charge SNMP
description: L’implémentation de l’WinSNMP de Microsoft fournit la prise en charge des communications SNMP de niveau 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100636"
---
# <a name="levels-of-snmp-support"></a><span data-ttu-id="076ea-103">Niveaux de prise en charge SNMP</span><span class="sxs-lookup"><span data-stu-id="076ea-103">Levels of SNMP Support</span></span>

<span data-ttu-id="076ea-104">L’implémentation de l’WinSNMP de Microsoft fournit la prise en charge des communications SNMP de niveau 2.</span><span class="sxs-lookup"><span data-stu-id="076ea-104">The Microsoft WinSNMP implementation provides level 2 SNMP communications support.</span></span> <span data-ttu-id="076ea-105">Le niveau 2 prend en charge le protocole SNMPv2 standard de l’IETF (Internet Engineering Task Force), tel que défini dans les RFC 1902-1908.</span><span class="sxs-lookup"><span data-stu-id="076ea-105">Level 2 supports the Internet Engineering Task Force (IETF) standard SNMPv2 protocol as defined in RFCs 1902-1908.</span></span> <span data-ttu-id="076ea-106">Il prend également en charge le wrapper de message basé sur la Communauté, tel que défini dans le document RFC 1901 (SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="076ea-106">It also supports the community-based message wrapper as defined in RFC 1901 (SNMPv2C).</span></span>

<span data-ttu-id="076ea-107">La prise en charge des communications de niveau 2 comprend l’encodage et le décodage des messages, précédemment appelé prise en charge des communications de niveau 0 dans WinSNMP version 1.1 a.</span><span class="sxs-lookup"><span data-stu-id="076ea-107">Level 2 communications support includes message encoding and decoding services, previously called Level 0 communications support in WinSNMP version 1.1a.</span></span> <span data-ttu-id="076ea-108">Le niveau 2 prend également en charge toutes les opérations de protocole SNMPv1, précédemment appelées prise en charge des communications de niveau 1 dans la version 1.1 de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="076ea-108">Level 2 also supports all SNMPv1 protocol operations, previously called Level 1 communications support in WinSNMP version 1.1a.</span></span>

<span data-ttu-id="076ea-109">L’implémentation retourne le niveau maximal de communications SNMP qu’il prend en charge en réponse à un appel de l’application WinSNMP à la fonction [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) .</span><span class="sxs-lookup"><span data-stu-id="076ea-109">The implementation returns the maximum level of SNMP communications it supports in response to a call by the WinSNMP application to the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function.</span></span>

<span data-ttu-id="076ea-110">Si l’application WinSNMP utilise l’implémentation pour le codage et le décodage des messages SNMP uniquement, l’application doit effectuer les transformations requises que l’implémentation aurait effectué.</span><span class="sxs-lookup"><span data-stu-id="076ea-110">If the WinSNMP application uses the implementation for SNMP message encoding and decoding only, the application must perform required transformations that the implementation would have performed.</span></span> <span data-ttu-id="076ea-111">Cela comprend la traduction des interruptions SNMPv1 retournées par un appel à la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) , vers des interruptions SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="076ea-111">This includes translating SNMPv1 traps returned by a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function, to SNMPv2C traps.</span></span> <span data-ttu-id="076ea-112">Il comprend également la conversion des types de PDU définis par SNMPv1 vers le type de PDU approprié défini par SNMPv2C, conformément à la norme RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="076ea-112">It also includes translating PDU types defined by SNMPv1 to the relevant PDU type defined by SNMPv2C, in accordance with RFC 1908.</span></span>

 

 




