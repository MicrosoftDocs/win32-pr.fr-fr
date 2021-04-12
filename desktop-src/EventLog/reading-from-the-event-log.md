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
# <a name="reading-from-the-event-log"></a><span data-ttu-id="6bdec-103">Lecture à partir du journal des événements</span><span class="sxs-lookup"><span data-stu-id="6bdec-103">Reading from the Event Log</span></span>

<span data-ttu-id="6bdec-104">Une application Observateur d’événements utilise la fonction [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) pour ouvrir le journal des événements pour une source d’événement.</span><span class="sxs-lookup"><span data-stu-id="6bdec-104">An event viewer application uses the [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to open the event log for an event source.</span></span> <span data-ttu-id="6bdec-105">L’observateur d’événements peut ensuite utiliser la fonction [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) pour lire les enregistrements d’événements à partir du journal.</span><span class="sxs-lookup"><span data-stu-id="6bdec-105">The event viewer can then use the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to read event records from the log.</span></span> <span data-ttu-id="6bdec-106">**ReadEventLog** retourne une mémoire tampon contenant une structure [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) et des informations supplémentaires qui décrivent un événement enregistré.</span><span class="sxs-lookup"><span data-stu-id="6bdec-106">**ReadEventLog** returns a buffer containing an [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure and additional information that describes a logged event.</span></span> <span data-ttu-id="6bdec-107">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="6bdec-107">The following diagram illustrates this process.</span></span>

![lecture à partir du journal des événements](images/readlog.png)

<span data-ttu-id="6bdec-109">Pour obtenir un exemple de code, consultez [interrogation des informations sur les événements](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="6bdec-109">For example code, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



