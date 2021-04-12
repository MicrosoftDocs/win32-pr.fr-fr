---
description: Le programme d’installation de Microsoft permet aux utilisateurs d’installer et de supprimer des blocs de fonctionnalités d’application appelés fonctionnalités Windows Installer.
ms.assetid: 88268c5c-57c5-49f8-92df-1ad8f30a70c2
title: Spécification des fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf7463b30247e921fb440ada1cd6f00f8e96a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203189"
---
# <a name="specifying-features"></a>Spécification des fonctionnalités

Le programme d’installation de Microsoft permet aux utilisateurs d’installer et de supprimer des blocs de fonctionnalités d’application appelés [fonctionnalités Windows Installer](windows-installer-features.md). Dans cette section, vous allez ajouter des informations à la base de données d’installation concernant les fonctionnalités disponibles pour l’exemple du bloc-notes. Pour plus d’informations, consultez [groupe de tables principales](core-tables-group.md) et [composants et fonctionnalités](components-and-features.md).

L’exemple du bloc-notes installe les fonctionnalités dans une hiérarchie de fonctionnalités parent et enfant. Dans la liste suivante, les fonctionnalités enfants sont mises en retrait par rapport à leur fonctionnalité parente. Les fonctionnalités doivent s’afficher dans cet ordre dans le [contrôle SelectionTree](selectiontree-control.md) de l’interface utilisateur.

Bloc-notes

-   Fichier Lisezmoi
-   Aide

Transistor

-   Janvier
    -   NewYears

Sport

-   Chaussures
-   Terrain

Spectacle

-   Concert
-   Jongl

Utilisez un éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la [table des fonctionnalités](feature-table.md)vide.



| Fonctionnalité  | Parent de la fonctionnalité \_ | Intitulé         | Description                | Afficher | Level | Répertoire\_ | Attributs |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Spectacle     |                 | Spectacle          | Événements Arts au niveau du parc rouge.   | 20      | 3     | NOTEPADDIR  | 0          |
| Chaussures | Sport           | Chaussures      | Jeux de baseball             | 17      | 3     | SPORTDIR    | 32         |
| Concert  | Spectacle            | Concert       | Événements de concert au niveau du parc rouge | 21      | 3     | ARTSDIR     | 2          |
| Jongl    | Spectacle            | Jongl         | Événements danse au niveau du parc rouge   | 23      | 3     | ARTSDIR     | 2          |
| Terrain | Sport           | Terrain      | Jeux de football             | 19      | 3     | SPORTDIR    | 2          |
| Transistor     |                 | Transistor          | Les admissions du parc rouge      | 6       | 3     | NOTEPADDIR  | 0          |
| Aide     | Bloc-notes         | Aide          | Fichier d’aide.                 | 5       | 3     | NOTEPADDIR  | 1          |
| Janvier  | Transistor            | Janvier       | Admission de janvier         | 10      | 3     | MONDIR      | 2          |
| NewYears | Janvier         | Nouvelle année | Premières années d’admission de jours   | 11      | 3     | HOLDIR      | 2          |
| Bloc-notes  |                 | Bloc-notes       | Éditeur de bloc-notes             | 1       | 3     | NOTEPADDIR  | 0          |
| Fichier Lisezmoi   | Bloc-notes         | Fichier Lisezmoi        | Fichier Lisez-moi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport    |                 | Événements sportifs  | Événements sportifs chez Red Park   | 14      | 3     | NOTEPADDIR  | 0          |



 

[Continuer](specifying-feature-component-relationships.md)

 

 



