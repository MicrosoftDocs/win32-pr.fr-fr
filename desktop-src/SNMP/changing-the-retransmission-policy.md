---
title: Modification de la stratégie de retransmission
description: L’implémentation de l’WinSNMP de Microsoft fournit une prise en charge de la stratégie de retransmission en stockant une valeur de délai d’attente et un nombre de tentatives pour l’application WinSNMP dans une base de données.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed160de40b300d1b2430304b7a487f4544fee9a13db6049d1d837958276da8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009767"
---
# <a name="changing-the-retransmission-policy"></a>Modification de la stratégie de retransmission

L’implémentation de l’WinSNMP de Microsoft fournit une prise en charge de la stratégie de retransmission en stockant une valeur de délai d’attente et un nombre de tentatives pour l’application WinSNMP dans une base de données. L’implémentation stocke des valeurs pour des entités de destination individuelles. L’implémentation fournit initialement des valeurs par défaut pour ces éléments, mais une application peut ajouter ou modifier des valeurs pour des entités individuelles.

Un appel aux fonctions [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) et [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) retourne les valeurs de délai d’attente et de nombre de tentatives pour une entité de destination spécifique. Pour modifier la valeur du délai d’attente, une application WinSNMP doit appeler la fonction [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) . Pour modifier la valeur du nombre de tentatives, l’application doit appeler la fonction [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) . Les paramètres mis à jour affectent les nouvelles demandes de message SNMP à l’entité de destination.

 

 




