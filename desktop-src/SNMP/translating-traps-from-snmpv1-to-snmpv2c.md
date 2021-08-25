---
title: Conversion d’interruptions de SNMPv1 en SNMPv2C
description: Lorsque l’implémentation de Microsoft WinSNMP reçoit des interruptions d’une entité opérant sous l’infrastructure SNMPv1, elle traduit les interruptions au format SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f70ddbdfb779f6b06f8ed26490c6fabd2421ae96f0006b4af5b7f1ab18f7d5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885859"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a>Conversion d’interruptions de SNMPv1 en SNMPv2C

Lorsque l’implémentation de Microsoft WinSNMP reçoit des interruptions d’une entité opérant sous l’infrastructure SNMPv1, elle traduit les interruptions au format SNMPv2C. Par conséquent, quand [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) remet un piège, il est toujours au format SNMPv2c. La norme RFC 1908, « coexistence entre la version 1 et la version 2 de l’infrastructure de gestion de réseau Internet standard », spécifie les règles de conversion de SNMPv1 au format d’interruption SNMPv2C.

Une application WinSNMP peut vérifier la dernière entrée de liaison de variable dans une liste de liaisons de variables pour déterminer si l’entrée est une interruption convertie de la structure SNMPv1 au format SNMPv2C. Si c’est le cas, la dernière liaison de variable sera toujours égale à la valeur « snmpTrapEnterpriseOID. 0 ».

Pour plus d’informations, consultez [gestion des interruptions et des notifications](managing-traps-and-notifications.md).

 

 




