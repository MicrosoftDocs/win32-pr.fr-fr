---
title: Traduction des demandes de message
description: Cette rubrique décrit le processus de traduction des demandes SNMPv1 en demandes SNMPv2.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2a67ecb78b16f818ea50158faf827e19d4eba5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507110"
---
# <a name="translating-message-requests"></a><span data-ttu-id="d53e8-103">Traduction des demandes de message</span><span class="sxs-lookup"><span data-stu-id="d53e8-103">Translating Message Requests</span></span>

<span data-ttu-id="d53e8-104">Cette rubrique décrit le processus de traduction des demandes SNMPv1 en demandes SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="d53e8-104">This topic describes the process of translating SNMPv1 requests into SNMPv2 requests.</span></span>

<span data-ttu-id="d53e8-105">Si une application WinSNMP demande une fonctionnalité qui est disponible sous la version de SNMP version 2C Framework (SNMPv2C), mais que l’entité cible prend uniquement en charge SNMP version 1 Framework (SNMPv1), l’implémentation Microsoft WinSNMP tente de convertir la demande au format SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="d53e8-105">If a WinSNMP application requests functionality that is available under the SNMP version 2C framework (SNMPv2C), but the target entity supports only the SNMP version 1 framework (SNMPv1), the Microsoft WinSNMP implementation attempts to translate the request to the SNMPv1 format.</span></span> <span data-ttu-id="d53e8-106">Pour ce faire, l’implémentation utilise les procédures définies dans le document RFC 1908, « coexistence entre la version 1 et la version 2 de l’infrastructure de gestion de réseau Internet-Standard ».</span><span class="sxs-lookup"><span data-stu-id="d53e8-106">To do this, the implementation uses the procedures defined in RFC 1908, "Coexistence Between Version 1 and Version 2 of the Internet-Standard Network Management Framework."</span></span> <span data-ttu-id="d53e8-107">Si la traduction n’est pas possible, la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) échoue avec le code d’erreur étendu SNMPAPI \_ opération \_ non valide.</span><span class="sxs-lookup"><span data-stu-id="d53e8-107">If translation is not possible, the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function fails with the extended error code SNMPAPI\_OPERATION\_INVALID.</span></span>

 

 




