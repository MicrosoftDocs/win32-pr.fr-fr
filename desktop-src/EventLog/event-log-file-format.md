---
description: Chaque journal des événements contient un en-tête (représenté par la \_ structure d’en-tête du fichier de journalisation Elf \_ ) qui a une taille fixe, suivi d’un nombre variable d’enregistrements d’événements (représentés par les structures EVENTLOGRECORD) et d’un enregistrement de fin de fichier (représenté par la structure de l’enregistrement de l’aide d’Elf \_ \_ ).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Format du fichier journal des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4ba5c8bc0114e319107272e706801544e3effa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528750"
---
# <a name="event-log-file-format"></a><span data-ttu-id="c0ead-103">Format du fichier journal des événements</span><span class="sxs-lookup"><span data-stu-id="c0ead-103">Event Log File Format</span></span>

<span data-ttu-id="c0ead-104">Chaque journal des événements contient un en-tête (représenté par la structure d' [**\_ \_ en-tête du fichier de journalisation Elf**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) ) qui a une taille fixe, suivi d’un nombre variable d’enregistrements d’événements (représentés par les structures [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) ) et d’un enregistrement de fin de fichier (représenté par la structure de l' [**\_ \_ enregistrement**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) de l’aide d’Elf).</span><span class="sxs-lookup"><span data-stu-id="c0ead-104">Each event log contains a header (represented by the [**ELF\_LOGFILE\_HEADER**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) structure) that has a fixed size, followed by a variable number of event records (represented by [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) structures), and an end-of-file record (represented by the [**ELF\_EOF\_RECORD**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) structure).</span></span>

<span data-ttu-id="c0ead-105">La structure d' **\_ \_ en-tête du fichier de journalisation Elf** et la structure d' **\_ \_ enregistrement du EOF Elf** sont écrites dans le journal des événements lorsque le journal des événements est créé et sont mis à jour chaque fois qu’un événement est écrit dans le journal.</span><span class="sxs-lookup"><span data-stu-id="c0ead-105">The **ELF\_LOGFILE\_HEADER** structure and the **ELF\_EOF\_RECORD** structure are written in the event log when the event log is created and are updated each time an event is written to the log.</span></span>

<span data-ttu-id="c0ead-106">Quand une application appelle la fonction [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) pour écrire une entrée dans le journal des événements, le système transmet les paramètres au service de journalisation des événements.</span><span class="sxs-lookup"><span data-stu-id="c0ead-106">When an application calls the [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) function to write an entry to the event log, the system passes the parameters to the event-logging service.</span></span> <span data-ttu-id="c0ead-107">Le service de journalisation des événements utilise les informations pour écrire une structure **EVENTLOGRECORD** dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="c0ead-107">The event-logging service uses the information to write an **EVENTLOGRECORD** structure to the event log.</span></span> <span data-ttu-id="c0ead-108">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="c0ead-108">The following diagram illustrates this process.</span></span>

![écriture d’un fichier journal](images/evreport.png)

<span data-ttu-id="c0ead-110">Les enregistrements d’événements sont organisés de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0ead-110">The event records are organized in one of the following ways:</span></span>

