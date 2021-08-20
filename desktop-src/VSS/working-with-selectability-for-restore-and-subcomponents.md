---
description: La sélectivité pour la restauration permet au demandeur de déterminer quand un composant peut être restauré individuellement.
ms.assetid: 684dc50f-5d7b-4c95-85dd-77c320d65fff
title: Utilisation de la sélectivité pour la restauration et les sous-composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1186c9517af8e7e7b914b9508e10a2b4c8d1961afdbf6d68c2dadcede58c4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937380"
---
# <a name="working-with-selectability-for-restore-and-subcomponents"></a>Utilisation de la sélectivité pour la restauration et les sous-composants

La sélectivité pour la restauration permet au demandeur de déterminer quand un composant peut être restauré individuellement. Un composant qui a été inclus pour la sauvegarde peut apparaître de l’une des deux manières suivantes :

-   Un composant a peut-être été [*explicitement inclus*](vssgloss-e.md) dans la sauvegarde. Ces composants ont une instance [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondante dans le document composants de sauvegarde. Ces composants sont inclus dans une restauration à l’aide de [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).
-   Un composant a peut-être été [*implicitement inclus*](vssgloss-i.md) dans la sauvegarde. Ces composants n’ont pas d’instance [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondante dans le document des composants de sauvegarde ; Toutefois, il y aura toujours une instance **IVssComponent** pour un composant ancêtre dans le document. Ces composants sont inclus dans une restauration à l’aide de [**IVssBackupComponents :: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Tout composant qui a été explicitement inclus dans la sauvegarde peut toujours être sélectionné individuellement pour la restauration, quelle que soit sa valeur de sélectivité-for-Restore. Le demandeur appelle [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), en passant l’ID d’enregistreur, le chemin d’accès logique et le nom du composant spécifique. Les composants qui ont été implicitement inclus dans la sauvegarde sont restaurés lorsqu’un ancêtre explicitement inclus est restauré. Les composants inclus implicitement peuvent être sélectionnés individuellement pour la restauration uniquement s’ils sont marqués comme sélectionnables pour la restauration. Le demandeur appelle d’abord **IVssBackupComponents :: SetSelectedForRestore** sur le composant ancêtre le plus proche inclus, puis il appelle [**IVssBackupComponents :: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) sur le composant ancêtre pour sélectionner le composant inclus implicitement pour la restauration. Une fois cette opération effectuée, seul le composant sélectionné implicitement sera restauré. tous les autres composants du jeu de composants ne seront pas restaurés.

Contrairement à la sélectivité pour la sauvegarde, qui doit toujours être définie explicitement lorsqu’un composant est ajouté avec [**IVssCreateWriterMetadata :: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), la sélectivité de RESTORE a une valeur par défaut false, qui peut être remplacée.

Étant donné que les composants de niveau supérieur (composants avec un chemin logique vide) peuvent uniquement être inclus explicitement dans une sauvegarde, la sélectivité pour la restauration n’a aucune signification pour ces composants.

 

 



