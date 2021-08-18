---
description: 'Les événements d’abandon peuvent être générés au cours d’une opération de sauvegarde dans l’un des cas suivants :'
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Abandon des opérations VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120ef8fb16c23d77a24526aad0fd62e56c1888a76dc2de884140094c6591cd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998269"
---
# <a name="aborting-vss-operations"></a>Abandon des opérations VSS

Les événements d' [*abandon*](vssgloss-a.md) peuvent être générés au cours d’une opération de sauvegarde dans l’un des cas suivants :

-   Un demandeur génère explicitement un [*événement d’abandon*](vssgloss-a.md) en appelant [**IVssBackupComponents :: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).
-   Les gestionnaires d’événements [*Freeze*](vssgloss-f.md) et [*dégeler*](vssgloss-t.md) d’un enregistreur [**(CVssWriter :: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) et [**CVssWriter :: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) retournent la **valeur false** ou ne peuvent pas se terminer dans la fenêtre de temps spécifiée dans [**CVssWriter :: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize).
-   Le fournisseur ou VSS n’a pas pu être créé lors de la création d’un cliché instantané à la suite de l’événement [*PrepareForSnapshot*](vssgloss-p.md) .

Les abandons ne sont pas pris en charge pour les opérations de restauration.

## <a name="requester-handling-and-creation-of-abort-events"></a>Traitement des demandeurs et création d’événements d’abandon

Une instance de l’interface [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) peut être utilisée pour une seule sauvegarde. par conséquent, si une erreur se produit lors du traitement d’une sauvegarde, il est généralement préférable de libérer l’instance actuelle et de recommencer.

Un demandeur doit signaler explicitement qu’il abandonne une opération de sauvegarde (à l’aide de [**IVssBackupComponents :: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) uniquement après la préparation réelle d’une sauvegarde, impliquant des enregistreurs ou la création d’un cliché instantané.

Concrètement, cela signifie que chaque fois qu’un demandeur doit arrêter une opération de sauvegarde après avoir généré un événement [*PrepareForBackup*](vssgloss-p.md) en appelant [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), il doit appeler [**IVssBackupComponents :: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) et attendre son retour avant de libérer l’instance [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) actuelle.

Par exemple, si un enregistreur a refusé une opération de sauvegarde, un demandeur doit utiliser [**IVssBackupComponents :: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) pour notifier à tous les autres enregistreurs que l’opération de sauvegarde ne sera pas effectuée.

Avant d’appeler [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), ou si l’appel à **PrepareForBackup** échoue, un demandeur peut libérer l’instance actuelle de l’interface [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) sans avoir à générer un événement d’abandon.

Par exemple, si l’instance actuelle de [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) est utilisée uniquement pour obtenir des informations en appelant [**IVSSBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) et en générant un événement d' [*identification*](vssgloss-i.md) , une fois que les informations ont été retournées, l’instance de **IVSSBackupComponents** peut simplement être libérée.

Un demandeur génère un certain nombre d’événements ([*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*dégeler*](vssgloss-t.md)et [*PostSnapshot*](vssgloss-p.md)) lorsqu’il appelle [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Lors de la gestion des événements Freeze et dégeler, un enregistreur peut échouer et générer un événement d’abandon seul. L’échec de la gestion des événements PrepareForSnapshot et PostSnapshot ne génère pas d’événement d’abandon.

Il n’est pas toujours possible pour un demandeur de savoir si un événement d’abandon a été généré quand [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) indique un échec. Par conséquent, un demandeur qui doit mettre fin à une opération de sauvegarde, car l’état de **IVssBackupComponents ::D osnapshotset** indique qu’un problème doit toujours appeler [**IVssBackupComponents :: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).

Si un demandeur a appelé [**IVssBackupComponents :: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup), il n’est pas nécessaire d’appeler [**IVssBackupComponents :: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) avant de libérer une instance de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

## <a name="writer-handling-and-creation-of-abort-events"></a>Gestion de l’enregistreur et création d’événements d’abandon

Comme indiqué précédemment, un enregistreur peut recevoir un événement d’abandon d’un demandeur, ou le fournisseur peut déclencher un événement lui-même. En outre, il est possible pour un enregistreur de recevoir plusieurs événements d’abandon dans certaines circonstances. Les développeurs d’enregistreur doivent coder toute implémentation de [**CVssWriter :: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) en tenant compte de cela.

Dans le cadre de la gestion d’un événement d’abandon, un enregistreur doit tenter de restaurer le processus qu’il a géré dans son état d’exécution normal, ainsi que d’effectuer la gestion des erreurs et la journalisation.

Cela peut signifier qu’une implémentation de [**CVssWriter :: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) devra peut-être effectuer de nombreuses tâches, ou toutes, des mêmes tâches que le gestionnaire d’événements dégeler ([**CVssWriter :: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) et le gestionnaire d’événements PostSnapshot ([**CVssWriter :: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)), et ces gestionnaires peuvent être appelés à partir de **CVssWriter :: OnAbort**.

 

 



