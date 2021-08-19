---
description: Une application Observateur d’événements utilise la fonction OpenEventLog pour ouvrir le journal des événements pour une source d’événement.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lecture à partir du journal des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d0756ba7d9609bca285ce33d69738984badf7effff8867fc5c3e1943b09145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151533"
---
# <a name="reading-from-the-event-log"></a>Lecture à partir du journal des événements

Une application Observateur d’événements utilise la fonction [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) pour ouvrir le journal des événements pour une source d’événement. L’observateur d’événements peut ensuite utiliser la fonction [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) pour lire les enregistrements d’événements à partir du journal. **ReadEventLog** retourne une mémoire tampon contenant une structure [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) et des informations supplémentaires qui décrivent un événement enregistré. Le diagramme suivant illustre ce processus.

![lecture à partir du journal des événements](images/readlog.png)

Pour obtenir un exemple de code, consultez [interrogation des informations sur les événements](querying-for-event-source-messages.md).

 

 



