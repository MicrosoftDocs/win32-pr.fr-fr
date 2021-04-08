---
title: Conversion d’interruptions de SNMPv1 en SNMPv2C
description: Lorsque l’implémentation de Microsoft WinSNMP reçoit des interruptions d’une entité opérant sous l’infrastructure SNMPv1, elle traduit les interruptions au format SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d36870bda9b434bcc19f42332f2751020689591
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839630"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a><span data-ttu-id="40758-103">Conversion d’interruptions de SNMPv1 en SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="40758-103">Translating Traps from SNMPv1 to SNMPv2C</span></span>

<span data-ttu-id="40758-104">Lorsque l’implémentation de Microsoft WinSNMP reçoit des interruptions d’une entité opérant sous l’infrastructure SNMPv1, elle traduit les interruptions au format SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="40758-104">When the Microsoft WinSNMP implementation receives traps from an entity operating under the SNMPv1 framework, it translates the traps to the SNMPv2C format.</span></span> <span data-ttu-id="40758-105">Par conséquent, quand [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) remet un piège, il est toujours au format SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="40758-105">Therefore, when [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) delivers a trap it is always in the SNMPv2C format.</span></span> <span data-ttu-id="40758-106">La norme RFC 1908, « coexistence entre la version 1 et la version 2 de l’infrastructure de gestion de réseau Internet standard », spécifie les règles de conversion de SNMPv1 au format d’interruption SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="40758-106">RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework," specifies the rules for translating from the SNMPv1 to the SNMPv2C trap format.</span></span>

<span data-ttu-id="40758-107">Une application WinSNMP peut vérifier la dernière entrée de liaison de variable dans une liste de liaisons de variables pour déterminer si l’entrée est une interruption convertie de la structure SNMPv1 au format SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="40758-107">A WinSNMP application can check the last variable binding entry in a variable binding list to determine if the entry is a trap translated from the SNMPv1 to the SNMPv2C format.</span></span> <span data-ttu-id="40758-108">Si c’est le cas, la dernière liaison de variable sera toujours égale à la valeur « snmpTrapEnterpriseOID. 0 ».</span><span class="sxs-lookup"><span data-stu-id="40758-108">If so, the last variable binding will always be equal to the value "snmpTrapEnterpriseOID.0".</span></span>

<span data-ttu-id="40758-109">Pour plus d’informations, consultez [gestion des interruptions et des notifications](managing-traps-and-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="40758-109">For more information, see [Managing Traps and Notifications](managing-traps-and-notifications.md).</span></span>

 

 




