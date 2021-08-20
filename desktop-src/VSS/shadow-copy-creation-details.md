---
description: En général, la création d’un cliché instantané dépend du type de cliché instantané à créer, de son contexte et du rôle accordé aux rédacteurs dans l’opération de cliché instantané.
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: Détails de la création de clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d8f506ef8d5c7acff86cb6a2fa890b3773423fddf339ea4911a0299963224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998129"
---
# <a name="shadow-copy-creation-details"></a>Détails de la création de clichés instantanés

En général, la création d’un cliché instantané dépend du type de cliché instantané à créer, de son contexte et du rôle accordé aux rédacteurs dans l’opération de cliché instantané. (Pour plus d’informations, consultez [configurations du contexte de cliché instantané](shadow-copy-context-configurations.md) .)

Le contexte de cliché instantané est défini en appelant la méthode [**IVssBackupComponents :: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) . Avant d’appeler la méthode [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) pour créer un cliché instantané, les demandeurs doivent appeler les méthodes [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) dans l’ordre spécifié dans les sections suivantes.

## <a name="prerequisites-for-all-shadow-copies"></a>Conditions préalables pour tous les clichés instantanés

Quel que soit le niveau de participation du writer, la création d’un cliché instantané requiert toujours l’initialisation du demandeur avec les appels à [**IVssBackupComponents :: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) et [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Si cet appel n’est pas effectué, la méthode [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) renvoie une erreur.

## <a name="shadow-copies-with-writer-participation"></a>Clichés instantanés avec participation au rédacteur

Si le contexte de cliché instantané spécifie la participation de l’enregistreur (c’est-à-dire que [**IVssBackupComponents :: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) est appelé avec la **\_ \_ sauvegarde VSS CTX**, ou la restauration de l' **\_ \_ application \_ VSS CTX**) :

-   Les demandeurs doivent toujours appeler [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) lorsque le contexte de cliché instantané prend en charge la participation de l’enregistreur. Si le contexte de cliché instantané prend en charge la participation de l’enregistreur et **IVssBackupComponents :: GatherWriterMetadata** n’est pas appelé avant [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), une erreur est retournée.
-   Si un demandeur souhaite sélectionner des composants d’enregistreur spécifiques, il doit appeler [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) avant d’appeler [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) pour créer le jeu de clichés instantanés.
-   [**StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) doit être appelé pour créer le jeu de clichés instantanés.
-   Les demandeurs peuvent ajouter un ou plusieurs volumes au jeu de clichés instantanés en appelant [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). Certains composants de l’enregistreur peuvent ne pas spécifier de volumes affectés. Dans ce cas, il est acceptable qu’un instantané soit vide (c’est-à-dire qu’il ne contienne aucun volume).
-   Pour garantir la cohérence des métadonnées de l’enregistreur, un demandeur doit toujours appeler [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) même si aucun composant n’est sélectionné. VSS génère alors un événement **PrepareForBackup** , dans lequel VSS appelle la méthode [**CVssWriter :: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) pour chaque rédacteur participant.
-   VSS génère [*PrepareForSnapshot*](vssgloss-p.md) et [*fige*](vssgloss-f.md) les événements avant de créer le cliché instantané en réponse à [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Les enregistreurs vont gérer les événements avec [**CVssWriter :: OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) et [**CVssWriter :: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze).
-   VSS génère des événements de [*libération*](vssgloss-t.md) et des événements [*PostSnapshot*](vssgloss-p.md) après la création d’un cliché instantané en réponse à [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Les enregistreurs vont gérer les événements avec [**CVssWriter :: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) et [**CVssWriter :: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot).

## <a name="shadow-copies-without-writer-participation"></a>Clichés instantanés sans participation au rédacteur

La création de clichés instantanés sans participation à l’écriture est déconseillée pour les applications de sauvegarde standard (voir [sauvegardes sans participation](backups-without-writer-participation.md)de l’enregistreur).

Il existe des utilisations, telles que des sauvegardes rapides d’un disque, pour fournir un filet de sécurité contre les dommages accidentels de fichiers, ce qui peut être effectué sans participation explicite du writer. Ce cliché instantané aurait un contexte de **sauvegarde de partage de \_ \_ fichiers CTX \_ \_ VSS** ou de **\_ \_ \_ restauration du NAS CTX VSS**.

Pour ce type de cliché instantané, notez les points suivants :

-   Les demandeurs doivent toujours appeler les méthodes requises indiquées dans [conditions préalables pour tous les clichés instantanés](#prerequisites-for-all-shadow-copies).
-   Les demandeurs peuvent appeler [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), mais cela n’est pas obligatoire.
-   Si les demandeurs appellent [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent), [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)ou [**IVssBackupComponents :: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete), une erreur est retournée.
-   Les fournisseurs ne génèrent pas d’événements [*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*dégeler*](vssgloss-t.md)ou [*PostSnapshot*](vssgloss-p.md) pour ce type de cliché instantané.

 

 



