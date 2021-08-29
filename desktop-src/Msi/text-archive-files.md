---
description: les tables de base de données Windows Installer peuvent être exportées vers des fichiers texte ASCII à l’aide de MsiDatabaseExport ou de la méthode d’exportation de l’objet de base de données.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Fichiers d’archive de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc232f5523613d62ca595ec55983aeaf9cee8d67408a66b7afb609fa75b69125
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626419"
---
# <a name="text-archive-files"></a>Fichiers d’archive de texte

les tables de base de données Windows Installer peuvent être exportées vers des fichiers texte ASCII à l’aide de [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) ou de la méthode d' [**exportation**](database-export.md) de l’objet [**de base de données**](database-object.md) . les informations contenues dans ces fichiers d’archive de texte peuvent ensuite être réimportées dans une base de données Windows Installer à l’aide de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) ou de la méthode d' [importation](database-import.md) de l’objet **de base de données** .

Les outils tels que les [msidb.exe](msidb-exe.md) sont en mesure d’exporter et d’importer des fichiers d’archive de texte. consultez [exporter](export-files.md) des fichiers et [importer des fichiers](import-files.md) pour obtenir des exemples de [script Windows Installer](windows-installer-scripting-examples.md) qui peuvent exporter et importer des fichiers d’archive de texte à partir d’une base de données.

> [!Note]  
> Les fichiers d’archive de texte ne sont pas destinés à modifier la base de données d’installation. pour créer et modifier un package d’installation, vous devez utiliser un outil de modification de table Windows Installer, tel qu' [Orca](orca-exe.md) ou un outil tiers.

 

Les fichiers d’archive de texte peuvent être utilisés dans les cas suivants.

-   Les fichiers d’archive de texte peuvent être utilisés avec les systèmes de gestion de version.
-   Pour supprimer l’espace de stockage gaspillé et réduire la taille finale des fichiers de .msi. Consultez [réduction de la taille d’un fichier de .msi](reducing-the-size-of-an--msi-file.md).
-   Pour ajouter des informations de localisation à une base de données d’installation. Pour plus d’informations, consultez [gestion des pages de codes des tables importées et exportées](code-page-handling-of-imported-and-exported-tables.md).

-   Pour déterminer la page de codes d’une base de données. Consultez [détermination de la page de codes d’une base de données d’installation](determining-an-installation-database-s-code-page.md).
-   Pour définir la page de codes d’une base de données. Consultez [définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md).
-   Pour augmenter la limite d’une colonne de base de données. Exportez la table à l’aide de [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), modifiez le fichier. IDT exporté, puis importez la table à l’aide de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Les auteurs ne peuvent pas modifier les types de données de colonne, les valeurs null ou les attributs de localisation des colonnes dans les tables standard. Consultez également [création d’un package volumineux](authoring-a-large-package.md).

Les pages suivantes décrivent les pages d’archive de texte et leurs formats.

-   [Format de fichier d’archive](archive-file-format.md)
-   [Données ASCII dans les fichiers d’archive de texte](ascii-data-in-text-archive-files.md)
-   [\_ForceCodepage](-forcecodepage.md)
-   [\_SummaryInformation](-summaryinformation.md)

 

 



