---
title: Niveaux de prise en charge SNMP
description: L’implémentation de l’WinSNMP de Microsoft fournit la prise en charge des communications SNMP de niveau 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa76a475ed266a7a4928a79f809b7011a537c777c89ea0a97d06983d6656a9ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009457"
---
# <a name="levels-of-snmp-support"></a>Niveaux de prise en charge SNMP

L’implémentation de l’WinSNMP de Microsoft fournit la prise en charge des communications SNMP de niveau 2. Le niveau 2 prend en charge le protocole SNMPv2 standard de l’IETF (Internet Engineering Task Force), tel que défini dans les RFC 1902-1908. Il prend également en charge le wrapper de message basé sur la Communauté, tel que défini dans le document RFC 1901 (SNMPv2C).

La prise en charge des communications de niveau 2 comprend l’encodage et le décodage des messages, précédemment appelé prise en charge des communications de niveau 0 dans WinSNMP version 1.1 a. Le niveau 2 prend également en charge toutes les opérations de protocole SNMPv1, précédemment appelées prise en charge des communications de niveau 1 dans la version 1.1 de WinSNMP.

L’implémentation retourne le niveau maximal de communications SNMP qu’il prend en charge en réponse à un appel de l’application WinSNMP à la fonction [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) .

Si l’application WinSNMP utilise l’implémentation pour le codage et le décodage des messages SNMP uniquement, l’application doit effectuer les transformations requises que l’implémentation aurait effectué. Cela comprend la traduction des interruptions SNMPv1 retournées par un appel à la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) , vers des interruptions SNMPv2c. Il comprend également la conversion des types de PDU définis par SNMPv1 vers le type de PDU approprié défini par SNMPv2C, conformément à la norme RFC 1908.

 

 




