---
description: Une application Observateur d’événements utilise la fonction OpenEventLog pour ouvrir le journal des événements pour une source d’événement.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lecture à partir du journal des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034350"
---
# <a name="reading-from-the-event-log"></a>Lecture à partir du journal des événements

Une application Observateur d’événements utilise la fonction [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) pour ouvrir le journal des événements pour une source d’événement. L’observateur d’événements peut ensuite utiliser la fonction [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) pour lire les enregistrements d’événements à partir du journal. **ReadEventLog** retourne une mémoire tampon contenant une structure [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) et des informations supplémentaires qui décrivent un événement enregistré. Le diagramme suivant illustre ce processus.

![lecture à partir du journal des événements](images/readlog.png)

Pour obtenir un exemple de code, consultez [interrogation des informations sur les événements](querying-for-event-source-messages.md).

 

 



