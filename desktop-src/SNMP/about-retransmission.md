---
title: À propos de la retransmission
description: Une application WinSNMP peut effectuer des demandes d’opération SNMP de différentes manières.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a26ba632cec096300927911c2277cbcf5911e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309598"
---
# <a name="about-retransmission"></a>À propos de la retransmission

Une application WinSNMP peut effectuer des demandes d’opération SNMP de différentes manières. L’application peut émettre plusieurs demandes à un agent SNMP, sans attendre de réponse, ou émettre une seule demande et attendre la réponse. Étant donné que SNMP peut être implémenté sur plusieurs protocoles de transport, les mécanismes de remise et les caractéristiques de fiabilité peuvent varier.

Lorsque vous codez l’application WinSNMP, vous devez déterminer le niveau de fiabilité dont vous avez besoin pour les opérations de communication, en fonction de la façon dont l’application émet les demandes d’opération. Vous devez ensuite sélectionner une stratégie de retransmission et implémenter une stratégie de retransmission.

Une stratégie de retransmission comprend un délai d’attente et un nombre de tentatives. Un délai d’attente est le temps écoulé, en centièmes de seconde, entre l’émission par une application d’une demande [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) et sa réception du message correspondant. L’application reçoit le message à la suite d’un appel à la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) . La valeur du délai d’attente est la période pendant laquelle l’implémentation de l’WinSNMP Microsoft attend qu’une entité réponde à une demande de communication. S’il n’y a pas de réponse dans le délai imparti, l’implémentation retransmet la demande si la valeur du nombre de tentatives spécifie des tentatives de retransmission ou échoue l’appel à [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg). Un nombre de tentatives est le nombre maximal de tentatives de retransmission effectuées par l’implémentation en cas d’échec d’une demande de transmission SNMP.

L’implémentation stocke les valeurs de délai d’attente et les nombres de tentatives dans sa base de données pour l’application. L’implémentation stocke des valeurs individuelles pour chaque entité de destination.

Les applications doivent établir leurs propres fréquences d’interrogation et doivent gérer les variables de minuterie. Pour plus d’informations, consultez [gestion de la stratégie de retransmission](managing-the-retransmission-policy.md).

 

 




