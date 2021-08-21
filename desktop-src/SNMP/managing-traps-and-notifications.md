---
title: Gestion des interruptions et des notifications
description: L’application WinSNMP doit s’inscrire pour recevoir des interruptions et des notifications en appelant la fonction SnmpRegister avec SNMPAPI \_ sur. L’application peut annuler l’inscription et désactiver les interruptions et les notifications en appelant la fonction avec SNMPAPI \_ off.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402a768aa28efb6f2fdc18994d749cfca2f2c412f748f853fb76fcd7fe3e41d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009377"
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

 

 




