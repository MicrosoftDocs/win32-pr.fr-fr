---
description: Le programme d’installation conserve les informations sur la structure du répertoire d’installation dans la table du répertoire.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Spécification de la structure de répertoires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862909"
---
# <a name="specifying-directory-structure"></a>Spécification de la structure de répertoires

Le programme d’installation conserve les informations sur la structure du répertoire d’installation dans la [table du répertoire](directory-table.md). Consultez le [groupe tables principales](core-tables-group.md). Dans cette section, vous allez ajouter des informations sur la structure de répertoires de l’exemple Notepad à la base de données vide que vous avez créée lors de l' [importation d’une base de données vide](importing-a-blank-database.md). Utilisez l’éditeur de base de données Orca fourni avec le kit de développement logiciel (SDK), ou un autre éditeur, pour ouvrir la table de répertoires dans MNP2000.msi. Utilisez l’éditeur pour entrer les données suivantes dans la table de répertoires vide.

[Table de répertoire](directory-table.md)



| Répertoire                                        | Répertoire \_ parent                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | Arts : événements       |
| HOLDIR                                           | MONDIR                                           | . : Jours fériés        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIR                                           | NOTEPADDIR                                       | Transistor              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | \_Parc rouge : bloc-notes |
| SPORTDIR                                         | NOTEPADDIR                                       | Sports : événements     |



 

L’entrée de ces données dans la table Directory spécifie les structures de répertoire source et cible. Consultez la [table Directory](directory-table.md) et [Utilisez les rubriques de la table Directory](using-the-directory-table.md) . Notez que la propriété [**targetDir**](targetdir.md) doit être le nom d’une racine dans la table des répertoires de chaque installation.

[Continuer](specifying-components.md)

 

 



