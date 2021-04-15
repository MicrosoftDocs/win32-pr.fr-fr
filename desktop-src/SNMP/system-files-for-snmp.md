---
title: Fichiers système pour SNMP
description: Le tableau suivant décrit les principaux fichiers liés au service SNMP.
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb917276fd807835fea703ec27cc66a0d493766d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462135"
---
# <a name="system-files-for-snmp"></a>Fichiers système pour SNMP

Le tableau suivant décrit les principaux fichiers liés au service SNMP.



| Nom de fichier     | Description                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | DLL de l’agent d’extension qui implémente la MIB DHCP définie par Microsoft. Installé uniquement sur les serveurs DHCP.                                                                                                                                 |
| EVNTAGNT.DLL | DLL SNMP qui traduit les journaux des événements en interruptions SNMP ; également connu sous le nom de traducteur d’événements SNMP.                                                                                                                                       |
| HOSTMIB.DLL  | DLL de l’agent d’extension qui implémente la MIB des ressources de l’hôte.                                                                                                                                                                         |
| LMMIB2.DLL   | DLL de l’agent d’extension qui implémente LAN Manager MIB-II.                                                                                                                                                                             |
| MGMTAPI.DLL  | Bibliothèque de l’API de gestion SNMP Microsoft. Cette API permet aux applications du gestionnaire SNMP d’écouter les requêtes du gestionnaire SNMP et d’envoyer des requêtes et de recevoir des réponses des agents SNMP.                                                |
| MIB. GRANULE      | Informations MIB compilées utilisées par MGMTAPI.DLL.                                                                                                                                                                                       |
| SNMP.EXE     | Service SNMP. Il s’agit de l’agent maître qui reçoit les demandes SNMP et les remet à la DLL de l’agent d’extension appropriée.                                                                                                        |
| SNMPAPI.DLL  | DLL des utilitaires SNMP utilisée par les dll de l’agent d’extension SNMP et les applications du gestionnaire. Cette DLL contient une infrastructure pour le développement de DLL d’agent d’extension.                                                                                   |
| SNMPSNAP.DLL | Application de configuration SNMP qui est un composant logiciel enfichable MMC (Microsoft Management Console). Le composant logiciel enfichable ajoute plusieurs pages à la feuille de propriétés du service SNMP. Pour plus d’informations, consultez l’aide en ligne du service SNMP. |
| SNMPTRAP.EXE | Service d’interruption SNMP. Reçoit des interruptions SNMP et les transfère aux applications du gestionnaire SNMP.                                                                                                                                              |
| WINSMIB.DLL  | DLL de l’agent d’extension qui implémente le MIB WINS défini par Microsoft. Installé uniquement sur les serveurs WINS.                                                                                                                                 |
| WSNMP32.DLL  | Bibliothèque de l' [API WinSNMP](winsnmp-api.md) Microsoft. Cette API permet aux applications du gestionnaire SNMP d’écouter les requêtes du gestionnaire SNMP et d’envoyer des requêtes et de recevoir des réponses des agents SNMP.                                     |



 

Pour plus d’informations, consultez [la base de données MIB (Management Information base) SNMP](the-snmp-management-information-base-mib-.md). (Vous pouvez également vous reporter au kit de ressources Windows 2000.)

 

 




