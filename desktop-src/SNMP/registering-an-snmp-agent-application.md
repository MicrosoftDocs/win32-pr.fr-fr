---
title: Inscription d’une application d’agent SNMP
description: Outre les opérations du gestionnaire SNMP, la version 2,0 de l’API WinSNMP prend également en charge les opérations de l’agent SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3415e511639c7cbbc18455ed93be74e11414c1f442797c8b72f7456092757c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009127"
---
# <a name="registering-an-snmp-agent-application"></a>Inscription d’une application d’agent SNMP

Outre les opérations du gestionnaire SNMP, la version 2,0 de l’API WinSNMP prend également en charge les opérations de l’agent SNMP.

Pour inscrire une application WinSNMP en tant qu’agent SNMP, l’application peut appeler la fonction [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) . Cette fonction indique à l’implémentation de Microsoft WinSNMP qu’une entité SNMP agira dans le rôle d’un agent SNMP. L’application peut également appeler **SnmpListen** pour informer l’implémentation lorsqu’elle ne fera plus Office d’agent.

Si une application appelle la fonction [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) et passe la valeur SNMPAPI \_ dans le paramètre *lStatus* , les actions suivantes se produisent :

1.  L’entité qui fonctionnera dans un rôle d’agent SNMP est liée à son port attribué et « écoute » les demandes de message SNMP entrantes.
2.  L’agent utilise une logique spécifique à l’application pour traiter chaque requête SNMP.
3.  L’agent forme les réponses appropriées à chaque requête.
4.  L’agent transmet la réponse à l’entité à l’origine de la demande en appelant la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) . Lorsque l’agent appelle **SnmpSendMsg**, il spécifie l’adresse de l’agent dans le paramètre *srcEntity* , ainsi que l’adresse de l’entité Remote Manager dans le paramètre *dstEntity* . (Ces valeurs sont l’inverse des valeurs que l’entité agent a reçues dans ces paramètres lorsqu’elle a appelé la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) pour récupérer une demande SNMP.)

Pour plus d’informations sur les applications de gestion SNMP et les applications de l’agent, consultez [à propos de SNMP](about-snmp.md).

 

 




