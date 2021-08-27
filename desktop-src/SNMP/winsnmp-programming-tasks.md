---
title: Tâches de programmation WinSNMP
description: Le tableau suivant récapitule les procédures de programmation de base que vous devez effectuer pour coder une application WinSNMP et les rubriques qui fournissent des informations sur ces tâches.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb83d6d61311866ddb84d3980f5742f82f51405
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479395"
---
# <a name="winsnmp-programming-tasks"></a>Tâches de programmation WinSNMP

Le tableau suivant récapitule les procédures de programmation de base que vous devez effectuer pour coder une application WinSNMP et les rubriques qui fournissent des informations sur ces tâches.




| Tâche de programmation | Fonctions et rubriques liées aux tâches | 
|------------------|----------------------------------|
| Ouvrez l’application WinSNMP. | Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Consultez <a href="opening-and-closing-a-winsnmp-application.md">ouverture et fermeture d’une application WinSNMP</a>.<br /> | 
| Ouvrez une ou plusieurs sessions WinSNMP. | Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Consultez <a href="opening-and-closing-a-winsnmp-session.md">ouverture et fermeture d’une session WinSNMP</a>.<br /> | 
| Inscrivez-vous pour recevoir des interruptions ou des notifications. | Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Consultez <a href="managing-traps-and-notifications.md">gestion des interruptions et des notifications</a>.<br /> | 
| Créez une ou plusieurs listes de liaisons de variables pour l’incorporation dans une PDU. | Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Consultez <a href="working-with-variable-binding-lists.md">utilisation des listes de liaisons de variables</a>.<br /><blockquote>[!Note]<br />L’application devra peut-être appeler d’autres <a href="winsnmp-functions.md">fonctions de liaison de variable</a> pour créer la liste de liaisons de variables.</blockquote><br /> | 
| Créez une ou plusieurs PDU pour la transmission et le traitement. | Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>. Consultez <a href="working-with-protocol-data-units.md">utilisation des unités de données de protocole</a>.<br /><blockquote>[!Note]<br />L’application devra peut-être appeler d’autres fonctions de l' <a href="winsnmp-functions.md">PDU</a> et des fonctions de l' <a href="winsnmp-functions.md">utilitaire</a> WinSNMP pour créer l’unité d’alimentation.</blockquote><br /> | 
| Envoyer une ou plusieurs demandes d’opération SNMP. | Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>. Consultez la page <a href="sending-snmp-messages.md">envoi de messages SNMP</a>.<br /> | 
| Récupérez la réponse à la demande d’opération SNMP. | Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>. Consultez <a href="receiving-snmp-messages.md">réception de messages SNMP</a>.<br /> | 
| Traitez la réponse de la demande. | Utilisez une logique spécifique à l’application. | 
| Fermez chaque session WinSNMP. | Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Consultez <a href="opening-and-closing-a-winsnmp-session.md">ouverture et fermeture d’une session WinSNMP</a>.<br /> | 
| Fermez l’application WinSNMP. | Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Consultez <a href="opening-and-closing-a-winsnmp-application.md">ouverture et fermeture d’une application WinSNMP</a>.<br /> | 




 

Les rubriques suivantes contiennent des informations supplémentaires sur d’autres concepts de programmation généraux spécifiques à l’environnement WinSNMP.



| Rubrique                                                              | Concepts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tâches de programmation générales](general-winsnmp-programming-tasks.md) | [Gestion des identificateurs d’objets libération des](managing-object-identifiers.md)[descripteurs WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Définition du mode de traduction entité et contexte](setting-the-entity-and-context-translation-mode.md)<br/> [Gestion de la stratégie de retransmission](managing-the-retransmission-policy.md)<br/> [Écriture d’applications WinSNMP avec plusieurs threads](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Inscription d’une application d’agent SNMP](registering-an-snmp-agent-application.md)<br/> |



 

En outre, l’application WinSNMP peut avoir besoin d’intégrer des appels aux fonctions WinSNMP suivantes : [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)et [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu). Cela permet à l’implémentation de Microsoft WinSNMP de libérer des objets de mémoire WinSNMP. En règle générale, l’application WinSNMP doit libérer toutes les ressources allouées à la suite d’un appel à une fonction WinSNMP. Pour plus d’informations sur la désallocation des ressources, consultez [allocation d’objets de mémoire WinSNMP](allocating-winsnmp-memory-objects.md).

 

 





