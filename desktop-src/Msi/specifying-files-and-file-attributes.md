---
description: L’installation et la suppression de chaque fichier sont déterminées par le composant Windows Installer qui contrôle le fichier.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Spécification des fichiers et des attributs de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719dacbc434d47b4074a183e67edb02a88cb3c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531892"
---
# <a name="specifying-files-and-file-attributes"></a>Spécification des fichiers et des attributs de fichier

L’installation et la suppression de chaque fichier sont déterminées par le [composant Windows Installer](windows-installer-components.md) qui contrôle le fichier. Une fois que le regroupement de ressources en composants a été spécifié, les informations d’attribut de fichier peuvent être ajoutées à la base de données d’installation. Dans cette section, vous allez ajouter des informations de fichier à la base de données d’installation de l’exemple du bloc-notes. Consultez le [groupe tables de fichiers](file-tables-group.md).

Les fichiers de l’exemple du bloc-notes ne sont pas compressés. Pour plus d’informations sur l’ajout de fichiers CAB à des packages, consultez sources compressées [et non compressées](compressed-and-uncompressed-sources.md) . Cet exemple ne contient pas d’informations sur le contrôle de version de fichier. Pour plus d’informations sur le contrôle de version de fichier, consultez règles de contrôle de [version de fichier](file-versioning-rules.md) et contrôle de [version de fichier par défaut](default-file-versioning.md).

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table de fichiers vide.

[Table de fichier](file-table.md)



| Fichier         | -\_ | FileName     | FileSize | Version | Language | Attributs | Séquence |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Chaussures    | Baseball.txt | 1 000     |         |          | 0          | 1        |
| Concert.txt  | Concert     | Concert.txt  | 1 000     |         |          | 0          | 1        |
| Dance.txt    | Jongl       | Dance.txt    | 1 000     |         |          | 0          | 1        |
| Football.txt | Terrain    | Football.txt | 1 000     |         |          | 0          | 1        |
| Help.txt     | Aide        | Help.txt     | 1 000     |         |          | 0          | 1        |
| January.txt  | Janvier     | January.txt  | 1 000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1 000     |         |          | 0          | 1        |
| Redpark.exe  | Bloc-notes     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Lisezmoi.txt   | Bloc-notes     | Lisezmoi.txt   | 1 000     |         |          | 0          | 1        |



 

[Continuer](specifying-source-media.md)

 

 



