---
title: Inscription d’une application d’agent SNMP
description: Outre les opérations du gestionnaire SNMP, la version 2,0 de l’API WinSNMP prend également en charge les opérations de l’agent SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940139"
---
# <a name="registering-an-snmp-agent-application"></a><span data-ttu-id="be7d7-103">Inscription d’une application d’agent SNMP</span><span class="sxs-lookup"><span data-stu-id="be7d7-103">Registering an SNMP Agent Application</span></span>

<span data-ttu-id="be7d7-104">Outre les opérations du gestionnaire SNMP, la version 2,0 de l’API WinSNMP prend également en charge les opérations de l’agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="be7d7-104">In addition to SNMP manager operations, the WinSNMP API version 2.0 also supports SNMP agent operations.</span></span>

<span data-ttu-id="be7d7-105">Pour inscrire une application WinSNMP en tant qu’agent SNMP, l’application peut appeler la fonction [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) .</span><span class="sxs-lookup"><span data-stu-id="be7d7-105">To register a WinSNMP application as an SNMP agent, the application can call the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function.</span></span> <span data-ttu-id="be7d7-106">Cette fonction indique à l’implémentation de Microsoft WinSNMP qu’une entité SNMP agira dans le rôle d’un agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="be7d7-106">This function informs the Microsoft WinSNMP implementation that an SNMP entity will be acting in the role of an SNMP agent.</span></span> <span data-ttu-id="be7d7-107">L’application peut également appeler **SnmpListen** pour informer l’implémentation lorsqu’elle ne fera plus Office d’agent.</span><span class="sxs-lookup"><span data-stu-id="be7d7-107">The application can also call **SnmpListen** to inform the implementation when it will no longer be acting as an agent.</span></span>

<span data-ttu-id="be7d7-108">Si une application appelle la fonction [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) et passe la valeur SNMPAPI \_ dans le paramètre *lStatus* , les actions suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="be7d7-108">If an application calls the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function and passes the value SNMPAPI\_ON in the *lStatus* parameter, the following actions occur:</span></span>

1.  <span data-ttu-id="be7d7-109">L’entité qui fonctionnera dans un rôle d’agent SNMP est liée à son port attribué et « écoute » les demandes de message SNMP entrantes.</span><span class="sxs-lookup"><span data-stu-id="be7d7-109">The entity that will be functioning in an SNMP agent role binds to its assigned port, and "listens" for incoming SNMP message requests.</span></span>
2.  <span data-ttu-id="be7d7-110">L’agent utilise une logique spécifique à l’application pour traiter chaque requête SNMP.</span><span class="sxs-lookup"><span data-stu-id="be7d7-110">The agent uses application-specific logic to process each SNMP request.</span></span>
3.  <span data-ttu-id="be7d7-111">L’agent forme les réponses appropriées à chaque requête.</span><span class="sxs-lookup"><span data-stu-id="be7d7-111">The agent forms appropriate responses to each request.</span></span>
4.  <span data-ttu-id="be7d7-112">L’agent transmet la réponse à l’entité à l’origine de la demande en appelant la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="be7d7-112">The agent transmits the response to the requesting entity by calling the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span> <span data-ttu-id="be7d7-113">Lorsque l’agent appelle **SnmpSendMsg**, il spécifie l’adresse de l’agent dans le paramètre *srcEntity* , ainsi que l’adresse de l’entité Remote Manager dans le paramètre *dstEntity* .</span><span class="sxs-lookup"><span data-stu-id="be7d7-113">When the agent calls **SnmpSendMsg**, it specifies the address of the agent in the *srcEntity* parameter, and the address of the remote manager entity in the *dstEntity* parameter.</span></span> <span data-ttu-id="be7d7-114">(Ces valeurs sont l’inverse des valeurs que l’entité agent a reçues dans ces paramètres lorsqu’elle a appelé la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour récupérer une demande SNMP.)</span><span class="sxs-lookup"><span data-stu-id="be7d7-114">(These values are the reverse of the values the agent entity received in these parameters when it called the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve an SNMP request.)</span></span>

<span data-ttu-id="be7d7-115">Pour plus d’informations sur les applications de gestion SNMP et les applications de l’agent, consultez [à propos de SNMP](about-snmp.md).</span><span class="sxs-lookup"><span data-stu-id="be7d7-115">For more information about SNMP management applications and agent applications, see [About SNMP](about-snmp.md).</span></span>

 

 




