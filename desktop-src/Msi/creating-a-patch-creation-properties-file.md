---
description: pour reproduire l’exemple de package de correctifs, vous avez besoin d’un outil logiciel permettant de créer et de modifier un package de correctifs Windows Installer.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Création d’un fichier de propriétés de création de correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50873fd508aa9f31435bd401284d38d13310991e150b28f4e24e5ec27f505dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379404"
---
# <a name="creating-a-patch-creation-properties-file"></a>Création d’un fichier de propriétés de création de correctifs

pour reproduire l’exemple de package de correctifs, vous avez besoin d’un outil logiciel permettant de créer et de modifier un package de correctifs Windows Installer. Plusieurs outils de création de packages de correctifs sont disponibles auprès des éditeurs de logiciels indépendants. l’exemple décrit dans les sections suivantes utilise une Windows Installer éditeur de base de données appelé Orca pour créer un fichier de propriétés de création de correctifs (extension. pcp). le fichier. pcp peut être utilisé avec les utilitaires [Msimsp.exe](msimsp-exe.md) et [Patchwiz.dll](patchwiz-dll.md) pour générer un package de correctifs Windows Installer (extension. msp). Orca, Msimsp.exe et Patchwiz.dll sont fournis dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Un fichier de propriétés de création de correctifs vide, template. PCP, est également fourni avec le kit de développement logiciel (SDK). Effectuez une copie de template. PCP et renommez cette copie MNP2000. PCP. Utilisez Orca ou un autre éditeur de base de données pour entrer les données suivantes dans la table Properties de MNP2000. PCP. La table propriétés contient des paramètres globaux pour le package correctif.

[Tableau des propriétés](properties-table-patchwiz-dll-.md)



| Nom                               | Valeur                                  |
|------------------------------------|----------------------------------------|
| AllowProductCodeMismatches         | 1                                      |
| AllowProductVersionMajorMismatches | 1                                      |
| ApiPatchingSymbolFlags             | 0x00000000                             |
| DontRemoveTempFolderWhenFinished   | 1                                      |
| IncludeWholeFilesOnly              | 0                                      |
| ListOfPatchGUIDsToReplace          |                                        |
| ListOfTargetProductCodes           | \*                                     |
| PatchGUID                          | {5406B219-A1AC-4BC4-8695-72292C8195AC} |
| PatchOutputPath                    | c : \\ sortie. msp                         |
| PatchSourceList                    | PatchSourceList                        |



 

Utilisez l’éditeur de base de données pour entrer les données suivantes dans la table ImageFamilies de MNP2000. PCP. La table ImageFamilies contient des informations à ajouter à la [table multimédia](media-table.md) lors de la mise à jour corrective.

[Table ImageFamilies](imagefamilies-table-patchwiz-dll-.md)



| Famille  | MediaSrcPropName | MediaDiskId | FileSequenceStart | DiskPrompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| MNPapps | MNPSrcPropName   | 2           | 1 000              |            |             |



 

Entrez les données suivantes dans la table UpgradedImages de MNP2000. PCP. La table UpgradedImages contient des informations sur l’image mise à niveau que vous avez créée lors de la [planification d’un correctif logiciel de petite mise à jour](planning-a-small-update-patch.md).

[Table UpgradedImages](upgradedimages-table-patchwiz-dll-.md)



| Upgraded   | MsiPath                                           | PatchMsiPath | SymbolPaths | Famille  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| MNP \_ fixe | C : \\ Remarque le \_ correctif du programme d’installation a \\ \\ mis à niveau \\MNP2000.msi |              |             | MNPapps |



 

Entrez les données suivantes dans la table TargetImages de MNP2000. PCP. La table TargetImages contient des informations sur l’image cible.

[Table TargetImages](targetimages-table-patchwiz-dll-.md)



| Cible     | MsiPath                                         | SymbolPaths | Upgraded   | Commande | ProductValidateFlags | IgnoreMissingSrcFiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| \_Erreur MNP | C : \\ remarque \_MNP2000.msi de la cible de correctif du programme d’installation \\ \\ \\ |             | MNP \_ fixe | 1     |                      | 0                     |



 

Pour l’exemple de package de correctifs, laissez les tableaux suivants dans MNP2000. PCP vide.

[\_Table UpgradedFiles OptionalData](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[Table FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md)

[\_Table TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md)

[Table ExternalFiles](externalfiles-table-patchwiz-dll-.md)

[Table UpgradedFilesToIgnore](upgradedfilestoignore-table-patchwiz-dll-.md)

[Continuer](generating-a-patch-package.md)

 

 



