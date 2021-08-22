---
title: Erreurs de transport réseau
description: L’implémentation de Microsoft WinSNMP peut détecter une erreur de transport réseau après avoir transmis un message SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15284bba97f2dda8d2fb4224dc2c94bd14050afb9463c73b4d297c1647ec273f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009307"
---
# <a name="network-transport-errors"></a>Erreurs de transport réseau

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

L’implémentation de Microsoft WinSNMP peut détecter une erreur de transport réseau après avoir transmis un message SNMP. Dans ce cas, l’implémentation envoie une notification de réception de données à la session WinSNMP qui a initié la demande de communication. L’implémentation retourne également l' \_ échec SNMPAPI lors de l’appel suivant à la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour la session. La fonction **SnmpRecvMsg** échoue avec un code d’erreur étendu qui indique une erreur de couche de transport réseau.

Pour obtenir la liste des erreurs spécifiques de la couche de transport, consultez les pages de référence pour les fonctions [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)et [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

 

 