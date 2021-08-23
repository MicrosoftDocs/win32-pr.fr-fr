---
description: Vous pouvez ajouter des informations de localisation à une base de données d’installation en important et en exportant des fichiers d’archive de texte ASCII à l’aide de MsiDatabaseExport et MsiDatabaseImport.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Gestion des pages de codes des tables importées et exportées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9a64617ccfda25380076d62e6dd4ad8c18c55f68afd0236b3258638c899f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065999"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a>Gestion des pages de codes des tables importées et exportées

Vous pouvez ajouter des informations de localisation à une base de données d’installation en important et en exportant des fichiers d’archive de texte ASCII à l’aide de [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) et [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Étant donné que le pool de chaînes de base de données utilise une page de codes ANSI, la base de données et les [fichiers d’archive de texte](text-archive-files.md) exportés ont des pages de codes.

Lorsqu’un [fichier d’archive de texte](text-archive-files.md) est exporté à partir d’une base de données, la page de codes du fichier d’archive est la même que la base de données parente. Pour obtenir la liste des pages de codes numériques, consultez [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md).

> [!Note]  
> L’exportation d’une table dans un fichier d’archive de texte traduit les caractères de contrôle pour éviter les conflits avec les délimiteurs de fichiers.

 

## <a name="ascii-text-archive-files"></a>Fichiers d’archive de texte ASCII

Les [fichiers d’archive de texte](text-archive-files.md) ASCII exportés par [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) sont expliqués dans le format suivant :

-   Les noms des colonnes de la table sont écrits sur la première ligne.
-   Les formats de colonne sont écrits sur la deuxième ligne.
-   Si la table contient uniquement des données ASCII, la troisième ligne du fichier texte est le nom de la table suivi d’une liste de clés primaires.
-   Si la table contient des données non-ASCII et que la base de données est marquée avec une page de codes numérique, le numéro de la page de codes apparaît au début de la troisième ligne.
-   Si la base de données contient des données non-ASCII, mais que la base de données n’est pas marquée avec la page de codes numérique, le numéro de page de codes système actuel est écrit au début de la troisième ligne.
-   Les lignes restantes du fichier texte sont les données de la page de codes spécifiée.
-   Si une table contient des flux, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exporte chaque flux de la table dans un fichier séparé.

### <a name="neutral-and-non-neutral-code-pages"></a>Pages de codes neutres et non neutres

Vous pouvez faciliter la localisation en commençant par une base de données qui contient une page de codes neutre :

-   Une base de données vide contient une page de codes neutre.
-   Une base de données qui ne contient pas de caractères étendus qui nécessitent une page de codes à représenter en ASCII a une page de codes neutre.

Pour plus d’informations, consultez [création d’une base de données à l’aide d’une page de codes neutre](creating-a-database-with-a-neutral-code-page.md).

Les pages de codes neutres et non neutres présentent les caractéristiques suivantes :

-   Si un [fichier d’archive de texte](text-archive-files.md) avec une page de codes non neutre est importé dans une base de données dont la page de codes n’est pas neutre, le programme d’installation renvoie une erreur lors de l’appel de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) .
-   Un [fichier d’archive de texte](text-archive-files.md) contenant une page de codes neutre peut être importé dans une base de données qui contient une page de codes.
-   Un [fichier d’archive de texte](text-archive-files.md) contenant une page de codes peut être importé dans une base de données qui contient une page de codes neutre.
-   L’importation d’un [fichier d’archive de texte](text-archive-files.md) dans une base de données à l’aide d’une page de codes neutre définit la page de codes de la base de données sur la page de codes du fichier d’archive. Tous les fichiers d’archive qui sont ensuite importés dans la base de données doivent avoir la même page de codes que le premier fichier.

Pour plus d’informations, consultez la [page détermination d’une page de codes de base de données d’installation](determining-an-installation-database-s-code-page.md) et [définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md).

Les [fichiers d’archive de texte](text-archive-files.md) qui sont exportés par [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) peuvent être utilisés avec les systèmes de gestion de version. Utilisez les [fonctions de base de données](database-functions.md) ou un éditeur de table de base de données pour modifier la base de données.

vous pouvez ajouter des informations de localisation à une base de données d’installation à l’aide d’un éditeur de table de base de données ou de l’API Windows Installer. Pour plus d’informations, consultez [gestion des pages de codes des chaînes de paramètres](code-page-handling-of-parameter-strings.md).

 

 



