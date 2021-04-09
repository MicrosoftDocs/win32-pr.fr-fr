---
description: Les informations relatives à chaque événement sont stockées dans le journal des événements dans un enregistrement du journal des événements. L’enregistrement du journal des événements contient des informations sur l’heure, le type et la catégorie. Pour plus d’informations, consultez la structure EVENTLOGRECORD.
ms.assetid: 73731505-97f5-4985-8d00-c6ce8604902d
title: Enregistrements du journal des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cc6caf1011c06eda0dca240bb7a3478c549827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864249"
---
# <a name="event-log-records"></a><span data-ttu-id="78bc2-105">Enregistrements du journal des événements</span><span class="sxs-lookup"><span data-stu-id="78bc2-105">Event Log Records</span></span>

<span data-ttu-id="78bc2-106">Les informations relatives à chaque événement sont stockées dans le journal des événements dans un *enregistrement du journal des événements*.</span><span class="sxs-lookup"><span data-stu-id="78bc2-106">Information about each event is stored in the event log in an *event log record*.</span></span> <span data-ttu-id="78bc2-107">L’enregistrement du journal des événements contient des informations sur l’heure, le type et la catégorie.</span><span class="sxs-lookup"><span data-stu-id="78bc2-107">The event log record includes time, type, and category information.</span></span> <span data-ttu-id="78bc2-108">Pour plus d’informations, consultez la structure [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="78bc2-108">For more information, see the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure.</span></span>

<span data-ttu-id="78bc2-109">Le membre **recordNumber** de [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contient le numéro d’enregistrement de l’enregistrement du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="78bc2-109">The **RecordNumber** member of [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contains the record number for the event log record.</span></span> <span data-ttu-id="78bc2-110">Le premier enregistrement écrit dans un journal des événements est le numéro d’enregistrement 1, et les autres enregistrements sont numérotés séquentiellement.</span><span class="sxs-lookup"><span data-stu-id="78bc2-110">The very first record written to an event log is record number 1, and other records are numbered sequentially.</span></span> <span data-ttu-id="78bc2-111">Si le numéro d’enregistrement atteint ULONG \_ Max, le numéro d’enregistrement suivant est 0, pas 1 ; Toutefois, vous utilisez zéro pour Rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="78bc2-111">If the record number reaches ULONG\_MAX, the next record number will be 0, not 1; however, you use zero to seek to the record.</span></span>

<span data-ttu-id="78bc2-112">Si la valeur de registre de [rétention](eventlog-key.md) est définie sur zéro, les enregistrements d’événement sont remplacés lorsque la taille maximale du journal est atteinte.</span><span class="sxs-lookup"><span data-stu-id="78bc2-112">If the [Retention](eventlog-key.md) registry value is set to zero, the event records are overwritten when the maximum log size is reached.</span></span> <span data-ttu-id="78bc2-113">Par conséquent, l’enregistrement le plus ancien dans un journal des événements ne peut pas être le numéro 1.</span><span class="sxs-lookup"><span data-stu-id="78bc2-113">Therefore, the oldest record in an event log may not be record number 1.</span></span> <span data-ttu-id="78bc2-114">Pour identifier l’enregistrement le plus ancien dans le journal, appelez la fonction [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="78bc2-114">To identify the oldest record in the log, call the [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) function.</span></span> <span data-ttu-id="78bc2-115">Vous pouvez ensuite appeler la fonction [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) et ajouter la valeur retournée au numéro d’enregistrement le plus ancien pour déterminer l’enregistrement le plus récent.</span><span class="sxs-lookup"><span data-stu-id="78bc2-115">You can then call the [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) function and add the returned value to the oldest record number to determine the newest record.</span></span>

<span data-ttu-id="78bc2-116">Vous pouvez lire des enregistrements individuels à partir du journal des événements à l’aide de la fonction [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) .</span><span class="sxs-lookup"><span data-stu-id="78bc2-116">You can read individual records from the event log using the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function.</span></span> <span data-ttu-id="78bc2-117">Pour plus d’informations, consultez [interrogation des informations sur les événements](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="78bc2-117">For more information, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



