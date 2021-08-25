---
title: Activation et désactivation de la retransmission
description: Une application peut définir le mode de retransmission avec un appel à la fonction SnmpSetRetransmitMode. Le nouveau mode de retransmission s’applique aux appels suivants à la fonction SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7624977b4959911cc4128c9a75ac70fac7031bfb853c4b31db34d0987b4d4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885669"
---
# <a name="turning-retransmission-on-and-off"></a>Activation et désactivation de la retransmission

Une application peut définir le mode de retransmission avec un appel à la fonction [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) . Le nouveau mode de retransmission s’applique aux appels suivants à la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .

Lorsque l’application appelle **SnmpSetRetransmitMode** avec la valeur du mode de retransmission SNMPAPI \_ sur, l’implémentation de l’WinSNMP Microsoft commence l’exécution de la stratégie de retransmission de l’application. Le nouveau mode de retransmission n’affecte pas les messages SNMP en suspens. Un message en attente est un message qui n’a pas de réponse au moment où l’application modifie le mode de retransmission.

Lorsque l’application WinSNMP appelle la fonction [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) avec le mode de retransmission valeur SNMPAPI \_ off, l’implémentation cesse d’exécuter la stratégie de retransmission. L’implémentation annule les tentatives de retransmission pour les messages SNMP en attente. Cela est dû au fait qu’il n’est pas possible que l’implémentation gère toutes les demandes et toutes les opérations SNMP en suspens, ainsi que les nouvelles requêtes, avant qu’un délai d’attente d’application ou un compteur de tentatives ne signale un événement.

 

 




