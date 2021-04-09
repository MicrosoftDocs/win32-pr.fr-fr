---
description: L’utilisation de composants sélectionnés implicitement nécessite l’accès aux documents de métadonnées document et enregistreur de composants de sauvegarde.
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Sélection et utilisation des propriétés de composant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d06683bafb02802d84f152f1ceb662eb7491f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115142"
---
# <a name="selectability-and-working-with-component-properties"></a>Sélection et utilisation des propriétés de composant

L’utilisation de composants sélectionnés implicitement nécessite l’accès aux documents de métadonnées document et enregistreur de composants de sauvegarde.

Il existe deux raisons à cela :

-   Les données de composant stockées dans le document des composants de sauvegarde (représentées par l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ) ne sont pas accessibles à des informations sur le jeu de fichiers du composant (spécification de fichier, chemin d’accès et indicateur de récurrence). (Consultez [utilisation du document sur les composants de sauvegarde](working-with-the-backup-components-document.md).)
-   Seuls les composants [*inclus explicitement*](vssgloss-e.md) dans le document composants de sauvegarde lors de la sauvegarde disposent de leurs informations directement stockées dans le document sur les composants de sauvegarde. Les demandeurs et les Writers doivent utiliser les informations disponibles par le biais de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , conjointement avec les informations de [*chemin d’accès logique*](vssgloss-l.md) et les documents de métadonnées d’écriture pour obtenir des informations et définir les propriétés des composants [*inclus implicitement*](vssgloss-i.md) .

Le cas « MyWriter » présenté dans [chemin logique des composants](logical-pathing-of-components.md) peut être utilisé pour illustrer la sélectivité de la sauvegarde.



| Nom du composant | Chemin logique            | Sélectionnable pour la sauvegarde | Sélectionnable pour la restauration | Inclus explicitement |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| Exécut  | ""                      | N                     | N                      | O                   |
| "ConfigFiles"  | Exécut           | N                     | N                      | O                   |
| "LicenseInfo"  | ""                      | O                     | N                      | O                   |
| « Security »     | ""                      | O                     | N                      | O                   |
| UserInfo     | « Security »              | N                     | N                      | N                   |
| EUR.1 | « Security »              | N                     | N                      | N                   |
| "writerData"   | ""                      | O                     | O                      | O                   |
| Jeu1         | "writerData"            | N                     | O                      | N                   |
| Janvier          | « writerData \\ Set1 »      | N                     | N                      | N                   |
| Decembre          | « writerData \\ Set1 »      | N                     | N                      | N                   |
| Set2         | "writerData"            | N                     | O                      | N                   |
| Janvier          | « writerData \\ Set2 »      | N                     | N                      | N                   |
| Decembre          | « writerData \\ Set2 »      | N                     | N                      | N                   |
| Demande        | « writerData \\ QueryLogs » | N                     | N                      | N                   |
| Syntaxe        | "writerData"            | O                     | O                      | N                   |
| Janvier          | « utilisation de writerData \\ »     | N                     | N                      | N                   |
| Decembre          | « utilisation de writerData \\ »     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Composants inclus implicitement dans le jeu de sauvegarde

