---
title: Assignation d’identificateurs de demande
description: Une application WinSNMP peut appeler la fonction SnmpCreatePdu ou la fonction SnmpSetPduData pour affecter un identificateur de demande généré par l’application à un PDU. L’application doit passer la valeur dans le \_ paramètre ID de demande.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671078"
---
# <a name="assigning-request-identifiers"></a><span data-ttu-id="69a96-104">Assignation d’identificateurs de demande</span><span class="sxs-lookup"><span data-stu-id="69a96-104">Assigning Request Identifiers</span></span>

<span data-ttu-id="69a96-105">Une application WinSNMP peut appeler la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) pour affecter un identificateur de demande généré par l’application à un PDU.</span><span class="sxs-lookup"><span data-stu-id="69a96-105">A WinSNMP application can call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function to assign an application-generated request identifier to a PDU.</span></span> <span data-ttu-id="69a96-106">L’application doit passer la valeur dans le *paramètre \_ ID de demande* .</span><span class="sxs-lookup"><span data-stu-id="69a96-106">The application must pass the value in the *request\_id* parameter.</span></span>

<span data-ttu-id="69a96-107">Une application peut demander que l’implémentation de l’WinSNMP Microsoft génère et assigner un identificateur de demande à un PDU en transmettant zéro dans le paramètre *\_ ID* de la demande de la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) .</span><span class="sxs-lookup"><span data-stu-id="69a96-107">An application can request that the Microsoft WinSNMP implementation generate and assign a request identifier to a PDU by passing zero in the *request\_id* parameter of the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="69a96-108">L’application peut récupérer l’identificateur de demande affecté à l’aide d’un appel à la fonction [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="69a96-108">The application can retrieve the assigned request identifier with a call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function.</span></span>

<span data-ttu-id="69a96-109">Pour assigner un identificateur de demande égal à une valeur spécifique, y compris zéro, l’application doit passer cette valeur dans le paramètre d' *\_ ID de demande* de la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="69a96-109">To assign a request identifier equal to a specific value, including zero, the application must pass that value in the *request\_id* parameter of the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span>

<span data-ttu-id="69a96-110">Lorsque l’implémentation exécute la stratégie de retransmission de l’application, elle comprend le champ **\_ ID** de la demande du PDU d’origine dans chaque message SNMP retransmis.</span><span class="sxs-lookup"><span data-stu-id="69a96-110">When the implementation executes the application's retransmission policy, it includes the **request\_id** field of the original PDU in each retransmitted SNMP message.</span></span> <span data-ttu-id="69a96-111">Pour plus d’informations, consultez [à propos de la retransmission](about-retransmission.md) et de [la gestion de la stratégie de retransmission](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="69a96-111">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

> [!Note]  
> <span data-ttu-id="69a96-112">Lorsque l’implémentation reçoit des interruptions d’une entité SNMPv1, elle attribue une valeur différente de zéro au **champ \_ ID** de la demande de la PDU.</span><span class="sxs-lookup"><span data-stu-id="69a96-112">When the implementation receives traps from an SNMPv1 entity, it assigns a non-zero value to the **request\_id** field of the PDU.</span></span> <span data-ttu-id="69a96-113">Cette valeur peut dupliquer un identificateur de demande utilisé par l’application dans un PDU de demande.</span><span class="sxs-lookup"><span data-stu-id="69a96-113">This value may duplicate a request identifier used by the application in a request PDU.</span></span> <span data-ttu-id="69a96-114">Les applications doivent vérifier la duplication.</span><span class="sxs-lookup"><span data-stu-id="69a96-114">Applications must check for duplication.</span></span>

 

 

 




