---
description: 'Un demandeur peut arrêter un jeu de clichés instantanés à l’aide de la méthode IVssBackupComponents :: BreakSnapshotSet ou IVssBackupComponentsEx2 :: BreakSnapshotSetEx.'
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Interruption de clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee7a17a77bb806bc6e3713c00c9a01b9bc583f56822b9940b0fe2afebb4e7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032899"
---
# <a name="breaking-shadow-copies"></a>Interruption de clichés instantanés

Un demandeur peut arrêter un jeu de clichés instantanés à l’aide de la méthode [**IVssBackupComponents :: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) ou [**IVssBackupComponentsEx2 :: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) .

Un cliché instantané endommagé est un volume qui contient un cliché instantané qui n’est plus géré par VSS. Le fait de rompre le cliché instantané n’a une signification que si le [*fournisseur*](vssgloss-p.md) du cliché instantané est un [*fournisseur de matériel*](vssgloss-h.md). Cela est dû au fait que seuls les fournisseurs de matériel peuvent implémenter un cliché instantané comme volume réel avec un cycle de vie indépendant de VSS. Si VSS ne gère pas ce type de volume, il est toujours disponible.

Les fournisseurs de logiciels maintiennent les clichés instantanés uniquement lorsqu’ils sont impliqués dans les opérations VSS. Pour cette raison, le fait de rompre le cliché instantané n’a aucune signification pour les fournisseurs de logiciels.

Si le cliché instantané a été géré par un fournisseur de matériel, le demandeur doit importer le cliché instantané avant d’appeler [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) ou [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex). En cas de clichés instantanés non transportables (créés par un fournisseur de matériel), ils sont importés implicitement dans le cadre de l’appel de [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .

Une fois que le demandeur a appelé [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) ou [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex), le jeu de clichés instantanés est toujours accessible via ses objets Device ou d’autres chemins d’accès, mais il n’est plus un jeu de clichés instantanés. Il peut être géré comme un ou plusieurs numéros d’unités logiques à l’aide des interfaces COM VDS (Virtual Disk Service). À l’aide de VDS, un demandeur peut convertir les numéros d’unités logiques en lecture/écriture, les monter avec des lettres de lecteur ou les masquer/les démasquer sur d’autres ordinateurs. Pour plus d’informations, consultez la documentation de l' [API VDS](../vds/virtual-disk-service-portal.md) .

 

 
