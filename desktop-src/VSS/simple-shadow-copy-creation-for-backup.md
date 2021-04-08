---
description: Plusieurs types de clichés instantanés peuvent être créés par un demandeur.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Création de clichés instantanés simples pour la sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11e030c0531c96eee40e9cd5bb7cc9366284985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751029"
---
# <a name="simple-shadow-copy-creation-for-backup"></a>Création de clichés instantanés simples pour la sauvegarde

Plusieurs types de clichés instantanés peuvent être créés par un demandeur. Toutefois, pour la plupart des applications de sauvegarde, procédez comme suit :

1.  Appelez [**IVssBackupComponents :: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) avec un contexte de sauvegarde Visual SourceSafe \_ \_ .
2.  Appelez [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) pour initialiser la communication avec les enregistreurs.
3.  Appelez [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) pour ajouter des composants de fichiers et de bases de données à la sauvegarde.
4.  Appelez [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) pour initialiser le mécanisme de clichés instantanés.
5.  Appelez [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) pour inclure les volumes dans le cliché instantané.
6.  Appelez [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) pour notifier les auteurs des opérations de sauvegarde.

 

 



