---
description: La base de données du programme d’installation permet au développeur d’un package d’installation de contrôler le transfert d’une application d’une source à une image cible.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Utilisation de la base de données du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec91d8982a8ddac47c96303f03a33e4c85cafa70c3ef480c660df42e72f8a84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996059"
---
# <a name="using-the-installer-database"></a>Utilisation de la base de données du programme d’installation

La [base de données du programme](installer-database.md) d’installation permet au développeur d’un package d’installation de contrôler le transfert d’une application d’une source à une image cible. La disposition des images source et cible de l’application est spécifiée dans la table de [répertoires](directory-table.md) et les actions qui installent l’application sont spécifiées dans six tables de séquence :

-   Table [InstallUISequence](installuisequence-table.md)
-   Table [InstallExecuteSequence](installexecutesequence-table.md)
-   Table [AdminUISequence](adminuisequence-table.md)
-   Table [AdminExecuteSequence](adminexecutesequence-table.md)
-   Table [AdvtUISequence](advtuisequence-table.md)
-   Table [AdvtExecuteSequence](advtexecutesequence-table.md)

Les sections suivantes décrivent l’utilisation [de la base de données du programme d’installation](installer-database.md):

-   [Utilisation de la table Directory](using-the-directory-table.md)
-   [Utilisation d’une table de séquences](using-a-sequence-table.md)
-   [Obtention d’un descripteur de base de données](obtaining-a-database-handle.md)
-   [Validation des bases de données](committing-databases.md)
-   [Importation et exportation](importing-and-exporting.md)
-   [Fusion de bases de données](merging-databases.md)
-   [Attribution d’un nom aux tables, propriétés et actions personnalisées](naming-custom-tables-properties-and-actions.md)
-   [Limitations OLE sur les Flux](ole-limitations-on-streams.md)
-   [Utilisation des requêtes](working-with-queries.md)
-   [Ajout de données binaires à une table à l’aide de SQL](adding-binary-data-to-a-table-using-sql.md)
-   [Utilisation des enregistrements](working-with-records.md)
-   [Utilisation des emplacements de dossiers](working-with-folder-locations.md)
-   [Spécification de l’ordre d’inscription automatique](specifying-the-order-of-self-registration.md)
-   [Mesures de conditionnement à exécuter pendant la suppression](conditioning-actions-to-run-during-removal.md)
-   [Appel de fonctions de base de données à partir de programmes](calling-database-functions-from-programs.md)
-   [Syntaxe d’instruction conditionnelle](conditional-statement-syntax.md)
-   [Format de définition de colonne](column-definition-format.md)
-   [Déterminer si une colonne est une clé primaire ou externe](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



