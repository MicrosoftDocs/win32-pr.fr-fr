---
description: Le document composants de sauvegarde est conservé par les instances de l’interface IVssBackupComponents.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Contenu du document des composants de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e12c88ebffa0037702e1f30dd818d4fd23fe4e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413405"
---
# <a name="backup-components-document-contents"></a>Contenu du document des composants de sauvegarde

Le document composants de sauvegarde est conservé par les instances de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Cette interface contient également de nombreuses méthodes de contrôle des opérations de sauvegarde, de manipulation des clichés instantanés et d’interrogation de l’état du système. Toutefois, toutes les informations du document ne sont pas directement accessibles par le biais de cette interface.

Le document composants de sauvegarde se compose de plusieurs ensembles de données :

-   Informations sur les composants qui ont été explicitement inclus dans une opération de sauvegarde ou de restauration
-   Représentation du composant stocké et des informations sur l’enregistreur
-   Informations d’État sur l’opération de sauvegarde/récupération

Alors que les informations sur les composants sont disponibles pour le demandeur et l’enregistreur, seul l’enregistreur a accès aux informations d’État.

## <a name="component-inclusion-information"></a>Informations sur l’inclusion du composant

Le document composants de sauvegarde contient une liste de ces composants explicitement inclus dans la sauvegarde et la restauration par le demandeur. La liste contient les éléments suivants :

-   [*Composants sélectionnables*](vssgloss-s.md)explicitement inclus.

    L’inclusion de ces fichiers dans les opérations de sauvegarde est indiquée par [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) et dans les opérations de restauration par [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Non sélectionnable pour les sous-composants de sauvegarde sans sélection pour l’ancêtre du composant de sauvegarde.

    Tous ces composants doivent être inclus si des composants de l’enregistreur doivent être inclus dans l’opération. L’inclusion de ces fichiers dans les opérations de sauvegarde est indiquée par [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) et dans les opérations de restauration par [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Les composants ajoutés implicitement à la sauvegarde (sous-[*composants*](vssgloss-s.md)) [*sélectionnables pour la restauration*](vssgloss-s.md) et sont ajoutés explicitement à la restauration.

    Ces composants peuvent être sélectionnables ou non sélectionnables, mais ils ont un ancêtre sélectionnable qui a été utilisé pour les sélectionner implicitement pour la sauvegarde. Ils sont ajoutés au document composants de sauvegarde par [**IVssBackupComponents :: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Les identités des composants inclus implicitement dans la restauration ne sont pas stockées dans le document sur les composants de sauvegarde.

VSS a accès aux informations sur l’inclusion de composants : les enregistreurs sans composants inclus explicitement dans une restauration ou une sauvegarde ne reçoivent aucun événement VSS après la génération des événements [*PrepareForBackup*](vssgloss-p.md) ou [*Restore*](vssgloss-p.md) .

Les enregistreurs ne peuvent pas directement interroger ces informations. Ce n’est pas une limitation significative, car par la conception, les enregistreurs VSS individuels ne doivent pas nécessiter d’informations détaillées sur l’état d’autres enregistreurs sur le système et, comme indiqué ci-dessus, ceux qui n’ont pas de composants inclus n’auront pas à participer à l’opération VSS.

Un demandeur peut déterminer les composants qui ont été explicitement inclus dans une opération.

La méthode [**IVssBackupComponents :: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) retourne le nombre d’enregistreurs avec les informations de composant stockées dans le document des composants de sauvegarde (et non le nombre de composants dans le document).

Le demandeur indexe les informations du writer stocké à l’aide de [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), qui retourne des instances de l’interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) . L’interface **IVssWriterComponentsExt** permet au demandeur d’obtenir la [*classe de writer*](vssgloss-w.md) et l’instance de [*writer*](vssgloss-w.md) des Writers participants, ainsi que d’accéder aux informations sur les composants de ses composants stockés dans le document sur les composants de sauvegarde.

## <a name="information-on-included-components"></a>Informations sur les composants inclus

La représentation du document des composants de sauvegarde des données du composant (qui n’inclut pas les informations de chemin d’accès et de spécification de fichier), accessible via des instances de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Les demandeurs et les Writers obtiennent l’accès aux instances de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) de différentes façons.

Un demandeur examine les données de composant à l’aide d’un writer par writer à l’aide d’instances de l’interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) retournée par [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

En plus des informations d’identification du writer, l’interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) fournit un tableau d’instances de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) : une pour chacun des composants inclus inclus.

Comme indiqué dans les [composants de sauvegarde cycle de vie des documents](backup-components-document-life-cycle.md), les enregistreurs peuvent accéder aux mêmes informations par le biais de l’interface [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) lors du traitement de l’événement PrepareForBackup, PrepareForSnapshot, PostSnapshot, BackupComplete, prerestauration ou postRestore.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permet aux rédacteurs et aux demandeurs d’obtenir les informations suivantes :

