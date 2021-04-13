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
# <a name="sending-snmp-messages"></a>Envoi de messages SNMP

Une application WinSNMP initie une demande de transmission en envoyant un message SNMP. Les messages SNMP incluent une unité de données de protocole SNMP. Pour plus d’informations, consultez [utilisation des unités de données de protocole](working-with-protocol-data-units.md).

Une application WinSNMP doit appeler la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) pour demander que l’implémentation de l’WinSNMP Microsoft transmette l’PDU, avec les autres éléments de message requis définis par la RFC appropriée. En plus de l’entité de destination, l’application doit spécifier l’entité source et un contexte pour la demande. La fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) s’exécute de façon asynchrone.

L’application WinSNMP doit appeler la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour récupérer la réponse à une demande **SnmpSendMsg** .

L’implémentation vérifie la validité de l’PDU et les autres éléments de message lorsqu’une application appelle [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).

 

 




