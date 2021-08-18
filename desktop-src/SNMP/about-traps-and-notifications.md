---
title: À propos des interruptions et des notifications
description: Un type de message qu’une application d’agent SNMP peut envoyer à une application WinSNMP est un message asynchrone qui informe l’application d’un événement important.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60739041237dad462e516e43c71d552446357f3ddc188d6609de2eef508b9658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009807"
---
# <a name="about-traps-and-notifications"></a>À propos des interruptions et des notifications

Un type de message qu’une application d’agent SNMP peut envoyer à une application WinSNMP est un message asynchrone qui informe l’application d’un événement important. Par exemple, un événement important se produit lorsqu’une liaison réseau s’arrête ou lorsqu’un échec d’authentification se produit.

Ces types de messages sont appelés des interruptions sous SNMPv1 et des notifications sous SNMPv2C. L’implémentation de l’WinSNMP de Microsoft traduit toujours les pièges SNMPv1 au format SNMPv2C, comme défini par RFC 1908.

Lorsque vous appelez la fonction [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) pour créer un PDU d’interruption, vous pouvez créer uniquement un PDU d’interruption SNMPv2c. Le seul type d’PDU d’interruption que vous pouvez mettre à jour avec un appel à la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) est un PDU d’interruption SNMPv2c.

Pour plus d’informations, voir les rubriques suivantes :



| Rubrique                                                                                    | Description |
|------------------------------------------------------------------------------------------|-------------|
| [Conversion d’interruptions de SNMPv1 en SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [Formats d’interruption](trap-formats.md)                                                         |             |



 

 

 




