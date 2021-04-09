---
title: Erreurs de transport réseau
description: L’implémentation de Microsoft WinSNMP peut détecter une erreur de transport réseau après avoir transmis un message SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842606"
---
# <a name="network-transport-errors"></a><span data-ttu-id="62d8b-103">Erreurs de transport réseau</span><span class="sxs-lookup"><span data-stu-id="62d8b-103">Network Transport Errors</span></span>

<span data-ttu-id="62d8b-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="62d8b-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="62d8b-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="62d8b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="62d8b-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="62d8b-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="62d8b-107">L’implémentation de Microsoft WinSNMP peut détecter une erreur de transport réseau après avoir transmis un message SNMP.</span><span class="sxs-lookup"><span data-stu-id="62d8b-107">The Microsoft WinSNMP implementation can detect a network transport error after it transmits an SNMP message.</span></span> <span data-ttu-id="62d8b-108">Dans ce cas, l’implémentation envoie une notification de réception de données à la session WinSNMP qui a initié la demande de communication.</span><span class="sxs-lookup"><span data-stu-id="62d8b-108">When this occurs, the implementation sends a data receipt notification to the WinSNMP session that initiated the communication request.</span></span> <span data-ttu-id="62d8b-109">L’implémentation retourne également l' \_ échec SNMPAPI lors de l’appel suivant à la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour la session.</span><span class="sxs-lookup"><span data-stu-id="62d8b-109">The implementation also returns SNMPAPI\_FAILURE on the next call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function for the session.</span></span> <span data-ttu-id="62d8b-110">La fonction **SnmpRecvMsg** échoue avec un code d’erreur étendu qui indique une erreur de couche de transport réseau.</span><span class="sxs-lookup"><span data-stu-id="62d8b-110">The **SnmpRecvMsg** function fails with an extended error code that indicates a network transport layer error.</span></span>

<span data-ttu-id="62d8b-111">Pour obtenir la liste des erreurs spécifiques de la couche de transport, consultez les pages de référence pour les fonctions [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)et [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="62d8b-111">For a list of specific transport layer errors, see the reference pages for the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg), and [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) functions.</span></span>

 

 