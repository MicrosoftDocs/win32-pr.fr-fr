---
title: Fonctions WinSNMP
description: Les fonctions utilisées avec l’WinSNMP sont classées dans les regroupements fonctionnels suivants. Une liste alphabétique suit.
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c355cb8da6a892614e7729d1db75ded3c3fb9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476955"
---
# <a name="winsnmp-functions"></a>Fonctions WinSNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Les fonctions utilisées avec l’WinSNMP sont classées dans les regroupements fonctionnels suivants. Une liste alphabétique suit.

-   [Fonctions de communication](#winsnmp-communications-functions)
-   [Fonctions d’entité et de contexte](#winsnmp-entity-and-context-functions)
-   [Fonctions de base de données](#winsnmp-database-functions)
-   [Fonctions PDU](#winsnmp-pdu-functions)
-   [Fonctions utilitaires](#winsnmp-utility-functions)
-   [Fonctions de liaison de variable](#winsnmp-variable-binding-functions)
-   [Liste alphabétique des fonctions WinSNMP](/windows)

## <a name="winsnmp-communications-functions"></a>Fonctions de communications WinSNMP

Les fonctions de communications WinSNMP fournissent une interface entre l’application WinSNMP d’appel et l’implémentation de l’WinSNMP Microsoft. L’implémentation gère la communication entre l’application et d’autres entités de gestion.




| Fonction | Description | 
|----------|-------------|
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>SnmpCancelMsg</strong></a> | Demande que l’implémentation de l’WinSNMP Microsoft annule les tentatives de retransmission et les notifications de délai d’attente pour un message de demande SNMP. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a> | Informe l’implémentation qu’une application est déconnectée et ne nécessite plus de ressources allouées. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>SnmpCleanupEx</strong></a> | Effectue un nettoyage lorsqu’il n’existe aucun appel réussi à <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> ou <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> dans une application winsnmp. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a> | Permet à l’implémentation de libérer les ressources associées à une session et de fermer les mécanismes de communication. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> | Demande à l’implémentation d’ouvrir une session WinSNMP et d’allouer des ressources et des mécanismes de communication. Lorsque vous développez de nouvelles applications WinSNMP, il est recommandé d’appeler la fonction <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> pour ouvrir une session WinSNMP au lieu d’appeler la fonction <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a> . | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>SnmpListen</strong></a> | Inscrit ou annule l’inscription d’une application WinSNMP en tant qu’agent SNMP. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a> | Demande à l’implémentation d’ouvrir une session WinSNMP et d’allouer des ressources et des mécanismes de communication. Lorsque vous développez de nouvelles applications WinSNMP, il est recommandé d’appeler la fonction <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> pour ouvrir une session WinSNMP au lieu d’appeler la fonction <strong>SnmpOpen</strong> . | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a> | Retourne des messages SNMP, des données d’interruption et des notifications en attente. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a> | Informe l’implémentation que l’application doit inscrire ou annuler l’inscription pour les interruptions et les notifications. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a> | Demande que l’implémentation transmette une unité de données de protocole. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> | Indique à l’implémentation d’effectuer des procédures d’initialisation pour l’application. Une application doit appeler la fonction <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> avec succès avant d’appeler une autre fonction winsnmp. | 
| <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> | Notifie l’implémentation de Microsoft WinSNMP que l’application WinSNMP requiert les services de l’implémentation. <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> permet la prise en charge de plusieurs modules logiciels indépendants qui utilisent WinSNMP au sein de la même application. | 
| <a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a> | Avertit une session WinSNMP qu’un message SNMP ou un événement asynchrone est disponible.<blockquote>[!Note]<br />Cette fonction de rappel s’applique uniquement aux sessions ouvertes à la suite d’un appel à la fonction <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> .</blockquote><br /> | 




 

## <a name="winsnmp-entity-and-context-functions"></a>Fonctions d’entité et de contexte WinSNMP

L’entité WinSNMP et les fonctions de contexte permettent à une application WinSNMP de spécifier des noms conviviaux pour les entités et les contextes SNMP. L’implémentation de l’WinSNMP Microsoft traduit le nom en composants SNMPv1 ou SNMPv2C à l’aide de la base de données de l’implémentation.



| Fonction                                     | Description                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | Retourne une chaîne qui identifie un contexte SNMP (un ensemble de ressources d’objet managé).                                  |
| [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | Retourne une chaîne qui identifie une entité de gestion SNMP.                                                            |
| [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | Libère les ressources allouées par la fonction [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) pour un contexte SNMP.         |
| [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | Libère les ressources allouées par la fonction [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) pour une entité de gestion SNMP. |
| [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | Modifie le port affecté à une entité de destination SNMP.                                                               |
| [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | Retourne un handle vers des informations de contexte SNMP qui sont spécifiques à l’implémentation.                                   |
| [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | Retourne un handle pour les informations d’entité de gestion SNMP qui sont spécifiques à l’implémentation.                         |



 

## <a name="winsnmp-database-functions"></a>Fonctions de base de données WinSNMP

Les fonctions de base de données WinSNMP fournissent à une application WinSNMP un accès aux paramètres actuels dans le magasin d’informations d’administration de l’implémentation de Microsoft WinSNMP. Ces fonctions permettent de modifier le mode de retransmission et l’entité et le mode de traduction du contexte. Les fonctions de base de données fournissent également à l’application la possibilité de manipuler les valeurs de délai d’attente et de nombre de nouvelles tentatives.



| Fonction                                               | Description                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | Retourne le paramètre actuel du mode de retransmission.                                               |
| [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | Retourne la valeur du nombre de tentatives, en unités, pour la retransmission des demandes de message SNMP.             |
| [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | Retourne la valeur du délai d’attente, en centièmes de seconde, pour la transmission des demandes de message SNMP. |
| [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | Retourne le paramètre actuel de l’entité et du mode de traduction du contexte.                               |
| [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | Récupère des informations qui identifient le fournisseur WinSNMP.                                             |
| [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | Modifie le mode de retransmission.                                                                      |
| [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | Modifie la valeur du nombre de tentatives pour la retransmission des demandes de message SNMP.                        |
| [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | Modifie la valeur de délai d’attente pour la transmission des demandes de message SNMP.                             |
| [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | Modifie l’entité et le mode de traduction du contexte.                                                      |



 

## <a name="winsnmp-pdu-functions"></a>Fonctions de l’IPDU WinSNMP

Les fonctions de l’IPDU WinSNMP permettent aux applications WinSNMP d’extraire et de mettre à jour les éléments de données (ou champs) d’une PDU. Cela comprend les PDU retournées par un appel à la fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) ou à la fonction [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) . Les fonctions PDU construisent également des PDU à utiliser dans les fonctions [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) et [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .



| Fonction                                     | Description                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | Crée et Initialise une unité de données de protocole SNMP.                                                                                                                               |
| [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | Duplique une unité de données de protocole SNMP.                                                                                                                                            |
| [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | Libère les ressources associées à une unité de données de protocole SNMP créée par [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou la fonction [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) . |
| [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | Retourne les éléments de données sélectionnés à partir d’une unité de données de protocole SNMP spécifiée.                                                                                                          |
| [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | Met à jour les éléments de données sélectionnés dans une unité de données de protocole SNMP spécifiée.                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a>Fonctions de l’utilitaire WinSNMP

Les fonctions de l’utilitaire WinSNMP permettent à une application WinSNMP de gérer des objets et des messages SNMP à travers l’interface WinSNMP.



| Fonction                                         | Description                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | Décode un message SNMP encodé ou sérialisé en ses composants constitutifs.                                      |
| [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | Crée un message SNMP encodé.                                                                                    |
| [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | Signale à l’implémentation de l’WinSNMP Microsoft qu’il doit libérer la mémoire allouée pour un descripteur spécifique. |
| [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | Retourne la dernière valeur de code d’erreur pour la dernière opération SNMP.                                                      |
| [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | Compare deux identificateurs d’objet SNMP.                                                                               |
| [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | Copie un identificateur d’objet SNMP.                                                                                   |
| [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | Convertit la représentation binaire interne d’un identificateur d’objet SNMP en son format de chaîne numérique en pointillés.       |
| [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | Convertit le format de chaîne numérique avec points d’un identificateur d’objet SNMP en sa représentation binaire interne.       |



 

## <a name="winsnmp-variable-binding-functions"></a>Fonctions de liaison de variable WinSNMP

Les fonctions de liaison de la variable WinSNMP permettent aux applications WinSNMP de construire et de manipuler des listes de liaisons de variables, et de les inclure dans des PDU.



| Fonction                                     | Description                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | Énumère les entrées de liaison de variable dans une liste de liaisons de variables spécifiée.                                                                                                   |
| [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | Crée une nouvelle liste de liaisons de variables.                                                                                                                                            |
| [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | Supprime une entrée de liaison de variable d’une liste de liaisons de variables.                                                                                                                  |
| [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | Copie une liste de liaisons de variables.                                                                                                                                                 |
| [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | Libère des ressources pour une liste de liaisons de variable allouée précédemment par [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) ou la fonction [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . |
| [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | Récupère des informations à partir d’une entrée de liaison de variable spécifiée.                                                                                                                  |
| [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | Modifie les entrées de liaison de variable dans une liste de liaisons de variables ; Ajoute de nouvelles entrées de liaison de variable à une liste de liaisons de variables existante.                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a>Liste alphabétique des fonctions WinSNMP

-   [**\_rappel SNMPAPI**](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
-   [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)
-   [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)
-   [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)
-   [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)
-   [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)
-   [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)
-   [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)
-   [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)
-   [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)
-   [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)
-   [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)
-   [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)
-   [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)
-   [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)
-   [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)
-   [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)
-   [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)
-   [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)
-   [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)
-   [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)
-   [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)
-   [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode)
-   [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)
-   [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)
-   [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)
-   [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)
-   [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)
-   [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten)
-   [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)
-   [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)
-   [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)
-   [**SnmpOpen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen)
-   [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)
-   [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)
-   [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)
-   [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)
-   [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)
-   [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)
-   [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)
-   [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)
-   [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)
-   [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)
-   [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)
-   [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)
-   [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)
-   [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

 

