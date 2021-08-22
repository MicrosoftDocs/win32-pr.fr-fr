---
description: La table file contient la liste complète de tous les fichiers sources pour l’installation.
ms.assetid: 481fdc45-82db-4128-93de-388562f636e9
title: Classement des numéros séquentiels dans un fichier CAB, table de fichiers et table Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f64558a570c7184da36feba8aeea6d2a7dc32c0d8add4c6963dece131c4849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327865"
---
# <a name="ordering-file-sequence-numbers-in-a-cabinet-file-table-and-media-table"></a>Classement des numéros séquentiels dans un fichier CAB, table de fichiers et table Media

La [table file](file-table.md) contient la liste complète de tous les fichiers sources pour l’installation. Les fichiers peuvent être stockés sur le support source en tant que fichiers individuels ou compressés dans des [fichiers CAB](cabinet-files.md). Les numéros de séquence de la colonne Sequence de la table file, ainsi que le champ LastSequence de la [table Media](media-table.md), spécifient l’ordre d’installation des fichiers et le support source sur lequel se trouvent chaque fichier. Chaque enregistrement de la table Media identifie le disque source contenant tous les fichiers dont les numéros de séquence sont inférieurs ou égaux à la valeur affichée dans la colonne LastSequence et qui est supérieur à la valeur LastSequence du disque précédent.

Supposons, par exemple, qu’un fichier a un numéro de séquence de 92 entré dans la colonne séquence de la table file. Pour déterminer sur quel disque source ce fichier réside, le programme d’installation vérifie l’enregistrement de la table des médias pour l’entrée avec la plus petite valeur LastSequence supérieure à 92. La colonne dipatinage est la clé primaire de la table multimédia et ce champ identifie de manière unique le disque dans la table.

la limite maximale du nombre de fichiers pouvant être listés dans la table de fichiers d’un package de Windows Installer est de 32767 fichiers. pour créer un package Windows Installer contenant d’autres fichiers, consultez [création d’un package volumineux](authoring-a-large-package.md).

Les auteurs de package peuvent réduire la taille des packages d’installation en compressant les fichiers sources et en les incluant dans des fichiers CAB. L’image du fichier source peut être compressée, décompressée ou une combinaison des deux types. Pour plus d’informations sur les sources compressées et non compressées, consultez sources compressées [et non compressées](compressed-and-uncompressed-sources.md). Les fichiers sources compressés doivent être stockés dans un fichier CAB. Les fichiers compressés dans un fichier CAB ont leurs propres numéros de séquence interne. Les valeurs de ces numéros de séquence internes n’ont pas besoin de correspondre à la valeur des numéros de séquence dans la table de fichiers. Toutefois, la séquence des fichiers spécifiée dans la table de fichiers doit être identique à la séquence réelle des fichiers dans les armoires. Les numéros de séquence des fichiers non compressés n’ont pas besoin d’être uniques. Par exemple, si tous les fichiers sont décompressés et se trouvent sur un disque, tous les fichiers peuvent avoir le même numéro de séquence dans la table de fichiers.

La table des médias décrit l’ensemble des disques qui composent le média source pour l’installation. La première entrée de la table des médias doit toujours avoir 1 dans le champ dipatinage. Les fichiers doivent être organisés sur le média source, de sorte que tous les fichiers sur le disque 1 ont des numéros de séquence de table de fichiers inférieurs aux numéros de séquence des fichiers sur le disque 2, et que tous les numéros de séquence sur le disque 2 soient plus petits que sur le disque 3, et ainsi de suite. Cette exigence s’applique également à un disque qui contient à la fois des sources compressées et non compressées. Par exemple, si les sources de média pour l’installation se trouvent sur deux disques source et si le disque 1 contient à la fois des fichiers non compressés et un fichier CAB, les deux fichiers non compressés et les fichiers de l’armoire doivent avoir des numéros séquentiels plus petits que le plus petit numéro de séquence de fichier de n’importe quel fichier stocké sur le disque 2. Si tous les fichiers sur le disque 1 sont compressés dans un fichier CAB, la table des médias peut être créée comme indiqué dans le tableau suivant.

[Table des médias](media-table.md) (partielle)



| DiskId | LastSequence | DiskPrompt | CAB   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          | mycab.cab | Disque 1      |
| 2      | 10           | 2          |           | Disque 2      |



 

Si certains fichiers sur le disque 1 sont compressés dans un fichier CAB et que d’autres ne sont pas compressés, la table multimédia peut être créée comme suit.

[Table des médias](media-table.md) (partielle)



| DiskId | LastSequence | DiskPrompt | CAB   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disque 1      |
| 2      | 10           | 1          | mycab.cab | Disque 1      |
| 3      | 15           | 2          |           | Disque 2      |



 

Notez que la création dans la table multimédia suivante est incorrecte, car elle spécifie des numéros de séquence de fichiers sur le disque 2 qui sont plus petits que certains fichiers dans le fichier cab sur le disque 1.

[Table des médias](media-table.md)



| DiskId | LastSequence | DiskPrompt | CAB   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disque 1      |
| 2      | 10           | 2          |           | Disque 2      |
| 3      | 15           | 1          | mycab.cab | Disque 1      |



 

Les fichiers volumineux peuvent être fractionnés entre deux fichiers CAB ou plus. Il ne peut pas y avoir plus de 15 fichiers dans un fichier CAB qui s’étend au fichier CAB suivant. Par exemple, si vous avez trois fichiers CAB, le premier fichier CAB peut avoir 15 fichiers qui s’étendent au deuxième fichier CAB, et la deuxième armoire peut avoir 15 fichiers qui s’étendent au troisième fichier CAB. Lorsque vous ajoutez un enregistrement à la table de fichiers pour un fichier de plusieurs armoires, utilisez la première partie du fichier pour spécifier le numéro de séquence de fichier que vous entrez dans la colonne séquence.

Les tables de fichiers et de supports peuvent être créées comme suit s’il y a trois fichiers, deux armoires et deux disques. Dans cet exemple, c1.cab réside sur disk1 et c2.cab réside sur disk2. Le fichier F2 s’étend sur les deux armoires. Le fichier CAB c1.cab contient la totalité du fichier F1 et la première partie du fichier F2. Le c2.cab Cabinet contient la deuxième partie de F2 et le fichier F3 entier.

[Table des médias](media-table.md) (partielle)



| DiskId | LastSequence | DiskPrompt | CAB | VolumeLabel |
|--------|--------------|------------|---------|-------------|
| 1      | 5            | 1          | c1.cab  | Disque 1      |
| 2      | 10           | 2          | c2.cab  | Disque 2      |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier | Séquence |
|------|----------|
| Ctrl+F1   | 1        |
| C2   | 2        |
| F3   | 6        |



 

 

 



