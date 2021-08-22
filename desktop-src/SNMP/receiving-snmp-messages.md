---
title: Réception des messages SNMP
description: L’application WinSNMP doit appeler la fonction SnmpRecvMsg pour récupérer la réponse à une demande SnmpSendMsg.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd341e71aa6b8387b82f6576599fb6cb7d3545f34e01f80267f19a73edb7cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009177"
---
# <a name="receiving-snmp-messages"></a>Réception des messages SNMP

L’application WinSNMP doit appeler la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour récupérer la réponse à une demande [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .

La fonction [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) transmet un handle de fenêtre d’application et un identificateur de message de notification à l’implémentation de Microsoft winsnmp. Lorsque la fenêtre d’application reçoit ce message, elle indique à l’application d’appeler la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) à l’aide du handle de session retourné par [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).

La fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) retourne deux descripteurs d’entité, un descripteur de contexte et le descripteur d’une PDU. Il est recommandé que l’application WinSNMP libère ces ressources à l’aide des fonctions [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)et [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .

Pour plus d’informations sur la gestion de la durée entre un appel à la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) et la réception de la réponse correspondante, consultez [à propos de la retransmission](about-retransmission.md). Pour plus d’informations sur l’utilisation du champ PDU **\_ ID** de la demande pour correspondre à un PDU de réponse avec son PDU de demande, consultez correspondance de la [réponse et des PDU de demande](matching-response-and-request-pdus.md).

 

 




