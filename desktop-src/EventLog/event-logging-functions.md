---
description: Les fonctions suivantes sont utilisées avec la journalisation des événements.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Fonctions de journalisation des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531893"
---
# <a name="event-logging-functions"></a><span data-ttu-id="58360-103">Fonctions de journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="58360-103">Event Logging Functions</span></span>

<span data-ttu-id="58360-104">Les fonctions suivantes sont utilisées avec la journalisation des événements.</span><span class="sxs-lookup"><span data-stu-id="58360-104">The following functions are used with event logging.</span></span>



| <span data-ttu-id="58360-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="58360-105">Function</span></span>                                                         | <span data-ttu-id="58360-106">Description</span><span class="sxs-lookup"><span data-stu-id="58360-106">Description</span></span>                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58360-107">**BackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="58360-107">**BackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | <span data-ttu-id="58360-108">Enregistre le journal des événements spécifié dans un fichier de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="58360-108">Saves the specified event log to a backup file.</span></span>                                                     |
| [<span data-ttu-id="58360-109">**ClearEventLog**</span><span class="sxs-lookup"><span data-stu-id="58360-109">**ClearEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | <span data-ttu-id="58360-110">Efface le journal des événements spécifié et enregistre éventuellement la copie actuelle du journal dans un fichier de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="58360-110">Clears the specified event log, and optionally saves the current copy of the log to a backup file.</span></span>  |
| [<span data-ttu-id="58360-111">**CloseEventLog**</span><span class="sxs-lookup"><span data-stu-id="58360-111">**CloseEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | <span data-ttu-id="58360-112">Ferme un handle de lecture du journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-112">Closes a read handle to the specified event log.</span></span>                                                    |
| [<span data-ttu-id="58360-113">**DeregisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="58360-113">**DeregisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | <span data-ttu-id="58360-114">Ferme un handle d’écriture dans le journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-114">Closes a write handle to the specified event log.</span></span>                                                   |
| [<span data-ttu-id="58360-115">**GetEventLogInformation**</span><span class="sxs-lookup"><span data-stu-id="58360-115">**GetEventLogInformation**</span></span>](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | <span data-ttu-id="58360-116">Récupère des informations sur le journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-116">Retrieves information about the specified event log.</span></span>                                                |
| [<span data-ttu-id="58360-117">**GetNumberOfEventLogRecords**</span><span class="sxs-lookup"><span data-stu-id="58360-117">**GetNumberOfEventLogRecords**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | <span data-ttu-id="58360-118">Récupère le nombre d’enregistrements dans le journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-118">Retrieves the number of records in the specified event log.</span></span>                                         |
| [<span data-ttu-id="58360-119">**GetOldestEventLogRecord**</span><span class="sxs-lookup"><span data-stu-id="58360-119">**GetOldestEventLogRecord**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | <span data-ttu-id="58360-120">Récupère le numéro d’enregistrement absolu de l’enregistrement le plus ancien dans le journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-120">Retrieves the absolute record number of the oldest record in the specified event log.</span></span>               |
| [<span data-ttu-id="58360-121">**NotifyChangeEventLog**</span><span class="sxs-lookup"><span data-stu-id="58360-121">**NotifyChangeEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | <span data-ttu-id="58360-122">Permet à une application de recevoir une notification lorsqu’un événement est écrit dans le journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-122">Enables an application to receive notification when an event is written to the specified event log.</span></span> |
| [<span data-ttu-id="58360-123">**OpenBackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="58360-123">**OpenBackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | <span data-ttu-id="58360-124">Ouvre un handle vers un journal des événements de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="58360-124">Opens a handle to a backup event log.</span></span>                                                               |
| [<span data-ttu-id="58360-125">**OpenEventLog**</span><span class="sxs-lookup"><span data-stu-id="58360-125">**OpenEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | <span data-ttu-id="58360-126">Ouvre un handle vers le journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-126">Opens a handle to the specified event log.</span></span>                                                          |
| [<span data-ttu-id="58360-127">**ReadEventLog**</span><span class="sxs-lookup"><span data-stu-id="58360-127">**ReadEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | <span data-ttu-id="58360-128">Lit un nombre entier d’entrées dans le journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-128">Reads a whole number of entries from the specified event log.</span></span>                                       |
| [<span data-ttu-id="58360-129">**RegisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="58360-129">**RegisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | <span data-ttu-id="58360-130">Récupère un handle enregistré dans le journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-130">Retrieves a registered handle to the specified event log.</span></span>                                           |
| [<span data-ttu-id="58360-131">**ReportEvent**</span><span class="sxs-lookup"><span data-stu-id="58360-131">**ReportEvent**</span></span>](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | <span data-ttu-id="58360-132">Écrit une entrée à la fin du journal des événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="58360-132">Writes an entry at the end of the specified event log.</span></span>                                              |



 

 

 



