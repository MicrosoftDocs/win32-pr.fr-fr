---
title: Envoi de messages SNMP
description: Une application WinSNMP initie une demande de transmission en envoyant un message SNMP. Les messages SNMP incluent une unité de données de protocole SNMP. Pour plus d’informations, consultez Utilisation des unités de données de protocole.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310714"
---
# <a name="sending-snmp-messages"></a><span data-ttu-id="a8738-105">Envoi de messages SNMP</span><span class="sxs-lookup"><span data-stu-id="a8738-105">Sending SNMP Messages</span></span>

<span data-ttu-id="a8738-106">Une application WinSNMP initie une demande de transmission en envoyant un message SNMP.</span><span class="sxs-lookup"><span data-stu-id="a8738-106">A WinSNMP application initiates a transmission request by sending an SNMP message.</span></span> <span data-ttu-id="a8738-107">Les messages SNMP incluent une unité de données de protocole SNMP.</span><span class="sxs-lookup"><span data-stu-id="a8738-107">SNMP messages include an SNMP protocol data unit.</span></span> <span data-ttu-id="a8738-108">Pour plus d’informations, consultez [utilisation des unités de données de protocole](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="a8738-108">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

<span data-ttu-id="a8738-109">Une application WinSNMP doit appeler la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) pour demander que l’implémentation de l’WinSNMP Microsoft transmette l’PDU, avec les autres éléments de message requis définis par la RFC appropriée.</span><span class="sxs-lookup"><span data-stu-id="a8738-109">A WinSNMP application must call the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit the PDU, with the other required message elements defined by the relevant RFC.</span></span> <span data-ttu-id="a8738-110">En plus de l’entité de destination, l’application doit spécifier l’entité source et un contexte pour la demande.</span><span class="sxs-lookup"><span data-stu-id="a8738-110">In addition to the destination entity, the application must specify the source entity and a context for the request.</span></span> <span data-ttu-id="a8738-111">La fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) s’exécute de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a8738-111">The [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function executes asynchronously.</span></span>

<span data-ttu-id="a8738-112">L’application WinSNMP doit appeler la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour récupérer la réponse à une demande **SnmpSendMsg** .</span><span class="sxs-lookup"><span data-stu-id="a8738-112">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an **SnmpSendMsg** request.</span></span>

<span data-ttu-id="a8738-113">L’implémentation vérifie la validité de l’PDU et les autres éléments de message lorsqu’une application appelle [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span><span class="sxs-lookup"><span data-stu-id="a8738-113">The implementation verifies the validity of the PDU and the other message elements when an application calls [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span>

 

 




