---
description: Effectuez une copie de l’exemple de package d’installation Windows Installer MNP2000.msi et renommez cette copie MNP2000t.msi.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Personnalisation d’une base de données d’origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3222ebce146e891c7b16c70eb78f0f26b95727c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544696"
---
# <a name="customizing-an-original-database"></a>Personnalisation d’une base de données d’origine

Effectuez une copie de l’exemple de package d’installation Windows Installer MNP2000.msi et renommez cette copie MNP2000t.msi. Dans les étapes suivantes, vous allez personnaliser ce fichier à l’aide d’un éditeur de tables de base de données comme Orca, qui est fourni avec le kit de développement logiciel (SDK) ou un autre éditeur de base de données.

Incluez le nouveau fichier de ressources pour la liste téléphonique, Phone.txt, dans le dossier du bloc-notes avec les autres fichiers sources.



| Fichier      | Description                             | Chemin de la source                 | Chemin d’accès à la cible                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | Ressource pour la fonctionnalité de \_ Liste téléphonique. | C : \\ exemple de \\ bloc-notes \\phone.txt | \[\] \\phone.txt de \_ parc \\ rouge d’ProgramFilesFolder |



 

Utilisez votre éditeur de base de données pour ajouter un enregistrement à la [table de fichiers](file-table.md) de MNP2000t.msi pour le nouveau fichier.

[Table de fichier](file-table.md)



| Fichier      | -\_ | FileName  | FileSize | Version | Language | Attributs | Séquence |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Téléphone       | Phone.txt | 1 000     |         |          | 0          | 1        |



 

Comme expliqué dans la section : [utilisation de transformations pour ajouter des ressources](using-transforms-to-add-resources.md), la transformation doit ajouter un ou plusieurs nouveaux composants à la base de données d’installation pour contenir la nouvelle fonctionnalité de liste téléphonique. Utilisez votre éditeur de base de données pour ajouter l’enregistrement suivant à la [table des composants](component-table.md) de MNP2000t.msi.

Le composant téléphone doit être identifié par un [GUID](guid.md)d’ID de composant unique. Si vous reproduisez l’exemple, ne réutilisez pas le même GUID d’ID de composant que dans le tableau suivant. Utilisez plutôt un utilitaire tel que Guidgen.exe pour générer un nouveau GUID. Veillez à utiliser une chaîne GUID cohérente avec le type de données [guid](guid.md) Windows Installer.

[Table des composants](component-table.md)



| Composant | ComponentId                            | Répertoire\_ | Attributs | Condition | KeyPath   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Téléphone     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

Utilisez votre éditeur de base de données pour modifier les données dans la [table des fonctionnalités](feature-table.md) de MNP2000t.msi. Entrez 0 dans la colonne niveau de l’enregistrement de la fonctionnalité de la porte. Cela désactive la fonctionnalité de porte et ses fonctionnalités enfants et masque ces fonctionnalités de l’interface utilisateur. Notez que, étant donné que la propriété [**INSTALLLEVEL**](installlevel.md) a la valeur 3 dans la [table de propriétés](property-table.md), le programme d’installation n’installe pas les fonctionnalités avec un niveau de 0. Ajoutez un enregistrement pour la nouvelle \_ fonctionnalité de liste téléphonique.

[Tableau des fonctionnalités](feature-table.md)



| Fonctionnalité     | Parent de la fonctionnalité \_ | Intitulé         | Description                | Afficher | Level | Répertoire\_ | Attributs |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Spectacle        |                 | Spectacle          | Événements Arts au niveau du parc rouge.   | 20      | 3     | NOTEPADDIR  | 0          |
| Chaussures    | Sport           | Chaussures      | Jeux de baseball             | 17      | 3     | SPORTDIR    | 32         |
| Concert     | Spectacle            | Concert       | Événements de concert au niveau du parc rouge | 21      | 3     | ARTSDIR     | 2          |
| Jongl       | Spectacle            | Jongl         | Événements danse au niveau du parc rouge   | 23      | 3     | ARTSDIR     | 2          |
| Terrain    | Sport           | Terrain      | Jeux de football             | 19      | 3     | SPORTDIR    | 2          |
| Transistor        |                 | Transistor          | Les admissions du parc rouge      | 6       | 0     | NOTEPADDIR  | 0          |
| Aide        | Bloc-notes         | Aide          | Fichier d’aide.                 | 5       | 3     | NOTEPADDIR  | 1          |
| Janvier     | Transistor            | Janvier       | Admission de janvier         | 10      | 3     | MONDIR      | 2          |
| NewYears    | Janvier         | Nouvelle année | Premières années d’admission de jours   | 11      | 3     | HOLDIR      | 2          |
| Bloc-notes     |                 | Bloc-notes       | Éditeur de bloc-notes             | 1       | 3     | NOTEPADDIR  | 0          |
| Fichier Lisezmoi      | Bloc-notes         | Fichier Lisezmoi        | Fichier Lisez-moi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport       |                 | Événements sportifs  | Événements sportifs chez Red Park   | 14      | 3     | NOTEPADDIR  | 0          |
| \_Liste téléphonique |                 | Liste téléphonique    | Liste téléphonique                 | 24      | 3     | NOTEPADDIR  | 0          |



 

Ajoutez l’enregistrement suivant à la [table FeatureComponents](featurecomponents-table.md) de MNP2000t.msi.

[Table FeatureComponents](featurecomponents-table.md)



| Fonctionnalité\_   | -\_ |
|-------------|-------------|
| \_Liste téléphonique | Téléphone       |



 

Ajoutez un nouvel enregistrement dans la [table de raccourcis](shortcut-table.md) pour créer un raccourci vers la \_ fonctionnalité de liste téléphonique.

[Tableau de raccourcis](shortcut-table.md)



| Raccourci | Répertoire\_ | Nom      | -\_ | Cible          | Arguments | Description | Touche d’accès rapide | Icône\_ | IndexIcône | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| À la une   | MENUDIR     | Phone.txt | Téléphone       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Continuer](generating-a-customization-transform.md)

 

 



