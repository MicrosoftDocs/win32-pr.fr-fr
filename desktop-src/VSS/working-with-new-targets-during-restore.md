---
description: Un demandeur peut avoir besoin de restaurer des fichiers à un emplacement indiqué par un autre nom que le chemin d’accès par défaut d’un jeu de fichiers ou le mappage d’un autre emplacement.
ms.assetid: ce11485c-da0e-4c16-962e-eeedc2da3de4
title: Utilisation de nouvelles cibles pendant la restauration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f7b9a614b043a423dd90868b0a66b505ee194ef968daed4952b0ba60fec6b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590463"
---
# <a name="working-with-new-targets-during-restore"></a>Utilisation de nouvelles cibles pendant la restauration

Un demandeur peut avoir besoin de restaurer des fichiers à un emplacement indiqué par un autre nom que le chemin d’accès par défaut d’un jeu de fichiers ou le mappage d’un [*autre emplacement*](vssgloss-a.md). Cela peut se produire pour de nombreuses raisons : par exemple, aucune destination de restauration n’a été accessible, ou un utilisateur demandeur demande intentionnellement que les fichiers soient restaurés à un emplacement précédemment inconnu. Dans ce cas, le demandeur utilise le nouveau mécanisme cible pour indiquer aux rédacteurs qu’il a restauré un fichier vers une autre zone sur le disque.

Tous les enregistreurs ne prennent pas en charge un demandeur qui modifie la destination de restauration d’un fichier. Un demandeur doit vérifier la prise en charge de l’enregistreur en vérifiant le masque de schéma de sauvegarde du writer (retourné par [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)) et en vérifiant qu’il contient l' \_ enregistreur VSS BS qui \_ \_ prend en charge la \_ nouvelle \_ balise cible.

Le demandeur indique une telle restauration par le biais de la méthode [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) . En plus de spécifier une spécification de fichier et une destination de restauration originale et nouvelle, le demandeur spécifie les informations sur les composants, à savoir un chemin d’accès logique et un nom de composant.

Les informations sur le composant sont utilisées dépendent du fait que le composant qui gère le fichier ayant une nouvelle cible ajoutée a été [*explicitement inclus*](vssgloss-e.md) ou [*implicitement inclus*](vssgloss-i.md) dans la sauvegarde.

Si le composant de gestion a été explicitement inclus, ses informations sont utilisées. Si le composant de gestion a été inclus implicitement, il s’agit d’un sous-composant dans un jeu de composants. Dans ce cas, les informations du composant qui définissent le jeu de composants sont utilisées.

Lors du traitement de l’événement [**postRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) , les enregistreurs doivent vérifier si l’un de ses fichiers a été restauré vers un nouvel emplacement. Pour ce faire, vous pouvez utiliser les méthodes [**IVssComponent :: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) et [**IVssComponent :: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) .

L’instance de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) utilisée varie selon que le composant de gestion du fichier a été explicitement ou implicitement ajouté à la sauvegarde.

 

 



