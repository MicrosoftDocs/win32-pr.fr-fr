---
title: La base de données WinSNMP
description: L’implémentation de Microsoft WinSNMP gère un magasin d’informations administratives dans une base de données.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462134"
---
# <a name="the-winsnmp-database"></a>La base de données WinSNMP

L’implémentation de Microsoft WinSNMP gère un magasin d’informations administratives dans une base de données. La base de données comprend les informations suivantes :

-   Propriétés du réseau et de la version.

    L’implémentation utilise ces propriétés pour déterminer le protocole de transport réseau et la structure de la version SNMP à utiliser pour effectuer les demandes de transmission. Pour plus d’informations, consultez [à propos des versions SNMP](about-snmp-versions.md).

-   Mode de traduction entité et contexte.

    L’implémentation utilise ce mode pour interpréter des noms conviviaux pour les entités et les contextes SNMP. Pour plus d’informations, consultez [définition du mode de traduction entité et contexte](setting-the-entity-and-context-translation-mode.md).

-   Paramètre de stratégie de retransmission.

    L’implémentation utilise ce paramètre pour déterminer s’il doit ou non exécuter la stratégie de retransmission de l’application. L’implémentation stocke une valeur de délai d’attente et un nombre de tentatives pour chaque entité de destination. Pour plus d’informations, consultez [à propos de la retransmission](about-retransmission.md) et de [la gestion de la stratégie de retransmission](managing-the-retransmission-policy.md).

 

 




