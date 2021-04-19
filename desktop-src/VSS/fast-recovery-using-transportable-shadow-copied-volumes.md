---
description: Les clichés instantanés transportables peuvent être utilisés pour faciliter une récupération rapide.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Récupération rapide à l’aide de volumes de clichés instantanés transportables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524697"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Récupération rapide à l’aide de volumes de clichés instantanés transportables

Les [*clichés instantanés transportables*](vssgloss-t.md) peuvent être utilisés pour faciliter une *récupération rapide*.

La récupération rapide peut être utilisée pour revenir rapidement à un cliché instantané antérieur. Les étapes impliquées sont les suivantes :

1.  Créez le cliché instantané transportable des numéros d’unités logiques appropriés. Le cliché instantané peut être [*persistant*](vssgloss-p.md) ou non persistant.
2.  Supprimer les numéros d’unités logiques d’origine
    1.  Si l’ordinateur est à l’intérieur d’un cluster, marquez les ressources de disque affectées comme étant hors connexion ou activez le [mode de maintenance](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) pour ces ressources de disque.
    2.  Masquez les numéros d’unités logiques affectés à partir de cet ordinateur (et de tous les autres nœuds si l’ordinateur se trouve dans un cluster).
3.  Importez le cliché instantané à l’aide de la méthode [**IVssBackupComponents :: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) .
4.  Rompez le cliché instantané à l’aide de la méthode [**IVssBackupComponents :: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .
5.  Marquez les nouveaux volumes de clichés instantanés comme étant en lecture/écriture.
6.  Si l’ordinateur se trouve dans un cluster, exposez les nouveaux numéros d’unités logiques de clichés instantanés en tant que LUN d’origine.
    1.  Démasquez les numéros d’unité logique de cliché instantané aux autres nœuds du cluster.
    2.  Marquez les ressources qui étaient précédemment marquées comme étant en ligne ou désactivez le mode de maintenance pour ces ressources de disque.

> [!Note]  
> Les clichés instantanés transportables dans un cluster ne sont pas pris en charge avant Windows Server 2003 avec Service Pack 1 (SP1). Cela est uniquement pris en charge avec les numéros d’unités logiques conformes, qui ont au moins une page VPD (SCSI vital Product Data) 0x83 \_ l’identificateur de stockage de type 1, 2 ou 8, et l’Association 0, et les numéros d’unités logiques doivent gérer un disque de base avec le partitionnement MBR.

 

 

 
