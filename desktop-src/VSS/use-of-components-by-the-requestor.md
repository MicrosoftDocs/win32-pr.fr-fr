---
description: Outre l’exécution d’une sauvegarde ou d’une restauration, et la surveillance des clichés instantanés, un demandeur doit gérer des informations sur les composants des rédacteurs avec lesquels il interagit.
ms.assetid: 641abfbe-fc72-4468-9ef6-69c452adb1b3
title: Utilisation de composants par le demandeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3149800a3f8cb52afff044e593f6b01177b27054c64a2ee19c19cb570ed633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998079"
---
# <a name="use-of-components-by-the-requester"></a>Utilisation de composants par le demandeur

Outre l’exécution d’une sauvegarde ou d’une restauration, et la surveillance des clichés instantanés, un demandeur doit gérer des informations sur les composants des rédacteurs avec lesquels il interagit. La sélection et le chemin logique des composants sont utilisés pour inclure ou exclure des données d’une sauvegarde, et pour déterminer les informations de composant qui sont incluses dans le document des composants de sauvegarde.

## <a name="requester-component-selection-during-backup"></a>Sélection du composant demandeur pendant la sauvegarde

Pendant les opérations de sauvegarde, un demandeur importe les données du composant de métadonnées du writer à l’aide des méthodes [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) et [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (pour plus d’informations, consultez [vue d’ensemble de l’initialisation](overview-of-backup-initialization.md) de la sauvegarde).

Après avoir examiné les informations du writer avec l’interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , un demandeur décide des Writers qu’il va sauvegarder et, dans une certaine mesure, des composants d’un enregistreur donné qu’il sauvegardera.

Lors de la sauvegarde d’un rédacteur, un demandeur :

-   Doit [*inclure explicitement*](vssgloss-e.md) tous les composants de l’enregistreur non sélectionnables pour la sauvegarde sans sélectionnable pour les ancêtres de sauvegarde à l’aide de [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) pour ajouter le composant au document des composants de sauvegarde
-   Peut inclure explicitement l’un des composants sélectionnables du writer pour la sauvegarde à l’aide de [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) pour ajouter le composant au document des composants de sauvegarde
-   Si un composant sélectionnable pour la sauvegarde définit un [*jeu de composants*](vssgloss-c.md), son inclusion explicite [*comprend implicitement*](vssgloss-i.md) tous les membres du jeu de composants, qu’il soit sélectionnable ou non pour la sauvegarde. Ces composants ne sont pas ajoutés au document composants de sauvegarde.

Lors de l’ajout d’un composant sélectionnable pour la sauvegarde ou de composants non sélectionnables pour la sauvegarde sans sélectionnable pour les ancêtres de sauvegarde dans le document des composants de sauvegarde, un demandeur spécifie les éléments suivants :

-   Instance du writer qui gère le composant
-   Identificateur de classe du writer
-   [*Chemin d’accès logique*](vssgloss-l.md) du composant (qui peut être **null**)
-   Nom du composant

Si un composant ne correspond pas à la spécification, une erreur est retournée.

Si un tel composant existe, VSS crée une interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) pour le composant dans le document composants de sauvegarde. Ces informations sont accessibles et modifiables par le writer et le demandeur. Pour un composant sélectionnable qui définit un [*jeu de composants*](vssgloss-c.md), il décrit non seulement les propriétés du composant, mais également tous les sous-composants qu’il contient.

Les informations sur les composants ajoutés implicitement ne sont pas disponibles dans le document composants de sauvegarde. En outre, aucune information de fichier n’est disponible dans le document sur les composants de sauvegarde. Pour obtenir ces informations, le demandeur devra examiner les documents de métadonnées de l’enregistreur (qui auront déjà été lus) dans le contexte des composants stockés sélectionnés dans le document composants de sauvegarde.

## <a name="requester-component-selection-during-restore"></a>Sélection du composant demandeur pendant la restauration

Pendant les opérations de restauration, un demandeur ne doit pas importer les informations sur les composants à partir des enregistreurs actuellement actifs sur le système via [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), car l’état des processus en cours d’exécution ne reflète pas nécessairement l’état des processus lorsqu’une sauvegarde a été effectuée.

Elle doit toujours générer un [*événement d’identification*](vssgloss-i.md) via [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), à la fois pour créer un *événement d’identification* et pour déterminer quels Writers sont actuellement sur le système et leur état.

Le demandeur récupère le document des composants de sauvegarde stocké pendant son initialisation ainsi que les documents de métadonnées de l’enregistreur stocké (pour plus d’informations, consultez [vue d’ensemble de l’initialisation de la restauration](overview-of-restore-initialization.md) ).

L’inclusion de composants lors de la sauvegarde est en grande partie identique à celle de la restauration, à ceci près que vous devez envisager [*d’utiliser Selectable pour la restauration*](vssgloss-s.md) avec le [*chemin logique*](vssgloss-l.md), et non [*sélectionnable pour la sauvegarde*](vssgloss-s.md).

Toutefois, il existe quelques différences :

