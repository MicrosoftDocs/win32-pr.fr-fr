---
description: 'Le document de métadonnées de l’enregistreur contient trois ensembles de données : les informations d’identification et de classification du writer, les spécifications au niveau de l’enregistreur et les données de composant.'
ms.assetid: 1a84790a-8f46-4e1b-8e45-5036830e8fee
title: Contenu du document de métadonnées de l’enregistreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f222977f1c8d785e6f69613f219545dc3402af7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033992"
---
# <a name="writer-metadata-document-contents"></a>Contenu du document de métadonnées de l’enregistreur

Le document de métadonnées de l’enregistreur contient trois ensembles de données : les informations d’identification et de classification du writer, les spécifications au niveau de l’enregistreur et les données de composant.

## <a name="writer-identification-information"></a>Informations d’identification de l’enregistreur

L’identification du writer et les informations de classification incluent les éléments suivants :

-   Nom de l’enregistreur
-   [*ID de classe de l’enregistreur*](vssgloss-w.md)
-   [*Instance d’enregistreur*](vssgloss-w.md)
-   Utilisation des données gérées par le writer sur le système hôte (voir [**type d' \_ utilisation \_ de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Type de données gérées par l’enregistreur (voir [**\_ \_ type de source VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

À l’exception de l’instance de writer, qui est unique et qui est générée par le système lors de l’initialisation d’un objet [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , toutes ces valeurs sont définies par un enregistreur lorsqu’il appelle [**CVssWriter :: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) et sont disponibles pour un demandeur en appelant [**IVssExamineWriterMetadata :: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity).

Étant donné que l’instance de writer est générée de manière unique, une instance de writer stockée Récupérée à partir d’un document de métadonnées d’écriture stocké n’est pas susceptible d’être utile.

En vérifiant le [**\_ \_ type d’utilisation de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type), une application peut déterminer si un enregistreur gère les données d’application générales, ou si les fichiers qu’il utilise font partie de l’état de démarrage du système ou sont utilisés par un service système. Les applications de sauvegarde et de restauration doivent respecter les types d’utilisation pour assurer la stabilité du système.

L’indicateur de [**\_ \_ type de source VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type) indique quel type d’application l’enregistreur gère les données à sauvegarder pendant un fonctionnement normal.

Actuellement, la distinction est limitée à la spécification de si l’enregistreur produit des fichiers dans le cadre d’opérations de base de données transactionnelles ou non transactionnelles, ou si les fichiers sont le résultat d’un type d’activité plus général. Cette liste peut croître au fil du temps. Ces informations peuvent être utiles pour déterminer le niveau d’activité normal attendu dans les fichiers d’un writer.

## <a name="writer-level-specification"></a>Spécification Writer-Level

Les spécifications au niveau de l’enregistreur contiennent des informations qui sont rédacteures dans sa portée, qui s’appliquent à toutes les données indépendantes de celles qui sont gérées par un composant.

Un enregistreur doit toujours spécifier des [*méthodes de restauration*](vssgloss-r.md).

Il peut éventuellement spécifier les éléments suivants :

-   Liste des fichiers exclus
-   [*Mappages d’emplacements secondaires*](vssgloss-a.md) pour la restauration

Les listes de fichiers include et Exclude contiennent des informations de fichier au-delà de celles figurant dans les composants, et leur spécification remplace la spécification de composant.

## <a name="restore-method-specification"></a>Spécification de la méthode Restore

La [*Méthode Restore*](vssgloss-r.md) est définie dans le document de métadonnées de l’enregistreur par [**IVssCreateWriterMetadata :: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) et récupérée par un demandeur avec [**IVssExamineWriterMetadata :: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Lors de la définition d’une méthode de restauration, un enregistreur indique la manière préférée de la restauration de fichiers, également appelée cible de restauration d’origine, pour tous les fichiers gérés par un enregistreur. Par exemple, la méthode Restore spécifie si tous les fichiers gérés par un enregistreur doivent être autorisés à remplacer les fichiers présents sur le disque. (Pour plus d’informations, consultez [configurations de restauration VSS](vss-restore-configurations.md) et [**\_ \_ énumération VSS RESTOREMETHOD**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) .)

## <a name="exclude-file-list-specification"></a>Exclure la spécification de liste de fichiers

La liste d’exclusion permet de paramétrer avec précision les spécifications de caractères génériques dans les composants en empêchant explicitement l’inclusion de certains fichiers dans un jeu de sauvegarde.

Par exemple, un composant peut avoir un [*jeu de fichiers*](vssgloss-f.md) contenant une spécification de fichier c : \\ base de données \\ \* . \* Bien qu’il s’agit d’une définition pratique, il se peut qu’il y ait parfois des fichiers temporaires générés (peut-être au format \* . tmp) et que l’enregistreur souhaite toujours empêcher leur sauvegarde.

Dans ce cas, un enregistreur ajoute \* . tmp à sa liste d’exclusion à l’aide de [**IVssCreateWriterMetadata :: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles). Cette spécification peut être récursive.

Un demandeur interroge ces informations à l’aide de [**IVssExamineWriterMetadata :: GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile).

La liste des fichiers d’exclusion est prioritaire sur les listes de fichiers de composants.

Ainsi, la liste des fichiers spécifiés pour la sauvegarde dans un document de métadonnées d’écriture se compose de tous les fichiers spécifiés dans les composants [*inclus explicitement*](vssgloss-e.md) et les composants [*inclus implicitement*](vssgloss-i.md) , moins tous les fichiers exclus.

## <a name="alternate-location-mappings-specification"></a>Spécification des mappages d’emplacements secondaires

Les mappages d’emplacements de remplacement sont initialement définis lors de la création d’un document de métadonnées d’écriture et indiquent un emplacement sur le disque dans lequel les fichiers peuvent être restaurés si la restauration d’un fichier vers l’emplacement d’origine n’est pas possible.

Les informations sont ajoutées sous la forme d’une chaîne de caractères larges terminée par un caractère NULL avec [**IVssCreateWriterMetadata :: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) et récupérées en tant qu’objet [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) par [**IVssExamineWriterMetadata :: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).

En dépit du fait que les mappages d’emplacements alternatifs sont spécifiés et examinés à l’aide des interfaces de niveau écriture ([**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) et [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)), ils sont spécifiés en termes de [*jeux de fichiers*](vssgloss-f.md). Le jeu de fichiers utilisé pour spécifier un autre mappage d’emplacement (chemin d’accès, spécification de fichier et indicateur de récurrence) doit correspondre à l’un des jeux de fichiers déjà ajoutés à l’un des composants du générateur (voir [Ajout de fichiers aux composants](definition-of-components-by-writers.md)).

Pour plus d’informations, consultez [emplacements de sauvegarde et de restauration non par défaut](non-default-backup-and-restore-locations.md).

## <a name="component-level-information"></a>Informations Component-Level

Les [*composants*](vssgloss-c.md) sont des collections de fichiers qui forment une unité logique à des fins de sauvegarde et de restauration. Tous les fichiers d’un composant (sauf ceux explicitement exclus) doivent être sauvegardés et restaurés en tant qu’unité.

Les Writers ajoutent des composants à l’aide de [**IVssCreateWriterMetadata :: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), en spécifiant les informations de composant suivantes :

-   Type
-   Nom
-   Chemin logique (le cas échéant)
-   Fonctionnalité prise en charge
-   [*Sélectivité*](vssgloss-s.md)
-   Métadonnées à utiliser par le writer pendant la restauration
-   Afficher des informations
-   Informations de notification

La sélection de la [*sauvegarde*](vssgloss-s.md) et de la [*sélectivité pour la restauration*](vssgloss-s.md) est complètement indépendante les unes des autres, et un enregistreur les utilise conjointement avec des chemins logiques pour indiquer les relations entre les différents composants qu’elle gère. Les enregistreurs peuvent indiquer les composants requis pour l' [*inclusion explicite*](vssgloss-e.md) (ceux qui peuvent être explicitement inclus à la discrétion d’un demandeur) et ceux qui peuvent uniquement être [*inclus implicitement*](vssgloss-i.md). (Voir [utilisation de la sélectivité et des chemins logiques](working-with-selectability-and-logical-paths.md).)

Des fichiers sont ajoutés à un composant donné à l’aide de [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles). (Consultez [Ajout de fichiers à des composants](definition-of-components-by-writers.md).)

Lors de l’ajout de fichiers à un composant pendant la sauvegarde, un enregistreur doit spécifier un jeu de fichiers (chemin d’accès, spécification de fichier et indicateur de récurrence) qui définit les fichiers à sauvegarder.

Les enregistreurs peuvent également spécifier un [*autre chemin d’accès*](vssgloss-a.md) pour la sauvegarde, ce qui ne doit pas être confondu avec les [*mappages d’emplacements de substitution*](vssgloss-a.md) mentionnés précédemment. Ce chemin alternatif indique un emplacement autre que celui par défaut à partir duquel les fichiers doivent être copiés lorsqu’un volume est sauvegardé.

Les informations relatives à un composant donné dans le document de métadonnées de l’enregistreur peuvent être obtenues via une interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) retournée par [**IVssExamineWriterMetadata :: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

Les fichiers et les chemins d’accès sont retournés dans [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) en tant qu’objets [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) .

Les informations sur les composants d’un enregistreur sont discutées en détail dans [définition des composants par les rédacteurs](definition-of-components-by-writers.md).

 

 



