---
title: Annulation de la retransmission
description: S’il n’y a aucune réponse à une demande de communication dans le délai d’attente spécifié pour une entité de destination et si des retransmissions sont spécifiées pour l’entité, l’implémentation de l’WinSNMP de Microsoft retransmet la demande.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029204"
---
# <a name="canceling-retransmission"></a>Annulation de la retransmission

S’il n’y a aucune réponse à une demande de communication dans le délai d’attente spécifié pour une entité de destination et si des retransmissions sont spécifiées pour l’entité, l’implémentation de l’WinSNMP de Microsoft retransmet la demande. Un appel à la fonction [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) peut annuler ce cycle de retransmission et libérer les structures de données internes associées à la demande de message.

Notez qu’il est possible pour une entité de destination de recevoir un message SNMP qui a été annulé par un appel à la fonction [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) . Il est également possible qu’une entité de destination puisse répondre à un message SNMP annulé. Cela est dû au fait que la mise en file d’attente des transactions se produit à plusieurs niveaux. Toutefois, une fois qu’un message a été annulé par un appel à [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), l’implémentation de l’WinSNMP de Microsoft ne retransmet pas le message, soumet un PDU de réponse ou envoie une notification d’expiration à l’application pour ce message.

 

 




