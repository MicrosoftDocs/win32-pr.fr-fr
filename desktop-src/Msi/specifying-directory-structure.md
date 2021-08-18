---
description: Le programme d’installation conserve les informations sur la structure du répertoire d’installation dans la table du répertoire.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Spécification de la structure de répertoires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc71e448c03a7fdbdf9de249122246aaf0038769a1dd409551330a503be7e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627889"
---
# <a name="specifying-directory-structure"></a>Spécification de la structure de répertoires

Le programme d’installation conserve les informations sur la structure du répertoire d’installation dans la [table du répertoire](directory-table.md). Consultez le [groupe tables principales](core-tables-group.md). dans cette section, vous allez ajouter des informations de structure de répertoires pour l’exemple de Bloc-notes à la base de données vide que vous avez créée lors de l' [importation d’une base de données vide](importing-a-blank-database.md). Utilisez l’éditeur de base de données Orca fourni avec le kit de développement logiciel (SDK), ou un autre éditeur, pour ouvrir la table de répertoires dans MNP2000.msi. Utilisez l’éditeur pour entrer les données suivantes dans la table de répertoires vide.

[Table de répertoire](directory-table.md)



| Répertoire                                        | Répertoire \_ parent                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | Arts : événements       |
| HOLDIR                                           | MONDIR                                           | . : Jours fériés        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIR                                           | NOTEPADDIR                                       | Porte              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | \_parc rouge : Bloc-notes |
| SPORTDIR                                         | NOTEPADDIR                                       | Sports : événements     |



 

L’entrée de ces données dans la table Directory spécifie les structures de répertoire source et cible. Consultez la [table Directory](directory-table.md) et [Utilisez les rubriques de la table Directory](using-the-directory-table.md) . Notez que la propriété [**targetDir**](targetdir.md) doit être le nom d’une racine dans la table des répertoires de chaque installation.

[Continuer](specifying-components.md)

 

 



