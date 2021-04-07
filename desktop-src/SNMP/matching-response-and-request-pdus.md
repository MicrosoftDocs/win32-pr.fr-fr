---
title: Réponse correspondante et demandes d’alimentation (PDU)
description: L’ordre dans lequel l’application WinSNMP reçoit des réponses SNMP peut ne pas correspondre à l’ordre dans lequel l’application envoie les demandes d’opération SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940141"
---
# <a name="matching-response-and-request-pdus"></a>Réponse correspondante et demandes d’alimentation (PDU)

L’ordre dans lequel l’application WinSNMP reçoit des réponses SNMP peut ne pas correspondre à l’ordre dans lequel l’application envoie les demandes d’opération SNMP. Pour correspondre à la réponse à la demande, l’application doit utiliser le champ d’identificateur de demande **( \_ ID de demande**) de la réponse.

Le **champ \_ ID** de la demande est une valeur numérique unique qui identifie la PDU. Les applications peuvent assigner des identificateurs de demande en appelant la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) . Appelez la fonction [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) pour récupérer l’ID de **demande \_** d’une PDU.

 

 