En examinant le document des métadonnées de l’enregistreur d’un enregistreur (voir [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) pendant la sauvegarde, un demandeur doit stocker une liste de tous les composants, leurs [*chemins d’accès logiques*](vssgloss-l.md)et leurs informations sur le jeu de fichiers.

Le jeu de fichiers et les informations sur les fichiers exclus seront nécessaires pour déterminer une liste de fichiers pour tout composant inclus (explicitement ou implicitement).

Pour les composants de sauvegarde non sélectionnables pour les ancêtres de sauvegarde et sélectionnables pour les composants de sauvegarde qui ne définissent pas de [*jeu de composants*](vssgloss-c.md), seul le jeu de fichiers et les informations sur les fichiers exclus seront nécessaires pour identifier tous les candidats du composant pour la sauvegarde, car ces composants ne définissent pas les sous-composants.

Pour les composants sélectionnables explicitement pour les composants de sauvegarde qui définissent un jeu de composants, les jeux de fichiers et les informations sur les fichiers d’exclusion pour le composant de définition et tous les sous- [*composants*](vssgloss-s.md) doivent être utilisés pour sélectionner les fichiers à sauvegarder.

Cela signifie que les jeux de sauvegarde des composants « exécutables », « ConfigFiles » et « LicenseInfo » ne peuvent être trouvés qu’en examinant uniquement les métadonnées de l’enregistreur pour ces composants à l’aide de leurs instances de l’interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .

Toutefois, si writerData est explicitement inclus dans la sauvegarde, vous devez examiner son instance de l’interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) et celles de « Set1 », « Jan » (avec le chemin d’accès logique « writerData \\ SET1 »),» Dec» (avec le chemin d’accès logique « writerData \\ SET1 »), « Set2 », « Jan » (avec le chemin d’accès logique « writerData \\ SET2 »), « Dec » (avec le chemin d’accès logique « writerData \\ SET2 »), « Query », « usage », « Jan » (avec le chemin d’accès logique « WriterData usage ») \\ et «DEC \\

Pour ce faire, un demandeur devra d’abord identifier que le composant « writerData » (chemin logique «») est sélectionnable. Il devra ensuite analyser tous les autres composants gérés par le writer pour déterminer si le premier élément de son chemin logique est « writerData ». Les composants dont le chemin logique est « writerData » sont identifiés comme des sous-composants de « writerData » et sont implicitement sélectionnés lorsqu’ils sont explicitement sélectionnés.

En fait, une analyse similaire doit être effectuée pour déterminer qu’aucun composant n’a « LicenseInfo » comme membre de début de son chemin logique, ce qui signifie que « LicenseInfo » n’a aucun sous-composant.

En raison de la complexité de ce mécanisme dans VSS, de nombreux enregistreurs de demandeurs peuvent trouver utile de créer leurs propres structures pour stocker des informations sur les jeux de sauvegarde et les composants de manière explicite et implicite.

## <a name="properties-of-implicitly-included-components"></a>Propriétés des composants inclus implicitement

Lors des opérations de restauration et de sauvegarde, les instances des interfaces [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) et [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) sont utilisées à la fois pour récupérer des informations sur les composants et pour définir ou modifier les propriétés d’un composant. Toutefois, seuls les composants explicitement inclus auront des instances de l’interface **IVssComponent** ou seront accessibles à l’interface **IVssBackupComponents** .

Certaines propriétés sont définies à l’échelle des composants dans l’étendue. Ces propriétés sont les suivantes :

-   État de la sauvegarde et de la restauration : <dl>

[**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Options de sauvegarde et de restauration : <dl>

[**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**IVssComponent::GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**IVssComponent::GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   Messages d’échec : <dl>

[**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   Cibles de restauration : <dl>

[**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)  
    [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)  
    </dl>
-   Tampons de sauvegarde : <dl>

[**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)  
    [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)  
    </dl>
-   Métadonnées supplémentaires : <dl>

[**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)  
    [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)  
    [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)  
    [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)  
    </dl>

Par conséquent, vous utilisez l’instance de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) du membre de définition d’un jeu de composants ou utilisez le nom, le type et le chemin logique du membre de définition avec une méthode [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) pour définir ou récupérer les propriétés de tous les membres du jeu de composants.

Pour cette raison, les jeux de composants sont traités comme des unités. Par exemple, la sauvegarde d’un jeu de composants est réussie uniquement si la sauvegarde de tous les jeux de fichiers de tous ses composants est réussie.

Dans l’exemple précédent, supposons qu’un fichier du composant « Jan » (avec le chemin d’accès logique « writerData \\ SET2 ») soit membre du jeu de composants défini par « writerData ». Si l’un des fichiers de « Jan » n’a pas pu être sauvegardé, un demandeur utilise les informations de « writerData » (son nom « writerData », son chemin d’accès «» et son type de composant) comme arguments lors de la définition de [**IVssBackupComponents :: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) avec la **valeur false** pour indiquer la défaillance du jeu de composants.

De même, l’état retourné par [**IVssComponent :: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) pour l’instance de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) « writerData » s’applique non seulement à « writerData », mais également à tous ses sous-composants.

En outre, si un enregistreur a choisi de modifier la cible de restauration à l’aide de [**IVssComponent :: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) de l’instance de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)« writerData », cela modifierait la cible de restauration de tous les jeux de fichiers de tous les sous-composants de « writerData ».

