---
title: Gestion des interruptions et des notifications
description: L’application WinSNMP doit s’inscrire pour recevoir des interruptions et des notifications en appelant la fonction SnmpRegister avec SNMPAPI \_ sur. L’application peut annuler l’inscription et désactiver les interruptions et les notifications en appelant la fonction avec SNMPAPI \_ off.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840517"
---
# <a name="managing-traps-and-notifications"></a>Gestion des interruptions et des notifications

L’application WinSNMP doit s’inscrire pour recevoir des interruptions et des notifications en appelant la fonction [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) avec SNMPAPI \_ sur. L’application peut annuler l’inscription et désactiver les interruptions et les notifications en appelant la fonction avec SNMPAPI \_ off.

Plusieurs options sont disponibles lorsque l’application appelle **SnmpRegister**. L’application peut s’inscrire ou se désinscrire pour les notifications et les interruptions suivantes :

-   Un type d’interruption ou de notification
-   Toutes les interruptions et notifications
-   Toutes les sources de demandes d’interruption et de notification
-   Interruptions et notifications de toutes les entités de gestion
-   Interruptions et notifications pour chaque contexte

Pour inscrire et recevoir un type de notification ou d’interruption prédéfini, l’application doit définir un identificateur d’objet (structure [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ) pour chaque type prédéfini. La structure doit contenir une séquence de critères spéciaux pour le type d’interruption ou de notification. RFC 1907, « base d’informations de gestion pour la version 2 du protocole simple Network Management Protocol (SNMPv2) », définit les identificateurs d’objet de notification et d’interruption.

Pour récupérer des données d’interruption et des notifications en attente pour une session WinSNMP, une application WinSNMP doit appeler la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) avec le descripteur de session retourné par la fonction [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .

Pour plus d’informations, consultez [envoi de messages SNMP](sending-snmp-messages.md) et [réception de messages SNMP](receiving-snmp-messages.md). Pour plus d’informations sur l’allocation et la désallocation des ressources pour les interruptions et les notifications, consultez [allocation d’objets mémoire WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




