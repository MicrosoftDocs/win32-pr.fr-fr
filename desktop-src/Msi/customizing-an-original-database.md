---
description: effectuez une copie de l’exemple de package d’installation Windows Installer MNP2000.msi et renommez cette copie MNP2000t.msi.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Personnalisation d’une base de données d’origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f02f176bb24b1792d9184ebc662a45c9dbfdb8df385b3fb481967c9c8a099a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075039"
---
# <a name="customizing-an-original-database"></a>Personnalisation d’une base de données d’origine

effectuez une copie de l’exemple de package d’installation Windows Installer MNP2000.msi et renommez cette copie MNP2000t.msi. Dans les étapes suivantes, vous allez personnaliser ce fichier à l’aide d’un éditeur de tables de base de données comme Orca, qui est fourni avec le kit de développement logiciel (SDK) ou un autre éditeur de base de données.

incluez le nouveau fichier de ressources pour la liste téléphonique, Phone.txt, dans le dossier Bloc-notes avec les autres fichiers sources.



| Fichier      | Description                             | Chemin de la source                 | Chemin d’accès à la cible                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | ressource pour la fonctionnalité de \_ liste Téléphone. | C : \\ exemple de \\ Bloc-notes \\phone.txt | \[\] \\phone.txt de \_ parc \\ rouge d’ProgramFilesFolder |



 

Utilisez votre éditeur de base de données pour ajouter un enregistrement à la [table de fichiers](file-table.md) de MNP2000t.msi pour le nouveau fichier.

[Table de fichier](file-table.md)



| Fichier      | Composant\_ | FileName  | FileSize | Version | Langage | Attributs | Séquence |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Téléphone       | Phone.txt | 1 000     |         |          | 0          | 1        |



 

Comme expliqué dans la section : [utilisation de transformations pour ajouter des ressources](using-transforms-to-add-resources.md), la transformation doit ajouter un ou plusieurs nouveaux composants à la base de données d’installation pour contenir la nouvelle fonctionnalité de liste téléphonique. Utilisez votre éditeur de base de données pour ajouter l’enregistrement suivant à la [table des composants](component-table.md) de MNP2000t.msi.

le composant Téléphone doit être identifié par un [GUID](guid.md)d’ID de composant unique. Si vous reproduisez l’exemple, ne réutilisez pas le même GUID d’ID de composant que dans le tableau suivant. Utilisez plutôt un utilitaire tel que Guidgen.exe pour générer un nouveau GUID. veillez à utiliser une chaîne guid cohérente avec le type de données [guid](guid.md) Windows Installer.

[Table des composants](component-table.md)



| Composant | ComponentId                            | Répertoire\_ | Attributs | Condition | KeyPath   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Téléphone     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

Utilisez votre éditeur de base de données pour modifier les données dans la [table des fonctionnalités](feature-table.md) de MNP2000t.msi. Entrez 0 dans la colonne niveau de l’enregistrement de la fonctionnalité de la porte. Cela désactive la fonctionnalité de porte et ses fonctionnalités enfants et masque ces fonctionnalités de l’interface utilisateur. Notez que, étant donné que la propriété [**INSTALLLEVEL**](installlevel.md) a la valeur 3 dans la [table de propriétés](property-table.md), le programme d’installation n’installe pas les fonctionnalités avec un niveau de 0. ajoutez un enregistrement pour la nouvelle fonctionnalité de liste de Téléphone \_ .

[Tableau des fonctionnalités](feature-table.md)



| Fonctionnalité     | Parent de la fonctionnalité \_ | Titre         | Description                | Affichage | Niveau | Répertoire\_ | Attributs |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Spectacle        |                 | Spectacle          | Événements Arts au niveau du parc rouge.   | 20      | 3     | NOTEPADDIR  | 0          |
| Chaussures    | Sport           | Chaussures      | Jeux de baseball             | 17      | 3     | SPORTDIR    | 32         |
| Concert     | Spectacle            | Concert       | Événements de concert au niveau du parc rouge | 21      | 3     | ARTSDIR     | 2          |
| Jongl       | Spectacle            | Jongl         | Événements danse au niveau du parc rouge   | 23      | 3     | ARTSDIR     | 2          |
| Terrain    | Sport           | Terrain      | Jeux de football             | 19      | 3     | SPORTDIR    | 2          |
| Porte        |                 | Porte          | Les admissions du parc rouge      | 6       | 0     | NOTEPADDIR  | 0          |
| Aide        | Bloc-notes         | Aide          | Fichier d’aide.                 | 5       | 3     | NOTEPADDIR  | 1          |
| Janvier     | Porte            | Janvier       | Admission de janvier         | 10      | 3     | MONDIR      | 2          |
| NewYears    | Janvier         | Nouvelle année | Premières années d’admission de jours   | 11      | 3     | HOLDIR      | 2          |
| Bloc-notes     |                 | Bloc-notes       | Bloc-notes Éditeurs             | 1       | 3     | NOTEPADDIR  | 0          |
| Fichier Lisezmoi      | Bloc-notes         | Fichier Lisezmoi        | Fichier Lisez-moi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport       |                 | Événements sportifs  | Événements sportifs chez Red Park   | 14      | 3     | NOTEPADDIR  | 0          |
| Téléphone \_ Tarifs |                 | Téléphone Tarifs    | Téléphone Tarifs                 | 24      | 3     | NOTEPADDIR  | 0          |



 

Ajoutez l’enregistrement suivant à la [table FeatureComponents](featurecomponents-table.md) de MNP2000t.msi.

[Table FeatureComponents](featurecomponents-table.md)



| Fonctionnalité\_   | Composant\_ |
|-------------|-------------|
| Téléphone \_ Tarifs | Téléphone       |



 

ajoutez un nouvel enregistrement dans la [table de raccourcis](shortcut-table.md) pour créer un raccourci vers la \_ fonctionnalité de liste de Téléphone.

[Tableau de raccourcis](shortcut-table.md)



| Raccourci | Répertoire\_ | Nom      | Composant\_ | Cible          | Arguments | Description | Touche d’accès rapide | Située\_ | IndexIcône | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| À la une   | MENUDIR     | Phone.txt | Téléphone       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Continuer](generating-a-customization-transform.md)

 

 



