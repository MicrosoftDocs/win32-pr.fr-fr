---
description: 'En réponse à un événement d’identification, chaque enregistreur présent sur le système construit son propre document de métadonnées d’écriture à l’aide de IVssCreateWriterMetadata. Un événement d’identification est généralement généré par un demandeur appelant IVssBackupComponents :: GatherWriterMetadata.'
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: Cycle de vie des documents de métadonnées de l’enregistreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45be5748625d21f99abe3e77e0d6474a62210904
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519303"
---
# <a name="writer-metadata-document-life-cycle"></a>Cycle de vie des documents de métadonnées de l’enregistreur

En réponse à un [*événement d’identification*](vssgloss-i.md), chaque enregistreur présent sur le système construit son propre document de métadonnées d’écriture à l’aide de [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata). Un *événement d’identification* est généralement généré par un demandeur appelant [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Lors de la création d’un document de métadonnées d’écriture, par le biais de l’interface [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) ou de l’initialisation de l’enregistreur ([**CVssWriter :: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)), un enregistreur doit spécifier explicitement les éléments suivants :

-   [*Méthode de restauration*](vssgloss-r.md)
-   Nom de l’enregistreur
-   [*ID de classe de l’enregistreur*](vssgloss-w.md)
-   Utilisation des données ( [**voir \_ \_ type d’utilisation de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Type de source de date (voir [**\_ \_ type de source VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

En outre, il peut également spécifier les éléments suivants :

-   Composants (qui peuvent éventuellement contenir des jeux de fichiers)
-   Ajouter d’autres mappages
-   Exclure les listes de fichiers

Une vue d’ensemble de la création de documents de métadonnées d’enregistreur se trouve dans [actions d’écriture pendant l’initialisation](overview-of-backup-initialization.md)de la sauvegarde.

Les demandeurs utilisent généralement l’une des deux méthodes pour obtenir l’accès aux métadonnées de l’enregistreur :

-   Pendant la plupart des opérations de sauvegarde, un demandeur utilise [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) pour obtenir une instance de l’interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) afin d’autoriser l’accès aux métadonnées d’un writer en cours d’exécution.
-   Pour les opérations de restauration ou les sauvegardes à l’aide de clichés instantanés importés (voir [importation de volumes de clichés instantanés transportables](importing-transportable-shadow-copied-volumes.md) pour plus d’informations sur l’importation des clichés instantanés), un demandeur récupère un document XML contenant les métadonnées et utilise [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) pour obtenir une interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , qu’il utilise pour lire les métadonnées de restauration.

Les documents de métadonnées d’écriture permettent au demandeur d’effectuer une sauvegarde pour en savoir plus sur les enregistreurs en cours d’exécution pendant la phase de découverte d’une sauvegarde.

Pour les Writers choisis pour participer à une sauvegarde, un demandeur importe bien, mais pas toutes, les informations contenues dans le document des métadonnées de l’enregistreur dans son propre document sur les composants de sauvegarde pendant la phase de découverte d’une sauvegarde.

Toutefois, seuls les documents de métadonnées de l’enregistreur et non le document composants de sauvegarde contiennent les spécifications de fichier et de chemin d’accès.

Pour plus d’informations sur la façon dont la phase de découverte d’une opération de sauvegarde est effectuée, consultez [vue d’ensemble de la phase de découverte de la sauvegarde](overview-of-the-backup-discovery-phase.md).

En outre, seuls les composants [*inclus explicitement*](vssgloss-e.md) disposent de leurs informations stockées dans le document des composants de sauvegarde au cours d’une opération de sauvegarde. Les informations sur les composants [*inclus implicitement*](vssgloss-i.md) ne sont pas incluses dans le document des composants de sauvegarde au cours d’une opération de sauvegarde, et doivent être interpolées à l’aide d’informations sur les composants explicitement inclus et les documents de métadonnées de l’enregistreur disponibles.

Les composants inclus implicitement peuvent toujours être [*sélectionnables pour la restauration*](vssgloss-s.md) et doivent éventuellement être inclus explicitement dans le document des composants de sauvegarde au moment de la restauration. Dans ce cas, tout comme l’ajout d’un composant pendant une opération de sauvegarde nécessitait l’accès au document de métadonnées de l’enregistreur writer’s du composant (puis récupéré à partir de l’enregistreur), un demandeur devra accéder à une copie des documents de métadonnées de l’enregistreur de ce writer, stockés au moment de la sauvegarde.

Par conséquent, la seule façon d’obtenir toutes les informations sur tous les fichiers et tous les composants impliqués dans une sauvegarde ou une restauration consiste à avoir chaque document de métadonnées de l’enregistreur pour chaque rédacteur qui participe à une sauvegarde stockée avec le document des composants de sauvegarde. (Pour plus d’informations, consultez [vue d’ensemble de la restauration de fichiers réelle](overview-of-actual-file-restoration.md).)

 

 



