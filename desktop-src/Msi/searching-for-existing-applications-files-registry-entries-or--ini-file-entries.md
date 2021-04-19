---
description: Windows Installer pouvez rechercher un fichier ou un répertoire spécifique pendant une installation. Les recherches de fichiers ou de répertoires permettent de déterminer si un utilisateur a déjà installé une version d’une application.
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: Recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41d0ebf8943d1fb82b7c0901a62230e6befdcba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529228"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a>Recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants

Windows Installer pouvez rechercher un fichier ou un répertoire spécifique pendant une installation. Les recherches de fichiers ou de répertoires permettent de déterminer si un utilisateur a déjà installé une version d’une application.

L' [action AppSearch](appsearch-action.md) recherche dans un système utilisateur les signatures de fichiers qui sont spécifiées dans la [table AppSearch](appsearch-table.md). Si l’action AppSearch trouve un fichier ou un répertoire installé avec la signature spécifiée, elle définit une propriété correspondante, également spécifiée dans la table AppSearch, à l’emplacement du fichier ou du répertoire. Lors de la recherche d’un fichier, la signature de fichier doit également figurer dans la [table de signatures](signature-table.md). Si une signature de fichier figure dans la table AppSearch et ne figure pas dans la table de signatures, la recherche recherche un répertoire, une entrée de registre ou une entrée de fichier. ini.

Pour accélérer la recherche d’un ordinateur utilisateur, le programme d’installation interroge les tables de base de données de localisation suivantes dans l’ordre indiqué pour un emplacement de recherche suggéré :

-   Si la signature de fichier est indiquée dans le [tableau CompLocator](complocator-table.md), l’emplacement de recherche suggéré est le chemin d’accès de clé d’un composant. Si la signature n’est pas indiquée dans ce tableau ou n’est pas installée à l’emplacement suggéré, le programme d’installation interroge la [table RegLocator](reglocator-table.md) à la recherche d’un emplacement suggéré.
-   Si la signature de fichier est indiquée dans le [tableau RegLocator](reglocator-table.md), l’emplacement de recherche suggéré est un chemin d’accès de clé écrit dans le registre de l’utilisateur. Si la signature n’est pas indiquée dans ce tableau ou n’est pas installée à l’emplacement suggéré, le programme d’installation interroge la [table IniLocator](inilocator-table.md) à la recherche d’un emplacement suggéré.
-   Si la signature de fichier est indiquée dans le [tableau IniLocator](inilocator-table.md), l’emplacement de recherche suggéré est un chemin d’accès de clé écrit dans un fichier. ini qui se trouve dans le répertoire Windows par défaut d’un système utilisateur. Si la signature n’est pas indiquée dans ce tableau ou n’est pas installée à l’emplacement suggéré, le programme d’installation interroge la [table DrLocator](drlocator-table.md) à la recherche d’un emplacement suggéré.
-   Si la signature de fichier figure dans la [table DrLocator](drlocator-table.md), l’emplacement de recherche suggéré est un chemin d’accès dans l’arborescence de répertoires de l’utilisateur. La profondeur des niveaux de sous-répertoires à rechercher sous cet emplacement est également spécifiée dans ce tableau.

La première fois que le programme d’installation trouve la signature de fichier à un emplacement suggéré, il cesse de Rechercher ce fichier ou ce répertoire et définit la propriété correspondante dans la [table AppSearch](appsearch-table.md). Pour plus d’informations, consultez les rubriques suivantes :

-   [Recherche d’un fichier sur tous les lecteurs fixes](searching-all-fixed-drives-for-a-file.md)
-   [Recherche d’un répertoire et d’un fichier dans le répertoire](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [Recherche d’un fichier et création d’une propriété contenant le chemin d’accès du fichier](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [Recherche d’un fichier dans un emplacement spécifique](searching-for-a-file-in-a-specific-location.md)
-   [Recherche d’une entrée de Registre et création d’une propriété contenant la valeur du Registre](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 



