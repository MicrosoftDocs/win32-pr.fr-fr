---
description: Les fonctions OpenEventLog, OpenBackupEventLog, RegisterEventSource, DeregisterEventSource et CloseEventLog ouvrent et ferment les handles du journal des événements.
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: Opérations de journalisation des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065acd268788de8c9674baa1fe47a3b89a719d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519651"
---
# <a name="event-logging-operations"></a>Opérations de journalisation des événements

Les fonctions [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga), [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga), [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea), [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)et [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) ouvrent et ferment les handles du journal des événements.

Le tableau suivant présente les opérations qui peuvent être effectuées sur un journal des événements ouvert et la fonction correspondante pour chaque opération.



| Opération | Fonction                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| Sauvegarde    | [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| Effacer     | [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| Superviser   | [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| Requête     | [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord), [ **GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) |
| Lire      | [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| Write     | [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

Les fonctions [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) et [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) prennent un nom de serveur facultatif en tant que paramètre, de sorte que les opérations peuvent être effectuées sur le serveur distant. Utilisez [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) pour la lecture ou l’exécution d’opérations d’administration (sauvegarde, effacement, surveillance et interrogation) dans le journal, et utilisez [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) pour l’écriture dans le journal.

Chaque appel à une fonction d’enregistrement des événements est une opération atomique. Lorsque vous lisez à partir du journal des événements, seuls les enregistrements d’événements entiers sont retournés. Lorsque vous écrivez dans le journal des événements, chaque enregistrement d’événement est systématiquement écrit comme un enregistrement complet dans le journal. La liste suivante décrit comment le service de journalisation des événements gère les conditions spéciales :

-   Le service de journalisation des événements reçoit une opération de lecture et une opération d’écriture en même temps : si la position de lecture se trouve à la fin du fichier, l’opération de lecture échoue avec l’état de fin de fichier (si l’opération d’écriture n’est pas terminée) ou retourne le nouvel enregistrement (si l’opération d’écriture est terminée).
-   Le service de journalisation des événements effectue une opération d’effacement avant de recevoir une opération de lecture : l’opération de lecture échoue avec l’État « fin de fichier ».
-   Le service de journalisation des événements effectue une opération d’effacement avant de recevoir une opération d’écriture : l’opération Clear tronque le journal, puis l’opération d’écriture ajoute le nouvel enregistrement au début du journal.

 

 



