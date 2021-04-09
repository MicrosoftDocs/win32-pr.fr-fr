---
title: Gestion des interruptions et des notifications
description: L’application WinSNMP doit s’inscrire pour recevoir des interruptions et des notifications en appelant la fonction SnmpRegister avec SNMPAPI \_ sur. L’application peut annuler l’inscription et désactiver les interruptions et les notifications en appelant la fonction avec SNMPAPI \_ off.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840517"
---
# <a name="managing-traps-and-notifications"></a><span data-ttu-id="cae53-104">Gestion des interruptions et des notifications</span><span class="sxs-lookup"><span data-stu-id="cae53-104">Managing Traps and Notifications</span></span>

<span data-ttu-id="cae53-105">L’application WinSNMP doit s’inscrire pour recevoir des interruptions et des notifications en appelant la fonction [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) avec SNMPAPI \_ sur.</span><span class="sxs-lookup"><span data-stu-id="cae53-105">The WinSNMP application must register to receive traps and notifications by calling the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) function with SNMPAPI\_ON.</span></span> <span data-ttu-id="cae53-106">L’application peut annuler l’inscription et désactiver les interruptions et les notifications en appelant la fonction avec SNMPAPI \_ off.</span><span class="sxs-lookup"><span data-stu-id="cae53-106">The application can unregister and disable traps and notifications by calling the function with SNMPAPI\_OFF.</span></span>

<span data-ttu-id="cae53-107">Plusieurs options sont disponibles lorsque l’application appelle **SnmpRegister**.</span><span class="sxs-lookup"><span data-stu-id="cae53-107">Several options are available when the application calls **SnmpRegister**.</span></span> <span data-ttu-id="cae53-108">L’application peut s’inscrire ou se désinscrire pour les notifications et les interruptions suivantes :</span><span class="sxs-lookup"><span data-stu-id="cae53-108">The application can register or unregister for the following traps and notifications:</span></span>

-   <span data-ttu-id="cae53-109">Un type d’interruption ou de notification</span><span class="sxs-lookup"><span data-stu-id="cae53-109">One type of trap or notification</span></span>
-   <span data-ttu-id="cae53-110">Toutes les interruptions et notifications</span><span class="sxs-lookup"><span data-stu-id="cae53-110">All traps and notifications</span></span>
-   <span data-ttu-id="cae53-111">Toutes les sources de demandes d’interruption et de notification</span><span class="sxs-lookup"><span data-stu-id="cae53-111">All sources of trap and notification requests</span></span>
-   <span data-ttu-id="cae53-112">Interruptions et notifications de toutes les entités de gestion</span><span class="sxs-lookup"><span data-stu-id="cae53-112">Traps and notifications from all management entities</span></span>
-   <span data-ttu-id="cae53-113">Interruptions et notifications pour chaque contexte</span><span class="sxs-lookup"><span data-stu-id="cae53-113">Traps and notifications for every context</span></span>

<span data-ttu-id="cae53-114">Pour inscrire et recevoir un type de notification ou d’interruption prédéfini, l’application doit définir un identificateur d’objet (structure [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ) pour chaque type prédéfini.</span><span class="sxs-lookup"><span data-stu-id="cae53-114">To register and receive a predefined trap or notification type, the application must define an object identifier (an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure) for each predefined type.</span></span> <span data-ttu-id="cae53-115">La structure doit contenir une séquence de critères spéciaux pour le type d’interruption ou de notification.</span><span class="sxs-lookup"><span data-stu-id="cae53-115">The structure must contain a pattern-matching sequence for the type of trap or notification.</span></span> <span data-ttu-id="cae53-116">RFC 1907, « base d’informations de gestion pour la version 2 du protocole simple Network Management Protocol (SNMPv2) », définit les identificateurs d’objet de notification et d’interruption.</span><span class="sxs-lookup"><span data-stu-id="cae53-116">RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)," defines trap and notification object identifiers.</span></span>

<span data-ttu-id="cae53-117">Pour récupérer des données d’interruption et des notifications en attente pour une session WinSNMP, une application WinSNMP doit appeler la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) avec le descripteur de session retourné par la fonction [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="cae53-117">To retrieve outstanding trap data and notifications for a WinSNMP session, a WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function with the session handle returned by the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span>

<span data-ttu-id="cae53-118">Pour plus d’informations, consultez [envoi de messages SNMP](sending-snmp-messages.md) et [réception de messages SNMP](receiving-snmp-messages.md).</span><span class="sxs-lookup"><span data-stu-id="cae53-118">For more information, see [Sending SNMP Messages](sending-snmp-messages.md) and [Receiving SNMP Messages](receiving-snmp-messages.md).</span></span> <span data-ttu-id="cae53-119">Pour plus d’informations sur l’allocation et la désallocation des ressources pour les interruptions et les notifications, consultez [allocation d’objets mémoire WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="cae53-119">For additional information about allocation and deallocation of resources for traps and notifications, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




