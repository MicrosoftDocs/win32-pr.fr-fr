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
# <a name="event-log-file-format"></a>Format du fichier journal des événements

Chaque journal des événements contient un en-tête (représenté par la structure d' [**\_ \_ en-tête du fichier de journalisation Elf**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) ) qui a une taille fixe, suivi d’un nombre variable d’enregistrements d’événements (représentés par les structures [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) ) et d’un enregistrement de fin de fichier (représenté par la structure de l' [**\_ \_ enregistrement**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) de l’aide d’Elf).

La structure d' **\_ \_ en-tête du fichier de journalisation Elf** et la structure d' **\_ \_ enregistrement du EOF Elf** sont écrites dans le journal des événements lorsque le journal des événements est créé et sont mis à jour chaque fois qu’un événement est écrit dans le journal.

Quand une application appelle la fonction [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) pour écrire une entrée dans le journal des événements, le système transmet les paramètres au service de journalisation des événements. Le service de journalisation des événements utilise les informations pour écrire une structure **EVENTLOGRECORD** dans le journal des événements. Le diagramme suivant illustre ce processus.

![écriture d’un fichier journal](images/evreport.png)

Les enregistrements d’événements sont organisés de l’une des manières suivantes :

-   Sans habillage. L’enregistrement le plus ancien est immédiatement après l’en-tête du journal des événements et les nouveaux enregistrements sont ajoutés après le dernier enregistrement ajouté (avant l' **\_ \_ enregistrement** de l’ancien EOF). L’exemple suivant illustre la méthode sans habillage :

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    La non-encapsulage peut se produire lorsque le journal des événements est créé ou lorsque le journal des événements est effacé. Le journal des événements continue d’être non encapsulé jusqu’à ce que la limite de taille du journal des événements soit atteinte. La taille du journal des événements est limitée par la valeur de configuration **MaxSize** ou par la quantité de ressources système.

    Lorsque la limite de taille du journal des événements est atteinte, elle peut commencer à inclure dans un wrapper. L’encapsulation est contrôlée par la valeur de configuration de **rétention** . Pour plus d’informations sur les valeurs de configuration du journal des événements, consultez [EventLog Key](eventlog-key.md).

-   Restrictions d'. Les enregistrements sont organisés en mémoire tampon circulaire. Au fur et à mesure de l’ajout de nouveaux enregistrements, les enregistrements les plus anciens sont remplacés. L’emplacement des enregistrements les plus anciens et les plus récents varie. L’exemple suivant illustre la méthode d’encapsulage.

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

    Dans l’exemple, l’enregistrement le plus ancien n’est plus 1, mais est 102 car l’espace des enregistrements 1 à 101 a été remplacé.

    Il y a un espace entre **l' \_ \_ enregistrement de EOF Elf** et l’enregistrement le plus ancien, car le système efface un nombre entier d’enregistrements pour libérer de l’espace pour le nouvel enregistrement. Par exemple, si l’enregistrement le plus récent est de 100 octets et que les deux enregistrements les plus anciens ont une longueur de 75 octets, le système supprime les deux enregistrements les plus anciens. Les 50 octets supplémentaires seront utilisés ultérieurement lors de l’écriture de nouveaux enregistrements.

    Un fichier journal d’événements a une taille fixe et lorsque les enregistrements du fichier sont renvoyés à la ligne, l’enregistrement à la fin du fichier est généralement divisé en deux enregistrements. Par exemple, si la position de l’écriture suivante est de 100 octets à partir de la fin du fichier et que la taille de l’enregistrement est de 300 octets, les 100 premiers octets seront écrits à la fin du fichier et les 200 octets suivants seront écrits au début du fichier immédiatement après l' **\_ \_ en-tête de fichier journal Elf**. Si l’espace disponible à la fin du fichier est inférieur à la partie fixe de **EVENTLOGRECORD** (0x38 octets), tout le nouvel enregistrement est écrit au début du fichier, immédiatement après l' **\_ \_ en-tête du fichier journal Elf**. Les octets inutilisés à la fin du fichier seront remplis avec le modèle 0x00000027.

Pour plus d’informations et pour obtenir un exemple de code, consultez [création de rapports sur un événement](reporting-an-event.md).

 

 
