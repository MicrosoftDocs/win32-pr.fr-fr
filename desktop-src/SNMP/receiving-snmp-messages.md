---
title: Réception des messages SNMP
description: L’application WinSNMP doit appeler la fonction SnmpRecvMsg pour récupérer la réponse à une demande SnmpSendMsg.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529420deaf637cec8598a8e8becc87ab514b40b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674909"
---
# <a name="receiving-snmp-messages"></a><span data-ttu-id="a19a4-103">Réception des messages SNMP</span><span class="sxs-lookup"><span data-stu-id="a19a4-103">Receiving SNMP Messages</span></span>

<span data-ttu-id="a19a4-104">L’application WinSNMP doit appeler la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour récupérer la réponse à une demande [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="a19a4-104">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) request.</span></span>

<span data-ttu-id="a19a4-105">La fonction [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) transmet un handle de fenêtre d’application et un identificateur de message de notification à l’implémentation de Microsoft winsnmp.</span><span class="sxs-lookup"><span data-stu-id="a19a4-105">The [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function passes an application window handle and a notification message identifier to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="a19a4-106">Lorsque la fenêtre d’application reçoit ce message, elle indique à l’application d’appeler la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) à l’aide du handle de session retourné par [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span><span class="sxs-lookup"><span data-stu-id="a19a4-106">When the application window receives this message, it signals the application to call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function using the session handle returned by [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span>

<span data-ttu-id="a19a4-107">La fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) retourne deux descripteurs d’entité, un descripteur de contexte et le descripteur d’une PDU.</span><span class="sxs-lookup"><span data-stu-id="a19a4-107">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function returns two entity handles, a context handle, and the handle to a PDU.</span></span> <span data-ttu-id="a19a4-108">Il est recommandé que l’application WinSNMP libère ces ressources à l’aide des fonctions [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)et [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .</span><span class="sxs-lookup"><span data-stu-id="a19a4-108">It is recommended that the WinSNMP application free these resources using the [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) functions.</span></span>

<span data-ttu-id="a19a4-109">Pour plus d’informations sur la gestion de la durée entre un appel à la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) et la réception de la réponse correspondante, consultez [à propos de la retransmission](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="a19a4-109">For additional information about managing the time between a call to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function and the receipt of the corresponding response, see [About Retransmission](about-retransmission.md).</span></span> <span data-ttu-id="a19a4-110">Pour plus d’informations sur l’utilisation du champ PDU **\_ ID** de la demande pour correspondre à un PDU de réponse avec son PDU de demande, consultez correspondance de la [réponse et des PDU de demande](matching-response-and-request-pdus.md).</span><span class="sxs-lookup"><span data-stu-id="a19a4-110">For additional information about using the **request\_id** PDU field to match a response PDU with its request PDU, see [Matching Response and Request PDUs](matching-response-and-request-pdus.md).</span></span>

 

 