-   Le nom, le type et le [*chemin logique*](vssgloss-l.md) d’un composant ([**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname), [**GetComponentType**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Comment un composant doit être restauré comme indiqué par la [*cible de restauration*](vssgloss-r.md) ([**IVssComponent :: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Si un autre emplacement a été utilisé pour restaurer un fichier ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Nouvelles informations sur la cible, le cas échéant ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Messages d’erreur avant et après la restauration ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Si un élément [*sélectionnable pour*](vssgloss-s.md) le composant de sauvegarde définissant un jeu de composants a été sélectionné pour la restauration ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))
-   Si une sauvegarde ou une restauration a réussi ([**GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Toutes les options de sauvegarde ou de restauration spécifiques au writer qui ont pu être définies par [**IVssBackupComponents :: SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) ou [**IVssBackupComponents :: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions))
-   Toutes les métadonnées de sauvegarde ou de restauration de métadonnées spécifiques au writer ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Informations de date et d’heure ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Informations sur les sous-composants de sauvegarde inclus explicitement dans une restauration ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

Contrairement aux demandeurs, les enregistreurs peuvent modifier certaines informations dans le document des composants de sauvegarde via l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) :

-   Comment un composant doit être restauré comme indiqué par la cible de restauration ([**IVssComponent :: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Sauvegarde et restauration spécifiques aux rédacteurs ([**IVssComponent :: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent :: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))
-   Informations de datage ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Messages d’erreur avant et après la restauration ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Informations sur l’état du demandeur

Les demandeurs insèrent des informations sur l’état d’une opération de sauvegarde ou de restauration dans le document des composants de sauvegarde à l’aide de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Les applications de Writer peuvent interroger ces informations par le biais de la classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) .

Les informations d’État stockées dans le document sur les composants de sauvegarde incluent les éléments suivants :

Informations générales sur la sauvegarde

-   Le type de sauvegarde globale (incrémentielle, différentielle ou complète)<dl> <dt>

Défini par les demandeurs à l’aide de [ **IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Récupéré par les enregistreurs à l’aide de [ **CVssWriter :: GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Défini par les demandeurs à l’aide de [ **IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Récupéré par les enregistreurs à l’aide de [ **CVssWriter :: AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Défini par les demandeurs à l’aide de [ **IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Récupéré par les enregistreurs à l’aide de [ **CVssWriter :: IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Défini par les demandeurs à l’aide de [ **IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Récupéré par les enregistreurs à l’aide de [ **CVssWriter :: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Informations générales sur la restauration

-   Le type de restauration globale (que la restauration se fasse par copie ou importation)<dl> <dt>

Défini par les demandeurs à l’aide de [ **IVssBackupComponents :: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Récupéré par les enregistreurs à l’aide de [ **CVssWriter :: GetRestoreType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Informations sur les fichiers de prise en charge

-   Emplacement des fichiers de plages utilisés par un composant spécifique dans les opérations de fichiers partielles<dl> <dt>

Défini par les demandeurs à l’aide de [ **IVssBackupComponents :: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Récupéré par les rédacteurs (ou les demandeurs) à l’aide de [ **IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

État des informations

-   Indiquer si l’un des composants d’un enregistreur donné a été correctement sauvegardé<dl> <dt>

Défini par les demandeurs à l’aide de [ **IVssBackupComponents :: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Récupéré par les rédacteurs et les demandeurs à l’aide de [ **IVssComponent :: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Défini par les demandeurs à l’aide de [ **IVssBackupComponents :: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Récupéré par les rédacteurs et les demandeurs à l’aide de [ **IVssComponent :: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Informations Writer-Settable

-   Spécification de sauvegarde supplémentaire pour l’un des composants d’un générateur donné<dl> <dt>

Défini par les enregistreurs à l’aide de [ **IVssComponent :: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Récupéré par les rédacteurs et les demandeurs à l’aide de [ **IVssComponent :: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Défini par les enregistreurs à l’aide de [ **IVssComponent :: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Récupéré par les rédacteurs et les demandeurs à l’aide de [ **IVssComponent :: GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Défini par les enregistreurs à l’aide de [ **IVssComponent :: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Récupéré par les rédacteurs et les demandeurs à l’aide de [ **IVssComponent :: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a><dl> <dt>

Stocké et défini par les demandeurs pour un composant spécifique à l’aide de [ **IVssBackupComponents :: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Récupéré par les rédacteurs et les demandeurs à l’aide de [ **IVssComponent :: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Défini par les enregistreurs à l’aide de [**IVssComponent :: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) ou [**IVssComponent :: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)
</dt> <dt>

Récupéré par les rédacteurs et les demandeurs à l’aide de [**IVssComponent :: GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) ou [**IVssComponent :: GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)
</dt> </dl>

 

 
