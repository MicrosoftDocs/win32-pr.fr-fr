---
title: Envoi de messages SNMP
description: Une application WinSNMP initie une demande de transmission en envoyant un message SNMP. Les messages SNMP incluent une unité de données de protocole SNMP. Pour plus d’informations, consultez Utilisation des unités de données de protocole.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4461c5d554444b2a7a5384a0ca79825b27ebe3c3bc489b6152c81ae71d172f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009067"
---
# <a name="sending-snmp-messages"></a>Envoi de messages SNMP

Une application WinSNMP initie une demande de transmission en envoyant un message SNMP. Les messages SNMP incluent une unité de données de protocole SNMP. Pour plus d’informations, consultez [utilisation des unités de données de protocole](working-with-protocol-data-units.md).

Une application WinSNMP doit appeler la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) pour demander que l’implémentation de l’WinSNMP Microsoft transmette l’PDU, avec les autres éléments de message requis définis par la RFC appropriée. En plus de l’entité de destination, l’application doit spécifier l’entité source et un contexte pour la demande. La fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) s’exécute de façon asynchrone.

L’application WinSNMP doit appeler la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour récupérer la réponse à une demande **SnmpSendMsg** .

L’implémentation vérifie la validité de l’PDU et les autres éléments de message lorsqu’une application appelle [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).

 

 