-   <span data-ttu-id="c0ead-111">Sans habillage.</span><span class="sxs-lookup"><span data-stu-id="c0ead-111">Non-wrapping.</span></span> <span data-ttu-id="c0ead-112">L’enregistrement le plus ancien est immédiatement après l’en-tête du journal des événements et les nouveaux enregistrements sont ajoutés après le dernier enregistrement ajouté (avant l' **\_ \_ enregistrement** de l’ancien EOF).</span><span class="sxs-lookup"><span data-stu-id="c0ead-112">The oldest record is immediately after the event log header and new records are added after the last record that was added (before the **ELF\_EOF\_RECORD**).</span></span> <span data-ttu-id="c0ead-113">L’exemple suivant illustre la méthode sans habillage :</span><span class="sxs-lookup"><span data-stu-id="c0ead-113">The following example shows the non-wrapping method:</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    <span data-ttu-id="c0ead-114">La non-encapsulage peut se produire lorsque le journal des événements est créé ou lorsque le journal des événements est effacé.</span><span class="sxs-lookup"><span data-stu-id="c0ead-114">Non-wrapping can occur when the event log is created or when the event log is cleared.</span></span> <span data-ttu-id="c0ead-115">Le journal des événements continue d’être non encapsulé jusqu’à ce que la limite de taille du journal des événements soit atteinte.</span><span class="sxs-lookup"><span data-stu-id="c0ead-115">The event log continues to be non-wrapping until the event log size limit is reached.</span></span> <span data-ttu-id="c0ead-116">La taille du journal des événements est limitée par la valeur de configuration **MaxSize** ou par la quantité de ressources système.</span><span class="sxs-lookup"><span data-stu-id="c0ead-116">The event log size is limited by either the **MaxSize** configuration value or the amount of system resources.</span></span>

    <span data-ttu-id="c0ead-117">Lorsque la limite de taille du journal des événements est atteinte, elle peut commencer à inclure dans un wrapper.</span><span class="sxs-lookup"><span data-stu-id="c0ead-117">When the event log size limit is reached, it might start wrapping.</span></span> <span data-ttu-id="c0ead-118">L’encapsulation est contrôlée par la valeur de configuration de **rétention** .</span><span class="sxs-lookup"><span data-stu-id="c0ead-118">Wrapping is controlled by the **Retention** configuration value.</span></span> <span data-ttu-id="c0ead-119">Pour plus d’informations sur les valeurs de configuration du journal des événements, consultez [EventLog Key](eventlog-key.md).</span><span class="sxs-lookup"><span data-stu-id="c0ead-119">For more information about the event log configuration values, see [Eventlog Key](eventlog-key.md).</span></span>

-   <span data-ttu-id="c0ead-120">Restrictions d'.</span><span class="sxs-lookup"><span data-stu-id="c0ead-120">Wrapping.</span></span> <span data-ttu-id="c0ead-121">Les enregistrements sont organisés en mémoire tampon circulaire.</span><span class="sxs-lookup"><span data-stu-id="c0ead-121">The records are organized as a circular buffer.</span></span> <span data-ttu-id="c0ead-122">Au fur et à mesure de l’ajout de nouveaux enregistrements, les enregistrements les plus anciens sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="c0ead-122">As new records are added, the oldest records are replaced.</span></span> <span data-ttu-id="c0ead-123">L’emplacement des enregistrements les plus anciens et les plus récents varie.</span><span class="sxs-lookup"><span data-stu-id="c0ead-123">The location of the oldest and newest records will vary.</span></span> <span data-ttu-id="c0ead-124">L’exemple suivant illustre la méthode d’encapsulage.</span><span class="sxs-lookup"><span data-stu-id="c0ead-124">The following example shows the wrapping method.</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    EVENT RECORD 301         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 400         (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    Wasted space
    EVENT RECORD 102         (EVENTLOGRECORD)
    EVENT RECORD 103         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 299         (EVENTLOGRECORD)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    ```

    <span data-ttu-id="c0ead-125">Dans l’exemple, l’enregistrement le plus ancien n’est plus 1, mais est 102 car l’espace des enregistrements 1 à 101 a été remplacé.</span><span class="sxs-lookup"><span data-stu-id="c0ead-125">In the example the oldest record is no longer 1, but is 102 because the space for records 1 to 101 was overwritten.</span></span>

    <span data-ttu-id="c0ead-126">Il y a un espace entre **l' \_ \_ enregistrement de EOF Elf** et l’enregistrement le plus ancien, car le système efface un nombre entier d’enregistrements pour libérer de l’espace pour le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c0ead-126">There is some space between the **ELF\_EOF\_RECORD** and the oldest record because the system will erase an integral number of records to free space for the newest record.</span></span> <span data-ttu-id="c0ead-127">Par exemple, si l’enregistrement le plus récent est de 100 octets et que les deux enregistrements les plus anciens ont une longueur de 75 octets, le système supprime les deux enregistrements les plus anciens.</span><span class="sxs-lookup"><span data-stu-id="c0ead-127">For example, if the newest record is 100 bytes long and the two oldest records are 75 bytes long, then the system will remove the two oldest records.</span></span> <span data-ttu-id="c0ead-128">Les 50 octets supplémentaires seront utilisés ultérieurement lors de l’écriture de nouveaux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c0ead-128">The extra 50 bytes will be used later when new records are written.</span></span>

    <span data-ttu-id="c0ead-129">Un fichier journal d’événements a une taille fixe et lorsque les enregistrements du fichier sont renvoyés à la ligne, l’enregistrement à la fin du fichier est généralement divisé en deux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c0ead-129">An event log file has a fixed size and when the records in the file wrap, the record at the end of the file will typically be split into two records.</span></span> <span data-ttu-id="c0ead-130">Par exemple, si la position de l’écriture suivante est de 100 octets à partir de la fin du fichier et que la taille de l’enregistrement est de 300 octets, les 100 premiers octets seront écrits à la fin du fichier et les 200 octets suivants seront écrits au début du fichier immédiatement après l' **\_ \_ en-tête de fichier journal Elf**.</span><span class="sxs-lookup"><span data-stu-id="c0ead-130">For example, if the position for the next write is 100 bytes from the end of the file and the size of the record is 300 bytes, the first 100 bytes will be written at the end of the file and the next 200 bytes will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="c0ead-131">Si l’espace disponible à la fin du fichier est inférieur à la partie fixe de **EVENTLOGRECORD** (0x38 octets), tout le nouvel enregistrement est écrit au début du fichier, immédiatement après l' **\_ \_ en-tête du fichier journal Elf**.</span><span class="sxs-lookup"><span data-stu-id="c0ead-131">If the available space at the end of the file is less than the fixed portion of the **EVENTLOGRECORD** (0x38 bytes), all of the new record will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="c0ead-132">Les octets inutilisés à la fin du fichier seront remplis avec le modèle 0x00000027.</span><span class="sxs-lookup"><span data-stu-id="c0ead-132">The unused bytes at the end of the file will be filled with the pattern 0x00000027.</span></span>

<span data-ttu-id="c0ead-133">Pour plus d’informations et pour obtenir un exemple de code, consultez [création de rapports sur un événement](reporting-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="c0ead-133">For more information and a code example, see [Reporting an Event](reporting-an-event.md).</span></span>

 

 