-   Si un composant a déjà été [*explicitement inclus*](vssgloss-e.md) dans le document des composants de sauvegarde lors de la sauvegarde, s’il est inclus pour la restauration (explicitement ou implicitement), [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) est utilisé pour l’ajouter explicitement au document des composants de sauvegarde pour restauration.
-   Si un composant a été [*implicitement inclus*](vssgloss-i.md) dans la sauvegarde et qu’il ne peut pas être sélectionné pour la restauration sans sélectionnable pour les ancêtres de restauration, ce qui, dans le cas de la sauvegarde, implique la nécessité d’une inclusion explicite ; le composant n’est pas inclus explicitement (c’est-à-dire qu’il n’est pas ajouté au document des composants de sauvegarde à l’aide de [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)). Ce composant doit être considéré comme étant implicitement sélectionné pour la restauration.
-   Parmi ces composants implicitement sélectionnés pour la sauvegarde (que ce composant soit sélectionnable ou non), seuls ceux qui peuvent être sélectionnés pour la restauration peuvent être ajoutés au document des composants de sauvegarde à l’aide de [**IVssBackupComponents :: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).
-   Sélectionnables pour les composants de restauration peut définir un [*jeu*](vssgloss-c.md) de composants pour la restauration, comme vous pouvez le faire pour les composants de sauvegarde. Ce composant sélectionnable pour la restauration définit ensuite ce jeu de composants pour l’opération de restauration.

Un enregistreur sans composants explicitement sélectionnés pour la restauration avant la génération d’un événement de [*prérestauration*](vssgloss-p.md) ne recevra aucun événement VSS.

Les demandeurs et les enregistreurs peuvent accéder aux informations de composant stockées à l’aide de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) . Par le biais de l’interface **IVssComponent** , les enregistreurs peuvent modifier certains paramètres de leurs composants explicitement inclus dans le document des composants de sauvegarde pour prendre en charge une restauration (telle que la [*cible de restauration*](vssgloss-r.md)). Si elle définit un jeu de composants, les modifications de l’enregistreur d’un composant explicitement inclus sont propagées à ses sous- [*composants*](vssgloss-s.md). En outre, l’interface fournit un mécanisme permettant de passer des informations sur la réussite et l’échec de la restauration entre l’enregistreur et le demandeur.

Comme pendant la sauvegarde, il y a des informations insuffisantes dans le document des composants de sauvegarde pour implémenter la restauration. Là encore, les documents de métadonnées de l’enregistreur sont requis pour fournir des informations sur les chemins d’accès réels des fichiers à restaurer et découvrir les composants non sélectionnables qui font partie du jeu de composants sélectionnables et doivent donc être restaurés.

Pour plus d’informations sur les types de sélectivité et leur utilisation, consultez Utilisation de la [sélectivité et des chemins d’accès logiques](working-with-selectability-and-logical-paths.md) .

## <a name="use-of-writer-component-document-information-by-the-requester"></a>Utilisation des informations de document du composant Writer par le demandeur

Chaque composant est identifié de manière unique par l' [*ID de classe du writer*](vssgloss-w.md) de son Writer parent, son nom et son [*chemin d’accès logique*](vssgloss-l.md).

Le demandeur peut utiliser l’interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) retournée par la méthode [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) pour obtenir des informations sur chaque composant stocké.

Le nom du composant et le chemin logique (entre autres éléments) sont accessibles via l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) retournée par [**IVssWriterComponentsExt :: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent).

> [!Note]  
> Pendant la phase de restauration, le demandeur doit appeler [**IVssWriterComponentsExt :: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) ou [**IVssWriterComponentsExt :: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) uniquement après l’appel à [**IVssBackupComponents ::P Restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) a retourné pour permettre au writer de mettre à jour le document des composants de sauvegarde. La modification de la cible de restauration constitue un exemple de cette mise à jour.

 

Vous trouverez des informations sur l’enregistreur parent de chaque composant sélectionnable stocké à l’aide de [**IVssWriterComponentsExt :: GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo).

Avec ces informations, les documents de métadonnées de l’enregistreur peuvent être interrogés et le document correspondant doit être identifié. Ensuite, en utilisant le [*chemin logique*](vssgloss-l.md), le demandeur peut identifier les composants non sélectionnables dépendants pour chaque composant sélectionnable, c’est-à-dire identifier tous les membres du [*jeu de composants*](vssgloss-c.md)sélectionnables du composant.

À l’aide de l’interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , le demandeur a désormais des informations complètes sur les composants, y compris la spécification du chemin d’accès (à partir de l’interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) ), pour les composants sélectionnables et non sélectionnables qu’il doit sauvegarder ou restaurer.

C’est l’une des raisons pour lesquelles un demandeur est essentiel d’enregistrer l’état de son propre document de composants de sauvegarde et les documents de métadonnées de l’enregistreur des rédacteurs qu’il sauvegarde.

Pour plus d’informations, consultez [utilisation de la sélectivité et des chemins d’accès logiques](working-with-selectability-and-logical-paths.md) .

 

 
