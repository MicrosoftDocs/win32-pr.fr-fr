---
title: À propos des interruptions et des notifications
description: Un type de message qu’une application d’agent SNMP peut envoyer à une application WinSNMP est un message asynchrone qui informe l’application d’un événement important.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840077"
---
# <a name="about-traps-and-notifications"></a><span data-ttu-id="9e600-103">À propos des interruptions et des notifications</span><span class="sxs-lookup"><span data-stu-id="9e600-103">About Traps and Notifications</span></span>

<span data-ttu-id="9e600-104">Un type de message qu’une application d’agent SNMP peut envoyer à une application WinSNMP est un message asynchrone qui informe l’application d’un événement important.</span><span class="sxs-lookup"><span data-stu-id="9e600-104">One type of message an SNMP agent application can send to a WinSNMP application is an asynchronous message that informs the application of a significant event.</span></span> <span data-ttu-id="9e600-105">Par exemple, un événement important se produit lorsqu’une liaison réseau s’arrête ou lorsqu’un échec d’authentification se produit.</span><span class="sxs-lookup"><span data-stu-id="9e600-105">An example of a significant event is when a network link shuts down or when an authentication failure occurs.</span></span>

<span data-ttu-id="9e600-106">Ces types de messages sont appelés des interruptions sous SNMPv1 et des notifications sous SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e600-106">These types of messages are called traps under SNMPv1 and notifications under SNMPv2C.</span></span> <span data-ttu-id="9e600-107">L’implémentation de l’WinSNMP de Microsoft traduit toujours les pièges SNMPv1 au format SNMPv2C, comme défini par RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="9e600-107">The Microsoft WinSNMP implementation always translates SNMPv1 traps to the SNMPv2C format, as defined by RFC 1908.</span></span>

<span data-ttu-id="9e600-108">Lorsque vous appelez la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) pour créer un PDU d’interruption, vous pouvez créer uniquement un PDU d’interruption SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="9e600-108">When you call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function to create a trap PDU, you can create only an SNMPv2C trap PDU.</span></span> <span data-ttu-id="9e600-109">Le seul type d’PDU d’interruption que vous pouvez mettre à jour avec un appel à la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) est un PDU d’interruption SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="9e600-109">The only type of trap PDU you can update with a call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function is an SNMPv2C trap PDU.</span></span>

<span data-ttu-id="9e600-110">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9e600-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="9e600-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9e600-111">Topic</span></span>                                                                                    | <span data-ttu-id="9e600-112">Description</span><span class="sxs-lookup"><span data-stu-id="9e600-112">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="9e600-113">Conversion d’interruptions de SNMPv1 en SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="9e600-113">Translating Traps from SNMPv1 to SNMPv2C</span></span>](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [<span data-ttu-id="9e600-114">Formats d’interruption</span><span class="sxs-lookup"><span data-stu-id="9e600-114">Trap Formats</span></span>](trap-formats.md)                                                         |             |



 

 

 




