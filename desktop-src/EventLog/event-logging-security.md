---
description: Le journal de sécurité est conçu pour être utilisé par le système. Toutefois, les utilisateurs peuvent lire et effacer le journal de sécurité s’ils ont reçu le \_ privilège de nom de sécurité de se \_ (le &\# 0034 ; gérer le journal d’audit et de sécurité&\# 0034 ; droit d’utilisateur). Pour plus d’informations, consultez privilèges.
ms.assetid: 861be39a-012e-473b-a2d3-2a8c7ba3adaa
title: Sécurité de la journalisation des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4e2dce7318efeb6f26917bca1d6812eb32a343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524166"
---
# <a name="event-logging-security"></a>Sécurité de la journalisation des événements

Le journal de **sécurité** est conçu pour être utilisé par le système. Toutefois, les utilisateurs peuvent lire et effacer le journal de **sécurité** s’ils ont reçu le \_ privilège de nom de sécurité de se \_ (le droit d’utilisateur « gérer le journal d’audit et de sécurité »). Pour plus d’informations, consultez [privilèges](/windows/desktop/SecAuthZ/privileges).

Seule l’autorité de sécurité locale (Lsass.exe) dispose de l’autorisation d’écriture pour le journal de **sécurité** . Aucun autre compte ne peut demander ce privilège. Pour écrire un événement dans le journal de **sécurité** , utilisez la fonction [**AuthzReportSecurityEvent**](/windows/desktop/api/authz/nf-authz-authzreportsecurityevent) .

L’accès au journal des **applications** , au journal **système** et aux journaux personnalisés est limité. Le système accorde l’accès en fonction des droits d’accès accordés au compte sous lequel le thread s’exécute. Le tableau suivant indique les types d’accès requis par les fonctions d’enregistrement des événements.



| Droit d’accès                 | Description                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| \_Effacement du fichier journal \_ de Elf (0x0004) | Requis par [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga).                                                    |
| \_Lecture du fichier journal Elf \_ (0x0001)  | Requis par [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) et [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga). |
| Écriture dans le \_ fichier journal Elf \_ (0x0002) | Requis par [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea).                                        |



 

Utilisez la valeur de registre de **douane** pour configurer la sécurité du journal des **applications** , le journal **système** et les journaux personnalisés. Pour plus d’informations, consultez la page [EventLog Key](eventlog-key.md).

**Windows XP/2000 :** Le tableau suivant décrit les droits d’accès accordés pour chaque compte sur chaque journal.

| Journal             | Compte                 | Lire | Write | Effacer |
|-----------------|-------------------------|------|-------|-------|
| **Application** | Administrateurs (système) | X    | X     | X     |
|                 | Administrateurs (domaine) | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Utilisateur interactif        | X    | X     |       |
| **Système**      | Administrateurs (système) | X    | X     | X     |
|                 | Administrateurs (domaine) | X    |       | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Utilisateur interactif        | X    |       |       |
| *Personnalisée*        | Administrateurs (système) | X    | X     | X     |
|                 | Administrateurs (domaine) | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Utilisateur interactif        | X    | X     |       |



 

Pour accorder l’accès aux membres du compte invité, modifiez la valeur de Registre suivante :

**HKEY \_ LOCAL \_ ordinateur** \\ **système** \\ **CurrentControlSet** \\ **services** \\ Journal des **événements** \\  \\ **RestrictGuestAccess**

 

 
