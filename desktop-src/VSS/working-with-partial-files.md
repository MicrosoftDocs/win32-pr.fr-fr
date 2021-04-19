---
description: Il est parfois utile de sauvegarder et de restaurer uniquement des sections de fichiers. VSS fournit des mécanismes de fichiers partiels, qui, si les demandeurs le prennent en charge, permet aux rédacteurs de spécifier des sauvegardes de fichiers partielles et des restaurations.
ms.assetid: 02b74a4e-d69f-4eeb-866a-3399598b7035
title: Utilisation de fichiers partiels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7194f01df11f6c0e368941e17ef6ab1620b17f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517273"
---
# <a name="working-with-partial-files"></a>Utilisation de fichiers partiels

Il est parfois utile de sauvegarder et de restaurer uniquement des sections de fichiers. VSS fournit des mécanismes de [*fichiers partiels*](vssgloss-p.md) , qui, si les demandeurs le prennent en charge, permet aux rédacteurs de spécifier des sauvegardes de fichiers partielles et des restaurations.

Les opérations de fichiers partielles sont souvent les plus utilisées pour les enregistreurs qui gèrent des fichiers très volumineux, mais uniquement une petite fraction de la modification entre les opérations de sauvegarde. Dans ce cas, il est souvent utile de copier uniquement la section qui a changé sur le support de sauvegarde. Pour cette raison, les opérations de fichiers partielles sont généralement, mais pas exclusivement, utilisées pour prendre en charge les opérations de sauvegarde et de restauration incrémentielles.

Si un writer souhaite implémenter une opération de fichier partielle, il utilise [**CVssWriter :: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled) pour déterminer si le demandeur avec lequel il travaille prend en charge l’opération.

Si le demandeur prend en charge les opérations de fichiers partielles et, s’il ajoute le composant qui gère le fichier (ou le composant qui définit le jeu de composants qui contient le fichier) au document des composants de sauvegarde, un writer indique les sections du fichier à enregistrer (en général, lors de la gestion d’un événement [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou [*PostSnapshot*](vssgloss-p.md) ) en appelant [**IVssComponent :: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

En plus d’un chemin d’accès et d’un nom de fichier, l’enregistreur fournit les informations de métadonnées facultatives à [**IVssComponent :: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

Les informations de plage sont fournies sous la forme d’une chaîne qui contient l’un des éléments suivants :

-   Paires d’offsets dans le fichier à sauvegarder (en octets) et longueur de la section à sauvegarder (en octets), le décalage et la longueur séparés par un signe deux-points, et chaque paire séparée par une virgule, par exemple *Offset1 ***:**_length1_*_,_* * Offset2 ***:**_length2_.

    Chaque valeur est un entier 64 bits (au format hexadécimal ou décimal) spécifiant respectivement un décalage d’octet et une longueur en octets.

-   Chemin d’accès complet, y compris le nom de fichier, sur le système actuel d’un fichier de plages binaires contenant les éléments suivants :
    -   Nombre (exprimé sous la forme d’un entier 64 bits) des différentes plages de fichiers contenues dans le fichier
    -   Chaque plage exprimée sous la forme d’une paire d’entiers 64 bits : le premier membre de la paire étant le décalage dans le fichier sauvegardé (en octets) et le deuxième membre étant la longueur des données à sauvegarder (en octets)

Si un writer utilise un fichier de plages pour spécifier une opération de fichier partielle, un demandeur doit garantir que ce fichier est sauvegardé (même si le fichier ne fait pas nécessairement partie du jeu de sauvegarde par défaut) ou que les informations de plages sont conservées sur le support de sauvegarde d’une autre façon. Si les informations du fichier de plages ne sont pas sauvegardées, il est impossible de restaurer le fichier partiellement sauvegardé.

Le writer peut également ajouter une chaîne contenant des métadonnées. Ces métadonnées peuvent être dans un format spécifique au writer, car elles sont destinées à permettre à l’enregistreur de valider toutes les restaurations ultérieures.

Avec ces informations, un demandeur de support peut effectuer une sauvegarde de fichiers partielle.

Par exemple, imaginez un fichier volumineux dont l’en-tête (octets 64-512) contient un nombre d’enregistrements et d’autres informations fréquemment mises à jour, et dont les données les plus récentes doivent être recherchées dans les 65536 derniers octets du fichier, octets 0x1239E8577A à 0x1239E7577A.

Un enregistreur peut spécifier une liste de plages comme chaîne «**64:448, 0x1239E8577A : 65536**».

Lors de la restauration, et avant l’exécution d’une opération de restauration, un demandeur doit vérifier si des fichiers nécessitent une prise en charge partielle des fichiers.

Pour ce faire, le demandeur itère d’abord sur les enregistreurs avec des composants stockés dans son document composants de sauvegarde à l’aide de [**IVssBackupComponents :: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) et [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

L’interface [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) est ensuite utilisée pour retourner des instances de l’interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) , qui fournissent [**IVssWriterComponentsExt :: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) et [**IVssWriterComponentsExt :: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount), qui permettent au demandeur d’obtenir des instances [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Cela permet à un demandeur d’obtenir des informations sur les fichiers partiellement sauvegardés afin de participer à une restauration à l’aide de [**IVssComponent :: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) et de [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) pour l’instance de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondant au composant qui gère le fichier (ou le composant qui définit le jeu de composants qui contient le fichier).

Si l’opération de fichier partielle est contrôlée par un fichier de plages, ce fichier doit être restauré avant les données copiées sur le disque. Cela peut se produire si le demandeur devait copier le fichier de plages vers un nouvel emplacement sur le disque. Dans ce cas, elle indique qu’elle s’est exécutée par le biais de [**IVssBackupComponents :: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

Le demandeur poursuit ensuite la copie des données dans les emplacements appropriés dans la destination de restauration déjà sur le disque.

Un enregistreur (lors de la gestion d’un événement [**postRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) ), en examinant [**IVssComponent :: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus) pour les fichiers indiqués par [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile), détermine si l’opération de fichier partielle a réussi. L’enregistreur doit toujours essayer de vérifier l’exactitude de cette restauration à l’aide des informations de décalage et des métadonnées incluses dans le document des composants de sauvegarde.

Si le demandeur a dû restaurer le fichier de plages à un nouvel emplacement, VSS met à jour ces informations pour que le chemin d’accès retourné par [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) soit correct.

 

 
