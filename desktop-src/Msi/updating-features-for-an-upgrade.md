---
description: L’exemple de package de mise à niveau Windows Installer ajoute de nouvelles fonctionnalités au produit d’origine.
ms.assetid: cbc4c2ff-e08b-4ebb-a306-a80f9a6e4360
title: Mise à jour des fonctionnalités pour une mise à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af072618bd0a2ba16a7f098d6b1129ba17c27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535458"
---
# <a name="updating-features-for-an-upgrade"></a>Mise à jour des fonctionnalités pour une mise à niveau

L’exemple de package de mise à niveau ajoute trois nouvelles fonctionnalités au produit d’origine :

-   Basket-ball, nouvelle fonctionnalité enfant de la fonctionnalité sport.
-   Opera, nouvelle fonctionnalité enfant de la fonctionnalité Arts.
-   Le souvenir, une nouvelle fonctionnalité enfant de la fonctionnalité de porte.

Utilisez votre éditeur de base de données pour ouvrir MNP2001.msi et entrez les données suivantes dans la [table des fonctionnalités](feature-table.md).

[Tableau des fonctionnalités](feature-table.md)



| Fonctionnalité    | Parent de la fonctionnalité \_ | Intitulé         | Description                | Afficher | Level | Répertoire\_ | Attributs |
|------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Spectacle       |                 | Spectacle          | Événements Arts au niveau du parc rouge.   | 18      | 3     | NOTEPADDIR  | 0          |
| Chaussures   | Sport           | Chaussures      | Jeux de baseball             | 17      | 3     | SPORTDIR    | 32         |
| Concert    | Spectacle            | Concert       | Événements de concert au niveau du parc rouge | 19      | 3     | ARTSDIR     | 2          |
| Jongl      | Spectacle            | Jongl         | Événements danse au niveau du parc rouge   | 21      | 3     | ARTSDIR     | 2          |
| Terrain   | Sport           | Terrain      | Jeux de football             | 13      | 3     | SPORTDIR    | 2          |
| Transistor       |                 | Transistor          | Les admissions du parc rouge      | 6       | 3     | NOTEPADDIR  | 0          |
| Aide       | Bloc-notes         | Aide          | Fichier d’aide.                 | 5       | 3     | NOTEPADDIR  | 1          |
| Janvier    | Transistor            | Janvier       | Admission de janvier         | 7       | 3     | MONDIR      | 2          |
| NewYears   | Janvier         | Nouvelle année | Premières années d’admission de jours   | 9       | 3     | HOLDIR      | 2          |
| Bloc-notes    |                 | Bloc-notes       | Éditeur de bloc-notes             | 1       | 3     | NOTEPADDIR  | 0          |
| Fichier Lisezmoi     | Bloc-notes         | Fichier Lisezmoi        | Fichier Lisez-moi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport      |                 | Événements sportifs  | Événements sportifs chez Red Park   | 12      | 3     | NOTEPADDIR  | 0          |
| Isole | Sport           | Isole    | Jeux de basket           | 15      | 3     | SPORTDIR    | 2          |
| Opera      | Spectacle            | Opera         | Performances Opera         | 23      | 3     | ARTSDIR     | 2          |
| Souvenir   | Transistor            | Jour du souvenir  | Admission du jour du souvenir    | 11      | 3     | HOLDIR      | 2          |



 

Utilisez votre éditeur de base de données pour ouvrir MNP2001.msi et entrez les données suivantes dans la [table FeatureComponents](featurecomponents-table.md)vide.



| Fonctionnalité\_  | -\_ |
|------------|-------------|
| Chaussures   | Chaussures    |
| Concert    | Concert     |
| Jongl      | Jongl       |
| Terrain   | Terrain    |
| Aide       | Aide        |
| Janvier    | Janvier     |
| NewYears   | NewYears    |
| Bloc-notes    | Bloc-notes     |
| Fichier Lisezmoi     | Bloc-notes     |
| Isole | Isole  |
| Opera      | Opera       |
| Souvenir   | Souvenir    |



 

[Continuer](updating-shortcuts-for-an-upgrade.md)

 

 



