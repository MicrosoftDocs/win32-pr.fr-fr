---
title: Fonctions SNMP
description: Cette rubrique décrit trois regroupements de fonctions SNMP et répertorie les fonctions incluses dans chaque groupe.
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- SNMP, fonctions SNMP
- Fonctions SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f4cc98ce84fbb66f8beb59a6bf995dc4315159
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194015"
---
# <a name="snmp-functions"></a>Fonctions SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Cette rubrique décrit trois regroupements de fonctions SNMP et répertorie les fonctions incluses dans chaque groupe :

-   [Fonctions de l’API de l’agent d’extension SNMP](#snmp-extension-agent-api-functions)
-   [Fonctions de l’API de gestion SNMP](#snmp-management-api-functions)
-   [Fonctions de l’API de l’utilitaire SNMP](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>Fonctions de l’API de l’agent d’extension SNMP

Les fonctions de l’agent d’extension SNMP définissent l’interface entre le service SNMP et les dll d’agent d’extension SNMP tierces. Le tableau suivant répertorie les fonctions que les applications peuvent utiliser pour résoudre les liaisons de variables spécifiées par les unités de données de protocole SNMP (PDU) entrantes.

| Fonction de l’API de l’agent d’extension SNMP                    | Description                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**SnmpExtensionClose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Demande que l’agent d’extension SNMP libère des ressources et termine les opérations.                                    |
| [**SnmpExtensionInit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Initialise la DLL de l’agent d’extension SNMP.                                                                                |
| [**SnmpExtensionInitEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Identifie toutes les sous-arborescences MIB (Management Information base) supplémentaires prises en charge par l’agent d’extension SNMP.             |
| [**SnmpExtensionMonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Fournit à l’agent d’extension SNMP des informations sur les compteurs internes et les paramètres du service.            |
| [**SnmpExtensionQuery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Résout les requêtes SNMP qui contiennent des variables dans une ou plusieurs sous-arborescences MIB inscrites de l’agent d’extension SNMP. |
| [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Traite les requêtes SNMP qui spécifient des variables dans une ou plusieurs sous-arborescences MIB inscrites par des agents d’extension SNMP. |
| [**SnmpExtensionTrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Récupère les informations dont le service a besoin pour générer des interruptions pour l’agent d’extension SNMP.                          |



 

## <a name="snmp-management-api-functions"></a>Fonctions de l’API de gestion SNMP

Les fonctions de gestion SNMP définissent l’interface entre les applications du gestionnaire SNMP tiers et la bibliothèque de liens dynamiques (DLL) de la fonction de gestion Mgmtapi.dll. La DLL fonctionne conjointement avec le service d’interruption SNMP (Snmptrap.exe) et peut interagir avec une ou plusieurs applications tierces du gestionnaire SNMP. Le tableau suivant répertorie les fonctions de gestion utilisées par des applications de gestionnaire tierces pour effectuer les opérations du gestionnaire SNMP.

| Fonction de l’API de gestion SNMP                   | Description                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpMgrClose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Ferme les sockets de communication et les structures de données associés à la session spécifiée.                                                                                                  |
| [**SnmpMgrCtl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Définit un paramètre d’opération associé à une session SNMP.                                                                                                                                   |
| [**SnmpMgrGetTrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Retourne les données d’interruption en attente que l’appelant n’a pas reçues si la réception de l’interruption est activée.                                                                                                           |
| [**SnmpMgrGetTrapEx**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Retourne les données d’interruption en attente que l’appelant n’a pas reçues si la réception de l’interruption est activée. Retourne également l’adresse de la source de transport et l’interruption de la communauté associée à l’interruption. |
| [**SnmpMgrOidToStr**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Convertit une structure d’identificateur d’objet interne en sa représentation sous forme de chaîne.                                                                                                                         |
| [**SnmpMgrOpen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Initialise les sockets de communication et les structures de données nécessaires pour établir la communication avec l’agent SNMP.                                                                               |
| [**SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Demande que l’opération spécifiée soit exécutée par l’agent spécifié.                                                                                                                             |
| [**SnmpMgrStrToOid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Convertit le format de chaîne d’un identificateur d’objet en sa structure d’identificateur d’objet interne.                                                                                                        |
| [**SnmpMgrTrapListen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Enregistre la capacité d’une application gestionnaire SNMP à recevoir des interruptions SNMP du service d’interruption SNMP.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>Fonctions de l’API de l’utilitaire SNMP

Les fonctions de l’utilitaire SNMP offrent des fonctionnalités qui sont utiles lors du développement d’applications SNMP, notamment la simplification de la manipulation des structures de données SNMP. Le tableau suivant répertorie les fonctions de l’utilitaire SNMP.

| Fonction API de l’utilitaire SNMP                                  | Description                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpSvcGetUptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Récupère le temps, en centiseconds, pendant lequel le service SNMP est en cours d’exécution.                                                                                  |
| [**SnmpSvcSetLogLevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Ajuste le niveau de détail de la sortie de débogage à partir du service SNMP et des agents d’extension SNMP.                                                              |
| [**SnmpSvcSetLogType**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Ajuste la destination pour la sortie de débogage du service SNMP et des agents d’extension SNMP.                                                                 |
| [**SnmpUtilAsnAnyCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Copie une structure [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) source vers une structure **AsnAny** de destination.                                                                      |
| [**SnmpUtilAsnAnyFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Libère la mémoire qui a été allouée pour une structure [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) spécifiée.                                                                        |
| [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Définit le niveau des informations de débogage à recevoir à partir du service SNMP ou à partir d’un appel à [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint).                       |
| [**SnmpUtilIdsToA**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Convertit un identificateur d’objet (OID) en chaîne terminée par le caractère null.                                                                                                   |
| [**SnmpUtilMemAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Alloue de la mémoire dynamique à partir du tas de processus.                                                                                                                    |
| [**SnmpUtilMemFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Libère l’objet mémoire spécifié.                                                                                                                                 |
| [**SnmpUtilMemReAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Modifie la taille de l’objet mémoire spécifié.                                                                                                                   |
| [**SnmpUtilOctetsCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Compare deux chaînes d’octets.                                                                                                                                        |
| [**SnmpUtilOctetsCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Copie une structure [**AsnOctetString**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) source vers une structure **AsnOctetString** de destination.                                              |
| [**SnmpUtilOctetsFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Libère la mémoire qui a été allouée pour la chaîne d’octets spécifiée.                                                                                                |
| [**SnmpUtilOctetsNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Effectue une comparaison de deux chaînes d’octets avec le nombre spécifié de sous-identificateurs.                                                                              |
| [**SnmpUtilOidAppend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Ajoute un identificateur d’objet source, contenu dans une structure [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) , à un identificateur d’objet de destination.          |
| [**SnmpUtilOidCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Compare deux identificateurs d’objet contenus dans les structures [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) .                                           |
| [**SnmpUtilOidCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Copie une structure [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) source vers une structure **AsnObjectIdentifier** de destination.                               |
| [**SnmpUtilOidFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Libère la mémoire qui a été allouée pour l’identificateur d’objet spécifié.                                                                                           |
| [**SnmpUtilOidNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Compare deux identificateurs d’objet contenus dans les structures [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) au nombre spécifié de sous-identificateurs. |
| [**SnmpUtilOidToA**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Convertit un identificateur d’objet (OID) en chaîne terminée par le caractère null.                                                                                                   |
| [**SnmpUtilPrintAsnAny**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Imprime une valeur contenue dans une structure [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) à des fins de débogage et de développement.                                              |
| [**SnmpUtilPrintOid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Met en forme l’identificateur d’objet (OID) spécifié et imprime le résultat sur le périphérique de sortie standard.                                                                 |
| [**SnmpUtilVarBindCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Copie une structure [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) source vers une structure **SnmpVarBind** de destination.                                                       |
| [**SnmpUtilVarBindListCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Copie une structure [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) source vers une structure **SnmpVarBindList** de destination.                                           |
| [**SnmpUtilVarBindFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Libère la mémoire qui a été allouée pour la structure [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) spécifiée.                                                            |
| [**SnmpUtilVarBindListFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Libère la mémoire qui a été allouée pour la structure [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) spécifiée.                                                    |



 

 

 