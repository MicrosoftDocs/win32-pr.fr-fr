---
title: Traduction des demandes de message
description: Cette rubrique décrit le processus de traduction des demandes SNMPv1 en demandes SNMPv2.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1775d59a8de0bd0473570f3028018a1a25cad2ebd4ee004025ad11a38e37e69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885889"
---
# <a name="translating-message-requests"></a>Traduction des demandes de message

Cette rubrique décrit le processus de traduction des demandes SNMPv1 en demandes SNMPv2.

Si une application WinSNMP demande une fonctionnalité qui est disponible sous la version de SNMP version 2C Framework (SNMPv2C), mais que l’entité cible prend uniquement en charge SNMP version 1 Framework (SNMPv1), l’implémentation Microsoft WinSNMP tente de convertir la demande au format SNMPv1. Pour ce faire, l’implémentation utilise les procédures définies dans le document RFC 1908, « coexistence entre la version 1 et la version 2 de l’infrastructure de gestion de réseau Internet-Standard ». Si la traduction n’est pas possible, la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) échoue avec le code d’erreur étendu SNMPAPI \_ opération \_ non valide.

 

 




