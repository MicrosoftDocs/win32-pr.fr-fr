---
title: Création d’une PDU
description: Pour créer et initialiser un PDU, une application WinSNMP appelle la fonction SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef0598c08c27d988825b3f0db3d8172362e9e6daf2ed4dbad049e2808b01034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009597"
---
# <a name="creating-a-pdu"></a>Création d’une PDU

Pour créer et initialiser un PDU, une application WinSNMP appelle la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . L’application doit appeler **SnmpCreatePdu** avant d’appeler la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) pour demander que l’implémentation Microsoft WINSNMP transmette un PDU. L’application doit également appeler [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) avant d’appeler la fonction [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) pour demander l’encodage d’un message SNMP.

L’application doit appeler la fonction [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) pour libérer les ressources allouées par la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) pour les nouvelles PDU.

 

 




