---
description: Un enregistreur peut échouer pour de nombreuses raisons de programmation.
ms.assetid: 50eced73-3917-4d7e-96cc-2d793b448738
title: Erreurs d’écriture et veto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c24c15ad10766fc6ec395ed058ab3cb72a689d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201452"
---
# <a name="writer-errors-and-vetoes"></a>Erreurs d’écriture et veto

Un enregistreur peut échouer pour de nombreuses raisons de programmation. Dans ce cas, l’opération de sauvegarde, de restauration ou de cliché instantané en cours doit être refusée en appelant la méthode [**CVssWriter :: SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure) dans l’une de ses méthodes de gestionnaire (par exemple, [**CVssWriter :: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) ou [**CVssWriter :: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) et en retournant **true**. Elle peut également définir éventuellement une chaîne de message d’erreur en réponse à une condition d’échec dans certaines méthodes de gestionnaire avec les méthodes [**IVssComponentEx :: SetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg), [**IVssComponentEx :: SetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg), [**IVssComponent :: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)et [**IVssComponent :: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) . Le demandeur peut accepter le veto ou poursuivre la sauvegarde, en ignorant le veto.

Un demandeur doit vérifier l’état de l’enregistreur (à l’aide de [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) et [**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)) après chaque événement qu’il génère.

Dans certains cas, les messages d’erreur peuvent être récupérés à partir de ces échecs (à l’aide des méthodes [**IVssComponentEx :: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg), [**IVssComponent :: GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**IVssComponentEx :: GetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg)et [**IVssComponent :: GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) ), ou un enregistreur peut choisir de définir des métadonnées (à l’aide de [**IVssComponent :: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata) et [**IVssComponent :: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) avec les informations d’état d’erreur). Pour obtenir un exemple de code qui montre comment afficher ces messages d’erreur, consultez [**IVssComponentEx :: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).

Selon l’état d’erreur, un demandeur ou son opérateur peut redémarrer la sauvegarde et le cliché instantané avec toute modification nécessaire à l’état du travail ou du système de sauvegarde.

Par exemple, supposons que [**GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) a retourné ce qui suit :

-   Service **VSS \_ E \_ WRITERERROR \_ INCONSISTENTSNAPSHOT** suggère qu’un demandeur peut ajouter des volumes supplémentaires au cliché instantané
-   Service **VSS \_ E \_ WRITERERROR \_ renouvelable** indique que toute nouvelle tentative sans reconfiguration peut fonctionner. Si le writer continue à retourner l’erreur après plusieurs tentatives, essayez de redémarrer le service qui héberge l’enregistreur. Les Writers suivants sont hébergés dans le service VSS : Registry Writer, éditeur de base de données d’inscription de classe COM+, enregistreur d’optimisation de cliché instantané et Enregistreur ASR (Automated System Recovery). Si le writer appartient à une application qui héberge l’enregistreur dans son propre processus, essayez de redémarrer l’application.

    **Windows Server 2003 et Windows XP :** Les enregistreurs suivants sont hébergés dans le service VSS : Registry Writer, l’enregistreur de base de données d’inscription de classe COM+, l’enregistreur des journaux des événements d’application et l’enregistreur Microsoft SQL Server 2000 Desktop Engine (MSDE).

-   \_ \_ L’état de l’enregistreur VSS E \_ \_ non \_ disponible indique qu’un enregistreur a peut-être atteint le nombre maximal de sessions de sauvegarde et de restauration disponibles et que la nouvelle tentative peut fonctionner lorsque le système est moins occupé.
-   Service **VSS \_ Le \_ \_** **\_ \_ \_ délai d’expiration** de WRITERERROR OUTOFRESOURCES ou VSS e WRITERERROR peut suggérer une réduction de la charge système avant une nouvelle tentative
-   Service **VSS \_ E \_ WRITERERROR non \_ renouvelable** ou l' **enregistreur VSS \_ e \_ \_ ne \_ répondrait probablement pas** une erreur de writer, si bien qu’il n’est pas possible de tenter de sauvegarder ses données avec VSS.

En fonction du writer et des composants qui les génèrent, il n’est pas toujours nécessaire pour une application de sauvegarde d’abandonner suite à une erreur de veto ou d’erreur.

Par exemple, un demandeur peut décider que l’intention du cliché instantané est de sauvegarder l’application A et que le veto a été reçu de l’enregistreur pour l’application de sauvegarde B. Dans ce cas, il est parfaitement acceptable de continuer à sauvegarder l’application A tout en ignorant le veto.

Voici quelques exemples de refus d’un rédacteur :

-   Le writer veto le processus de création de clichés instantanés lorsqu’il n’a pas pu interrompre ses activités pendant la création du cliché instantané. Cela indique qu’il y a une forte probabilité que le cliché instantané ne soit pas valide, car une opération d’écriture s’est produite pendant l’état de blocage.
-   Une application de sauvegarde a demandé un cliché instantané du volume C : et un enregistreur détermine qu’un cliché instantané de C : et D : est de sauvegarder ses données. Dans ce cas, l’enregistreur est refusé. L’application de sauvegarde peut examiner les métadonnées et déterminer si le writer sera ignoré ou si le processus de création de clichés instantanés sera abandonné et redémarré ultérieurement.

 

 



