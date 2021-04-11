---
title: À propos de l’implémentation de Microsoft WinSNMP
description: L’implémentation de Microsoft WinSNMP est conforme à la version 2,0 de WinSNMP.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939557"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a>À propos de l’implémentation de Microsoft WinSNMP

L’implémentation de Microsoft WinSNMP est conforme à la version 2,0 de WinSNMP. Il prend en charge toutes les fonctions et opérations définies à la fois dans les spécifications de la version 1.1 de WinSNMP et dans l’addenda de la version 2,0 de l’WinSNMP. L’implémentation fournit les services suivants pour les applications WinSNMP :

-   Gère les communications vers et à partir des entités de gestion. L’entité peut résider sur l’ordinateur local ou être connectée via un réseau local ou étendu, ou Internet. Pour plus d’informations, consultez [niveaux de prise en charge de SNMP](levels-of-snmp-support.md).
-   Masque les détails du protocole SNMP, le ASN (Abstract Syntax Notation One) et les règles de codage de base (BER) pour décrire la syntaxe de transfert.
-   Vérifie l’exactitude des PDU et rejette les PDU non valides. Pour plus d’informations, consultez [utilisation des unités de données de protocole](working-with-protocol-data-units.md).
-   Transforme les types de PDU SNMPv2C lorsque cela est nécessaire conformément aux RFC pertinentes.
-   Convertit les interruptions SNMPv1 d’un agent SNMPv1 en interruptions SNMPv2C, conformément à la norme RFC 1908, « coexistence entre la version 1 et la version 2 de l’infrastructure de gestion de réseau Internet standard ». Pour plus d’informations, consultez [conversion d’interruptions de SNMPv1 en SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).
-   Prend en charge la stratégie de retransmission de l’application et fournit la prise en charge de l’exécution de la retransmission. Pour plus d’informations, consultez [la base de données WinSNMP](the-winsnmp-database.md) et [à propos de la retransmission](about-retransmission.md).
-   Fournit la prise en charge de la traduction des entités et des contextes pour l’application. Pour plus d’informations, consultez [la base de données WinSNMP](the-winsnmp-database.md) et [définition de l’entité et du mode de traduction du contexte](setting-the-entity-and-context-translation-mode.md).

Pour plus d’informations sur la relation entre une application WinSNMP et l’implémentation, consultez l’article sur les [concepts de gestion des données WinSNMP](winsnmp-data-management-concepts.md) et les [sessions WinSNMP](winsnmp-sessions.md).

 

 




