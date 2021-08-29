---
title: Assignation d’identificateurs de demande
description: Une application WinSNMP peut appeler la fonction SnmpCreatePdu ou la fonction SnmpSetPduData pour affecter un identificateur de demande généré par l’application à un PDU. L’application doit passer la valeur dans le \_ paramètre ID de demande.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9914256a071d93ebebd932e6771758c4c76e2c419f8f9cf13a0323ca44ea7715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009797"
---
# <a name="assigning-request-identifiers"></a>Assignation d’identificateurs de demande

Une application WinSNMP peut appeler la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) pour affecter un identificateur de demande généré par l’application à un PDU. L’application doit passer la valeur dans le *paramètre \_ ID de demande* .

Une application peut demander que l’implémentation de l’WinSNMP Microsoft génère et assigner un identificateur de demande à un PDU en transmettant zéro dans le paramètre *\_ ID* de la demande de la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . L’application peut récupérer l’identificateur de demande affecté à l’aide d’un appel à la fonction [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) .

Pour assigner un identificateur de demande égal à une valeur spécifique, y compris zéro, l’application doit passer cette valeur dans le paramètre d' *\_ ID de demande* de la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .

Lorsque l’implémentation exécute la stratégie de retransmission de l’application, elle comprend le champ **\_ ID** de la demande du PDU d’origine dans chaque message SNMP retransmis. Pour plus d’informations, consultez [à propos de la retransmission](about-retransmission.md) et de [la gestion de la stratégie de retransmission](managing-the-retransmission-policy.md).

> [!Note]  
> Lorsque l’implémentation reçoit des interruptions d’une entité SNMPv1, elle attribue une valeur différente de zéro au **champ \_ ID** de la demande de la PDU. Cette valeur peut dupliquer un identificateur de demande utilisé par l’application dans un PDU de demande. Les applications doivent vérifier la duplication.

 

 

 




