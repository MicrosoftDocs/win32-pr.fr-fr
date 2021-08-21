---
description: Étant donné que la mise à niveau met à jour les fichiers utilisés par l’application, vous devez modifier la table de fichiers de la base de données.
ms.assetid: 65a7ae86-b426-4dd4-8cf5-f905dc2a1727
title: Mise à jour des fichiers et des attributs de fichier pour une mise à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c56560432a18746b31e3bb983be1f465199c51b15601c3dfd47911fe7f6ab4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809889"
---
# <a name="updating-files-and-file-attributes-for-an-upgrade"></a>Mise à jour des fichiers et des attributs de fichier pour une mise à niveau

Étant donné que la mise à niveau met à jour les fichiers utilisés par l’application, vous devez modifier la [table de fichiers](file-table.md) de la base de données. Utilisez l’éditeur de base de données Orca fourni avec le kit de développement logiciel (SDK), ou un autre éditeur pour ouvrir MNP2001.msi et entrez les données suivantes dans la [table file](file-table.md).

[Table de fichier](file-table.md)



| Fichier         | Composant\_ | FileName     | FileSize | Version | Langage | Attributs | Séquence |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseba01.txt | Chaussures    | Baseba01.txt | 1 000     |         |          | 0          | 1        |
| Concer01.txt | Concert     | Concer01.txt | 1 000     |         |          | 0          | 1        |
| Dance01.txt  | Jongl       | Dance01.txt  | 1 000     |         |          | 0          | 1        |
| Opera01.txt  | Opera       | Opera01.txt  | 1 000     |         |          | 0          | 1        |
| Footba01.txt | Terrain    | Footba01.txt | 1 000     |         |          | 0          | 1        |
| Basket01.txt | Isole  | Basket01.txt | 1 000     |         |          | 0          | 1        |
| Help.txt     | Aide        | Help.txt     | 1 000     |         |          | 0          | 1        |
| Januar01.txt | Janvier     | Januar01.txt | 1 000     |         |          | 0          | 1        |
| NewYea01.txt | NewYears    | NewYea01.txt | 1 000     |         |          | 0          | 1        |
| Memori01.txt | Souvenir    | Memori01.txt | 1 000     |         |          | 0          | 1        |
| Redpark.exe  | Bloc-notes     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Lisezmoi.txt   | Bloc-notes     | Lisezmoi.txt   | 1 000     |         |          | 0          | 1        |



 

[Continuer](updating-components-for-an-upgrade.md)

 

 



