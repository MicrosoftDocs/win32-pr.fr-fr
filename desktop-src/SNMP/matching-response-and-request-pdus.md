---
title: Réponse correspondante et demandes d’alimentation (PDU)
description: L’ordre dans lequel l’application WinSNMP reçoit des réponses SNMP peut ne pas correspondre à l’ordre dans lequel l’application envoie les demandes d’opération SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e669b3e15652b8df68cb8fc27437106e644909e99bf0b7aee21a128194cf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009317"
---
# <a name="matching-response-and-request-pdus"></a>Réponse correspondante et demandes d’alimentation (PDU)

L’ordre dans lequel l’application WinSNMP reçoit des réponses SNMP peut ne pas correspondre à l’ordre dans lequel l’application envoie les demandes d’opération SNMP. Pour correspondre à la réponse à la demande, l’application doit utiliser le champ d’identificateur de demande **( \_ ID de demande**) de la réponse.

Le **champ \_ ID** de la demande est une valeur numérique unique qui identifie la PDU. Les applications peuvent assigner des identificateurs de demande en appelant la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) . Appelez la fonction [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) pour récupérer l’ID de **demande \_** d’une PDU.

 

 




