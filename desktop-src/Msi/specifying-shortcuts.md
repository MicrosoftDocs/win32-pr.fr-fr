---
description: La table de raccourcis et les tables associées de la base de données d’installation contiennent les informations nécessaires pour installer les raccourcis. Consultez le groupe tables d’informations sur les programmes et les raccourcis du programme d’installation de la modification.
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: Spécification de raccourcis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67b43a104ee05b3711ac98395098acf9393faab8e046296e58d93df4d6b9218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624683"
---
# <a name="specifying-shortcuts"></a>Spécification de raccourcis

La [table de raccourcis](shortcut-table.md) et les tables associées de la base de données d’installation contiennent les informations nécessaires pour installer les raccourcis. Consultez le [groupe tables d’informations sur les programmes](program-information-tables-group.md) et les [raccourcis du programme d’installation](editing-installer-shortcuts.md)de la modification.

dans cette section, vous allez ajouter des informations qui spécifient les raccourcis publiés et non publiés pour l’exemple Bloc-notes.

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans le tableau de raccourcis.

[Tableau de raccourcis](shortcut-table.md)



| Raccourci  | Répertoire\_ | Nom         | -\_ | Cible             | Arguments | Description | Touche d’accès rapide | Icône\_         | IndexIcône | ShowCmd | WkDir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sBaseball | MENUDIR     | Baseball.txt | Chaussures    | Chaussures           |           |             |        | \_icon.exe Orca |           |         |       |
| sConcert  | MENUDIR     | Concert.txt  | Concert     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sDance    | MENUDIR     | Dance.txt    | Jongl       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sFootball | MENUDIR     | Football.txt | Terrain    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| sHelp     | MENUDIR     | Help.txt     | Aide        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sJanuary  | MENUDIR     | January.txt  | Janvier     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| sNewYears | MENUDIR     | NewYears.txt | NewYears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| sNotepad  | MENUDIR     | Redpark.exe  | Bloc-notes     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sReadme   | MENUDIR     | Lisezmoi.txt   | Bloc-notes     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

L’exemple d’installation doit activer l’installation d’un raccourci publié pour la fonctionnalité de baseball. Pour cela, vous devez spécifier une clé de la table d’icônes dans la \_ colonne icône du tableau de raccourcis. dans le cadre de cet exemple, vous pouvez copier l’icône de l’éditeur de base de données Orca fourni avec le kit de développement logiciel (SDK) Windows Installer. Exportez la [table d’icônes](icon-table.md) à partir de Orca.msi puis fusionnez cette table dans la base de données MNP2000.msi à l’aide d’Orca ou d’un autre outil de fusion. Orca crée également un répertoire nommé Icon dans le répertoire contenant MNP2000.msi et ajoute l’icône fichier de données binaire Orca \_icon.exe. IBD. Consultez la colonne de données dans la table des icônes. La table d’icône terminée doit se présenter comme suit quand elle est affichée dans Orca.

[Table d’icônes](icon-table.md)



| Nom           | Données            |
|----------------|-----------------|
| \_icon.exe Orca | \[Binary Data\] |



 

[Continuer](specifying-properties.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modification des raccourcis du programme d’installation](editing-installer-shortcuts.md)
</dt> </dl>

 

 