Les propriétés suivantes ne s’appliquent pas à l’ensemble du composant, mais à des fichiers ou jeux de fichiers particuliers :

-   Mappages d’emplacements secondaires : <dl>

[**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**IVssComponent::GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   Fichiers différenciés : <dl>

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   Fichiers partiels : <dl>

[**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
    [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)  
    </dl>
-   Cibles dirigées : <dl>

[**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)  
    [**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)  
    [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount)  
    </dl>
-   Nouvelles cibles : <dl>

[**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

Lorsqu’un demandeur accède à ces fonctionnalités pour un sous-composant à l’aide de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , il utilise les informations de composant pour le composant qui définit le jeu de composants, mais les informations sur le fichier ou le jeu de fichiers du sous-composant.

De même, si la propriété est accessible via l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , l’instance correspondant au sous-composant de définition est utilisée, mais les arguments de fichier ou de jeu de fichiers sont extraits du sous-composant.

Par exemple, supposons que le sous-composant « Jan » (avec le chemin d’accès logique « writerData \\ SET2 ») contenait un jeu de fichiers avec le chemin d’accès « c : \\ Fred », une spécification de fichier « \* . dat » et qu’un indicateur récursif de **true** puisse être restauré à un autre emplacement.

Dans ce cas, un demandeur appelle [**IVssBackupComponents :: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping), à l’aide des informations de « writerData » (type de composant, nom de composant « writeData » et un chemin d’accès logique « ») ainsi que des informations sur le jeu de fichiers «Jan » (chemin d’accès « c : \\ Fred », spécification de fichier « \* . dat » et récurrence égale **true**).

Notez que dans ce cas, les informations du jeu de fichiers doivent correspondre exactement aux informations sur le jeu de fichiers utilisées par [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) pour ajouter des fichiers à Jan.

De même, si un auteur souhaite ajouter une cible dirigée à un fichier avec le chemin d’accès « c : \\ Ethel » et le nom « Lucy. dat » gérés par « Jan » (avec le chemin d’accès logique « writerData \\ SET2 »), il utilise l’instance [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondant à « writerData », mais les informations de fichier de « Jan ».

## <a name="implicitly-included-components-in-the-restore-set"></a>Composants inclus implicitement dans le jeu de restauration

Les composants qui étaient implicitement inclus dans une sauvegarde peuvent être inclus explicitement dans une restauration s’ils peuvent être sélectionnés pour la restauration. Comme indiqué dans [utilisation de la sélectivité pour la restauration et](working-with-selectability-for-restore-and-subcomponents.md)les sous-composants, ces composants sont ajoutés au document des composants de sauvegarde à l’aide de la méthode [**IVssBackupComponents :: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) .

Toutefois, cela ne crée pas de nouvelle instance de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , pas plus que le composant directement accessible via l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

Au lieu de cela, un composant explicitement inclus pour la restauration, mais inclus implicitement pour la sauvegarde, doit être accessible par le biais d’une instance de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondant au composant qui a défini le jeu de composants dont il était membre lors de la sauvegarde.

Par exemple, pour inclure explicitement pour Restore « Set1 », un sous-composant du composant sélectionnable pour la sauvegarde « writerData », vous obtenez des informations à son sujet en appelant la méthode [**IVssComponent :: GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) de l’instance de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) « writerData ».

 

 



