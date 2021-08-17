---
title: Tâches de programmation WinSNMP
description: Le tableau suivant récapitule les procédures de programmation de base que vous devez effectuer pour coder une application WinSNMP et les rubriques qui fournissent des informations sur ces tâches.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007ed1a50688ceff7cdd3bfd9916c1726773cf5ecb2e175af99880950c5c3db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142792"
---
# <a name="winsnmp-programming-tasks"></a>Tâches de programmation WinSNMP

Le tableau suivant récapitule les procédures de programmation de base que vous devez effectuer pour coder une application WinSNMP et les rubriques qui fournissent des informations sur ces tâches.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tâche de programmation</th>
<th>Fonctions et rubriques liées aux tâches</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ouvrez l’application WinSNMP.</td>
<td>Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Consultez <a href="opening-and-closing-a-winsnmp-application.md">ouverture et fermeture d’une application WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Ouvrez une ou plusieurs sessions WinSNMP.</td>
<td>Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Consultez <a href="opening-and-closing-a-winsnmp-session.md">ouverture et fermeture d’une session WinSNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Inscrivez-vous pour recevoir des interruptions ou des notifications.</td>
<td>Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Consultez <a href="managing-traps-and-notifications.md">gestion des interruptions et des notifications</a>.<br/></td>
</tr>
<tr class="even">
<td>Créez une ou plusieurs listes de liaisons de variables pour l’incorporation dans une PDU.</td>
<td>Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Consultez <a href="working-with-variable-binding-lists.md">utilisation des listes de liaisons de variables</a>.<br/>
<blockquote>
[!Note]<br />
L’application devra peut-être appeler d’autres <a href="winsnmp-functions.md">fonctions de liaison de variable</a> pour créer la liste de liaisons de variables.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Créez une ou plusieurs PDU pour la transmission et le traitement.</td>
<td>Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>. Consultez <a href="working-with-protocol-data-units.md">utilisation des unités de données de protocole</a>.<br/>
<blockquote>
[!Note]<br />
L’application devra peut-être appeler d’autres fonctions de l' <a href="winsnmp-functions.md">PDU</a> et des fonctions de l' <a href="winsnmp-functions.md">utilitaire</a> WinSNMP pour créer l’unité d’alimentation.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Envoyer une ou plusieurs demandes d’opération SNMP.</td>
<td>Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>. Consultez la page <a href="sending-snmp-messages.md">envoi de messages SNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Récupérez la réponse à la demande d’opération SNMP.</td>
<td>Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>. Consultez <a href="receiving-snmp-messages.md">réception de messages SNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Traitez la réponse de la demande.</td>
<td>Utilisez une logique spécifique à l’application.</td>
</tr>
<tr class="odd">
<td>Fermez chaque session WinSNMP.</td>
<td>Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Consultez <a href="opening-and-closing-a-winsnmp-session.md">ouverture et fermeture d’une session WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Fermez l’application WinSNMP.</td>
<td>Utilisez <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Consultez <a href="opening-and-closing-a-winsnmp-application.md">ouverture et fermeture d’une application WinSNMP</a>.<br/></td>
</tr>
</tbody>
</table>



 

Les rubriques suivantes contiennent des informations supplémentaires sur d’autres concepts de programmation généraux spécifiques à l’environnement WinSNMP.



| Rubrique                                                              | Concepts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tâches de programmation générales](general-winsnmp-programming-tasks.md) | [Gestion des identificateurs d’objets libération des](managing-object-identifiers.md)[descripteurs WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Définition du mode de traduction entité et contexte](setting-the-entity-and-context-translation-mode.md)<br/> [Gestion de la stratégie de retransmission](managing-the-retransmission-policy.md)<br/> [Écriture d’applications WinSNMP avec plusieurs threads](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Inscription d’une application d’agent SNMP](registering-an-snmp-agent-application.md)<br/> |



 

En outre, l’application WinSNMP peut avoir besoin d’intégrer des appels aux fonctions WinSNMP suivantes : [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)et [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu). Cela permet à l’implémentation de Microsoft WinSNMP de libérer des objets de mémoire WinSNMP. En règle générale, l’application WinSNMP doit libérer toutes les ressources allouées à la suite d’un appel à une fonction WinSNMP. Pour plus d’informations sur la désallocation des ressources, consultez [allocation d’objets de mémoire WinSNMP](allocating-winsnmp-memory-objects.md).

 

 





