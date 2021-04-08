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
# <a name="about-traps-and-notifications"></a>À propos des interruptions et des notifications

Un type de message qu’une application d’agent SNMP peut envoyer à une application WinSNMP est un message asynchrone qui informe l’application d’un événement important. Par exemple, un événement important se produit lorsqu’une liaison réseau s’arrête ou lorsqu’un échec d’authentification se produit.

Ces types de messages sont appelés des interruptions sous SNMPv1 et des notifications sous SNMPv2C. L’implémentation de l’WinSNMP de Microsoft traduit toujours les pièges SNMPv1 au format SNMPv2C, comme défini par RFC 1908.

Lorsque vous appelez la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) pour créer un PDU d’interruption, vous pouvez créer uniquement un PDU d’interruption SNMPv2c. Le seul type d’PDU d’interruption que vous pouvez mettre à jour avec un appel à la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) est un PDU d’interruption SNMPv2c.

Pour plus d'informations, consultez les rubriques ci-dessous.



| Rubrique                                                                                    | Description |
|------------------------------------------------------------------------------------------|-------------|
| [Conversion d’interruptions de SNMPv1 en SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [Formats d’interruption](trap-formats.md)                                                         |             |



 

 

 




