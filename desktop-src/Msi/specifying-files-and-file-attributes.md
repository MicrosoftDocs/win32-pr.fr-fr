---
description: l’installation et la suppression de chaque fichier sont déterminées par le composant Windows Installer qui contrôle le fichier.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Spécification des fichiers et des attributs de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdb63bf2779ddc5730013bad06b382c168a62bab5e897d5d621f7a65644e445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893729"
---
# <a name="specifying-files-and-file-attributes"></a>Spécification des fichiers et des attributs de fichier

l’installation et la suppression de chaque fichier sont déterminées par le [composant Windows Installer](windows-installer-components.md) qui contrôle le fichier. Une fois que le regroupement de ressources en composants a été spécifié, les informations d’attribut de fichier peuvent être ajoutées à la base de données d’installation. dans cette section, vous allez ajouter des informations de fichier à la base de données d’installation pour l’exemple Bloc-notes. Consultez le [groupe tables de fichiers](file-tables-group.md).

les fichiers de l’exemple de Bloc-notes sont décompressés. Pour plus d’informations sur l’ajout de fichiers CAB à des packages, consultez sources compressées [et non compressées](compressed-and-uncompressed-sources.md) . Cet exemple ne contient pas d’informations sur le contrôle de version de fichier. Pour plus d’informations sur le contrôle de version de fichier, consultez règles de contrôle de [version de fichier](file-versioning-rules.md) et contrôle de [version de fichier par défaut](default-file-versioning.md).

Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table de fichiers vide.

[Table de fichier](file-table.md)



| Fichier         | Composant\_ | FileName     | FileSize | Version | Langage | Attributs | Séquence |
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

 

 



