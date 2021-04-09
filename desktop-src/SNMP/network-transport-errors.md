---
title: Erreurs de transport réseau
description: L’implémentation de Microsoft WinSNMP peut détecter une erreur de transport réseau après avoir transmis un message SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842606"
---
# <a name="network-transport-errors"></a>Erreurs de transport réseau

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

L’implémentation de Microsoft WinSNMP peut détecter une erreur de transport réseau après avoir transmis un message SNMP. Dans ce cas, l’implémentation envoie une notification de réception de données à la session WinSNMP qui a initié la demande de communication. L’implémentation retourne également l' \_ échec SNMPAPI lors de l’appel suivant à la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour la session. La fonction **SnmpRecvMsg** échoue avec un code d’erreur étendu qui indique une erreur de couche de transport réseau.

Pour obtenir la liste des erreurs spécifiques de la couche de transport, consultez les pages de référence pour les fonctions [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)et [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

 

 