---
description: Respectez ces recommandations pour faciliter la localisation des packages Windows Installer.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Préparation d’un package de Windows Installer pour la localisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515962"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>Préparation d’un package de Windows Installer pour la localisation

La localisation d’un package Windows Installer dans plusieurs langues peut être simplifiée en procédant comme suit :

-   Créer une base de données d’installation de base qui est indépendante de la page de codes. Consultez [création d’une base de données à l’aide d’une page de codes neutre](creating-a-database-with-a-neutral-code-page.md). La page de codes de la base de données localisée peut ensuite être définie par l’importation d’une table d’archive de texte avec une page de codes non neutre dans la base de données de base. Consultez [définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md).
-   Organisez les fichiers nécessitant une localisation dans des composants distincts et installez ces fichiers dans des répertoires distincts. Cela permet de s’assurer que deux packages localisés n’installent jamais des fichiers portant le même nom dans le même répertoire.

Par exemple, une application dans le monde entier utilisant les ressources suivantes peut avoir trois composants.



| Composant | Ressource                   |
|-----------|----------------------------|
| RÉELLES     | worldwide.exe              |
| RÉELLES     | entrées de Registre mondiales |
| RÉELLES     | raccourci dans le monde entier         |
| FR       | engui.dll                  |
| FR       | readme.txt                 |
| FRA       | fraui.dll                  |
| FRA       | readme.txt                 |



 

Les fichiers qui doivent être localisés peuvent être installés dans les emplacements de répertoire suivants :

-   \[\] \\worldwide.exe du monde de ProgramFilesFolder \\
-   \[engui.dll de l’anglais du monde de l' \] \\ \\ anglais \\
-   \[readme.txt de l’anglais du monde de l' \] \\ \\ anglais \\
-   \[fraui.dll de la \] \\ planète universelle de l' \\ anglais \\
-   \[readme.txt de la \] \\ planète universelle de l' \\ anglais \\

 

 



