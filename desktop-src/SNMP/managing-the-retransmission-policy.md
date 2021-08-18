---
title: Gestion de la stratégie de retransmission
description: L’application WinSNMP peut demander que l’implémentation de l’WinSNMP Microsoft exécute la stratégie de retransmission de l’application. Lorsque l’implémentation gère la retransmission, elle utilise le délai d’attente et les valeurs du nombre de tentatives dans sa base de données.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63737f8cb4a0fcdb8c6e3824d07cbc7c592c1f7e9813e8751197fcd1d64ad786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009427"
---
# <a name="managing-the-retransmission-policy"></a>Gestion de la stratégie de retransmission

L’application WinSNMP peut demander que l’implémentation de l’WinSNMP Microsoft exécute la stratégie de retransmission de l’application. Lorsque l’implémentation gère la retransmission, elle utilise le délai d’attente et les valeurs du nombre de tentatives dans sa base de données.

L’implémentation identifie le mode de retransmission par défaut dans une valeur de retour de la fonction [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) lors de l’initialisation. Le mode peut prendre l’une des valeurs suivantes.



| Valeur        | Signification                                                                      |
|--------------|------------------------------------------------------------------------------|
| SNMPAPI \_ sur  | L’implémentation exécute la stratégie de retransmission de l’application.     |
| SNMPAPI \_ désactivé | L’implémentation n’exécute pas la stratégie de retransmission de l’application. |



 

Une application WinSNMP peut récupérer à tout moment le mode de retransmission en vigueur pour l’implémentation en appelant la fonction [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) . L’API WinSNMP fournit d’autres [fonctions de base de données](winsnmp-functions.md) qui simplifient la gestion de la stratégie de retransmission.

À tout moment pendant l’exécution du programme, l’application WinSNMP peut ajuster l’exécution de la stratégie en effectuant l’une des étapes suivantes :

-   Demandez que l’implémentation démarre ou arrête l’exécution de la stratégie de retransmission en appelant la fonction [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) . Pour plus d’informations, consultez [activation et désactivation de la retransmission](turning-retransmission-on-and-off.md).
-   Modifiez les valeurs de délai d’attente et de nombre de nouvelles tentatives dans la base de données de l’implémentation. Pour plus d’informations, consultez [modification de la stratégie de retransmission](changing-the-retransmission-policy.md).
-   Appelez la fonction [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) pour annuler le cycle de retransmission et libérer les structures de données internes associées à une demande de message SNMP unique. Pour plus d’informations, consultez annulation de la [retransmission](canceling-retransmission.md).

L’application peut exécuter sa propre stratégie de retransmission. Dans ce cas, l’exécution peut ou non reposer sur les valeurs de la base de données.

 

 




