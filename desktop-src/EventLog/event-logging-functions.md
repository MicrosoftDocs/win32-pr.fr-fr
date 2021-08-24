---
description: Les fonctions suivantes sont utilisées avec la journalisation des événements.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Fonctions de journalisation des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6ba5e43286a65b9d3456edc9cd80e8812bd9a32975ec63158c0717b41c6894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069589"
---
# <a name="event-logging-functions"></a>Fonctions de journalisation des événements

Les fonctions suivantes sont utilisées avec la journalisation des événements.



| Fonction                                                         | Description                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | Enregistre le journal des événements spécifié dans un fichier de sauvegarde.                                                     |
| [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | Efface le journal des événements spécifié et enregistre éventuellement la copie actuelle du journal dans un fichier de sauvegarde.  |
| [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | Ferme un handle de lecture du journal des événements spécifié.                                                    |
| [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | Ferme un handle d’écriture dans le journal des événements spécifié.                                                   |
| [**GetEventLogInformation**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | Récupère des informations sur le journal des événements spécifié.                                                |
| [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | Récupère le nombre d’enregistrements dans le journal des événements spécifié.                                         |
| [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | Récupère le numéro d’enregistrement absolu de l’enregistrement le plus ancien dans le journal des événements spécifié.               |
| [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | Permet à une application de recevoir une notification lorsqu’un événement est écrit dans le journal des événements spécifié. |
| [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | Ouvre un handle vers un journal des événements de sauvegarde.                                                               |
| [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | Ouvre un handle vers le journal des événements spécifié.                                                          |
| [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | Lit un nombre entier d’entrées dans le journal des événements spécifié.                                       |
| [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | Récupère un handle enregistré dans le journal des événements spécifié.                                           |
| [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | Écrit une entrée à la fin du journal des événements spécifié.                                              |



 

 

 



