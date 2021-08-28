---
description: respectez ces recommandations pour faciliter la localisation des packages Windows Installer.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: préparation d’un Package de Windows Installer pour la localisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e9a1ce06e74197dc8844622861a1f42252deae8b96d3ce57ea852673818de3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129159"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>préparation d’un Package de Windows Installer pour la localisation

la localisation d’un package Windows Installer dans plusieurs langues peut être simplifiée en procédant comme suit :

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

 

 



