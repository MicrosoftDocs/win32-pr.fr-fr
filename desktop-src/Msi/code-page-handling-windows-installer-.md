---
description: L’Windows Installer stocke toutes les chaînes de base de données dans un seul pool de chaînes partagé pour réduire la taille de la base de données et améliorer les performances. Pour obtenir la liste des pages de codes numériques, consultez localisation des tables Error et ActionText.
ms.assetid: 5d413fb7-99da-49f3-ace3-ec285df2e634
title: Gestion des pages de codes (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db2788a1bfc6bdb49ec1402d5bba8a1a2594b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524075"
---
# <a name="code-page-handling-windows-installer"></a>Gestion des pages de codes (Windows Installer)

L’Windows Installer stocke toutes les chaînes de base de données dans un seul pool de chaînes partagé pour réduire la taille de la base de données et améliorer les performances. Pour obtenir la liste des pages de codes numériques, consultez [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md).

Pour plus d’informations, [détermination de la page de codes d’une base de données d’installation](determining-an-installation-database-s-code-page.md).

Windows Installer utilise [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) pour déterminer si la page de codes est valide.

### <a name="localizing-a-windows-installer-package"></a>Localisation d’un package Windows Installer

Si vous localisez un package de Windows Installer, il peut impliquer la modification des informations dans les tables de base de données, l’exportation des tables vers des fichiers d’archive de texte ANSI, puis l’importation des fichiers d’archive dans la base de données localisée. Vous pouvez également ajouter des modifications de localisation à une base de données à l’aide d’un éditeur de table de base de données ou [de fonctions de base de données](database-functions.md). Il est important de définir la page de codes de la base de données qui est localisée avant d’apporter des modifications de localisation à la base de données. Ne définissez pas la page de codes de la base de données après la localisation de la base de données, car cela peut corrompre les caractères étendus. Pour plus d’informations, consultez [définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md).

L’approche recommandée pour gérer les pages de codes consiste à créer une base de données neutre qui contient uniquement des caractères qui peuvent être traduits dans une page de codes. Pour plus d’informations, consultez [création d’une base de données à l’aide d’une page de codes neutre](creating-a-database-with-a-neutral-code-page.md).

Si vous ajoutez des informations de localisation à des fichiers d’archive de base de données, vous pouvez utiliser [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) pour exporter des tables à partir d’une base de données qui contient des modifications de localisation vers des fichiers d’archive de texte ANSI, puis les importer dans la base de données localisée avec [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). La page de codes d’un fichier d’archive exporté est toujours la même que la base de données parente. Les pages de codes d’un fichier importé et la base de données qui reçoit le fichier doivent être identiques, ou au moins l’une des deux pages de codes doit être neutre. Pour plus d’informations, consultez [gestion des pages de codes des tables importées et exportées](code-page-handling-of-imported-and-exported-tables.md).

Si vous ajoutez des informations de localisation à l’aide d’un éditeur de texte ou si les [fonctions de base de données](database-functions.md) veillent uniquement à passer des paramètres de chaîne à l’API Windows Installer qui utilise la page de codes de la base de données localisée. Si un paramètre de chaîne contient des caractères qui ne sont pas représentés par la page de codes de la base de données, une erreur se produit lors de l’appel de [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Pour plus d’informations, consultez [gestion des pages de codes des chaînes de paramètres](code-page-handling-of-parameter-strings.md).

Si un package est utilisé pour installer plusieurs versions linguistiques d’un produit, la transformation utilisée pour localiser les chaînes peut également modifier la page de codes de la base de données.

 

 
