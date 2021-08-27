---
description: Les demandeurs ont la responsabilité principale du cycle de vie d’un document sur les composants de sauvegarde.
ms.assetid: 287b7b9a-ac04-4a74-83c1-2cdd4a571ac1
title: Cycle de vie des documents des composants de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4804625f979e0d5621d96a2230c1419354d0dbeb4c368312dbd3943e0ac0c4bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124529"
---
# <a name="backup-components-document-life-cycle"></a>Cycle de vie des documents des composants de sauvegarde

Les demandeurs ont la responsabilité principale du cycle de vie d’un document sur les composants de sauvegarde.

Ce contrôle est exercé par une instance de l’objet d’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) retourné par [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents).

Un demandeur doit initialiser un document de composants de sauvegarde avant une sauvegarde ou une restauration en appelant [**IVssBackupComponents :: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) ou [**IVssBackupComponents :: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore). Le demandeur peut initialiser le document comme vide ou il peut charger une copie précédemment stockée du document.

Pour les opérations de sauvegarde, un document de composants de sauvegarde est généralement initialisé comme vide. Ses données seront remplies avec la collaboration des rédacteurs du système au cours du traitement de la sauvegarde.

Pour les opérations de restauration, un document composants de sauvegarde est généralement initialisé à partir d’un document stocké généré au cours de la sauvegarde initiale. Cela permet à la restauration (conjointement avec l’examen des documents de métadonnées de l’enregistreur stocké) de déterminer quelles données ont été initialement sauvegardées et comment elles doivent être restaurées.

La sauvegarde des [*clichés instantanés transportables*](vssgloss-t.md) est une exception à cette règle. Dans ce cas, un cliché instantané peut avoir été déplacé d’un système (où il a été créé avec le document des composants de la sauvegarde initiale) vers un autre au moyen de réassigner l’unité logique d’un périphérique de stockage partagé. Pour sauvegarder dans ces circonstances, un demandeur charge l’état de sauvegarde stocké et se poursuit là où le système initial s’est arrêté. (Pour plus d’informations, consultez [importation de volumes de clichés instantanés transportables](importing-transportable-shadow-copied-volumes.md).)

Au cours du traitement d’une sauvegarde, le demandeur décide quels composants doivent être copiés sur la base des composants marqués comme [*sélectionnables pour la sauvegarde*](vssgloss-s.md), les [*chemins logiques*](vssgloss-l.md)du composant et sa propre logique interne.

Certains des composants seront [*inclus explicitement*](vssgloss-e.md) dans l’opération de sauvegarde ; des informations sur le composant seront ajoutées au document composants de sauvegarde. D’autres seront [*incluses implicitement*](vssgloss-i.md) dans la sauvegarde. les informations sur les composants ajoutés ne sont pas ajoutées au document composants de sauvegarde.

Tous les composants d’un enregistreur non sélectionnables pour les composants de sauvegarde sans ancêtre sélectionnable dans leur chemin logique, et ceux sélectionnables pour les composants de sauvegarde choisis par le demandeur, seront ajoutés de manière explicite.

Les composants non sélectionnables et sélectionnables pour les composants de sauvegarde peuvent être ajoutés implicitement s’ils ont un ancêtre sélectionnable dans leur chemin logique, qui est explicitement inclus dans la sauvegarde. Ces composants (sous-[*composants*](vssgloss-s.md)) sont des membres de [*jeux de composants*](vssgloss-s.md) définis par leur ancêtre sélectionnable.

Lors du traitement des opérations de restauration, le demandeur utilise la [*sélectivité pour la restauration*](vssgloss-s.md) au lieu de la possibilité de sélection pour la sauvegarde, conjointement avec les informations de chemin d’accès logique et sa propre logique interne pour déterminer les fichiers à restaurer.

Si un composant qui avait été implicitement ajouté à la sauvegarde est à présent explicitement ajouté à la restauration, le demandeur met à jour le document des composants de sauvegarde avec les informations de ce composant.

Les informations sur les composants stockés sont disponibles à la fois pour les demandeurs et les Writers via des instances de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

C’est par le biais des interfaces [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que les rédacteurs peuvent interroger et (jusqu’à la fin des événements [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) et [**postRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) ) modifier les informations dans le document des composants de sauvegarde.

Quand le gestionnaire d’événements [**CVssWriter :: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), [**CVssWriter :: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore), [**CVssWriter :: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot), [**CVssWriter :: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete)ou [**CVssWriter :: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) est appelé, un writer reçoit une instance d’une interface [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) .

Notez que, lors de la génération de l’événement [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , le document composants de sauvegarde est en lecture seule et, par conséquent, [**CVssWriter :: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) ne peut pas utiliser l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) pour le modifier.

À partir de l’interface [**IVSSWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) , l’enregistreur peut récupérer des instances de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) qui lui permettra d’accéder à tous ses composants explicitement ajoutés au document des composants de sauvegarde et à modifier leur état. Pour plus d’informations, consultez [vue d’ensemble du traitement d’une sauvegarde sous VSS](overview-of-processing-a-backup-under-vss.md) et [vue d’ensemble du traitement d’une restauration sous VSS](overview-of-processing-a-restore-under-vss.md).

Les documents des composants de sauvegarde sont supprimés de la mémoire lors de la libération de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , et doivent être stockés à l’aide de [**IVssBackupComponents :: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml), ou toutes leurs informations seront perdues.

En outre, lorsqu’un document [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) est correctement libéré, un événement [**BackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) est généré et des [*clichés instantanés de mise en sortie automatique*](vssgloss-a.md) sont supprimés.

 

 



