---
title: Modification de la stratégie de retransmission
description: L’implémentation de l’WinSNMP de Microsoft fournit une prise en charge de la stratégie de retransmission en stockant une valeur de délai d’attente et un nombre de tentatives pour l’application WinSNMP dans une base de données.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840073"
---
# <a name="changing-the-retransmission-policy"></a>Modification de la stratégie de retransmission

L’implémentation de l’WinSNMP de Microsoft fournit une prise en charge de la stratégie de retransmission en stockant une valeur de délai d’attente et un nombre de tentatives pour l’application WinSNMP dans une base de données. L’implémentation stocke des valeurs pour des entités de destination individuelles. L’implémentation fournit initialement des valeurs par défaut pour ces éléments, mais une application peut ajouter ou modifier des valeurs pour des entités individuelles.

Un appel aux fonctions [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) et [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) retourne les valeurs de délai d’attente et de nombre de tentatives pour une entité de destination spécifique. Pour modifier la valeur du délai d’attente, une application WinSNMP doit appeler la fonction [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) . Pour modifier la valeur du nombre de tentatives, l’application doit appeler la fonction [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) . Les paramètres mis à jour affectent les nouvelles demandes de message SNMP à l’entité de destination.

 

 




