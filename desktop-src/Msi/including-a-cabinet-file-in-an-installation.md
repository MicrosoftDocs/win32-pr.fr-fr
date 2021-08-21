---
description: Cette section décrit l’inclusion de fichiers CAB dans des installations de. Pour plus d’informations, consultez Utilisation d’armoires et de sources compressées.
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: Inclusion d’un fichier cab dans une installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0970d87b8b219e1558c6b3f1daf78a6a01100a7bc41f9ae1dad51a25048b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787339"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>Inclusion d’un fichier cab dans une installation

Cette section décrit l’inclusion de fichiers CAB dans des installations de. Pour plus d’informations, consultez [utilisation d’armoires et de sources compressées](using-cabinets-and-compressed-sources.md).

**Pour inclure un fichier cab dans un package d’installation**

1.  Utilisez un outil de création d’armoire pour compresser les fichiers sources dans un fichier CAB. Consultez [fichiers CAB](cabinet-files.md).
2.  Le fichier cab doit se trouver dans un flux de données à l’intérieur du fichier .msi ou dans un fichier CAB séparé situé à la racine de l’arborescence source spécifiée par la [table de répertoires](directory-table.md).
3.  Déterminez si la source doit être un type compressé ou un type mixte qui a à la fois des fichiers non compressés et des fichiers compressés. Consultez sources compressées [et non compressées](compressed-and-uncompressed-sources.md). Selon le type d’image source, définissez les bits d’indicateur compressés ou non compressés de la propriété [**Résumé du nombre de mots**](word-count-summary.md) .
4.  Ajoutez un enregistrement à la [table de fichiers](file-table.md) pour chacun des fichiers dans le fichier CAB. Entrez dans la colonne fichier une clé de fichier qui correspond exactement à la clé de fichier du fichier dans le fichier CAB. Les clés de fichier respectent la casse. La séquence d’installation de fichier dans la table de fichiers et l’armoire doit également être identique. La séquence de fichiers est spécifiée par le numéro de séquence dans la colonne séquence. Pour obtenir le numéro de séquence du premier fichier du fichier CAB, procédez comme suit. Recherchez l’enregistrement existant dans la [table des médias](media-table.md) qui a la plus grande valeur dans la colonne dipatinage. Le champ LastSequence de cet enregistrement indique le dernier numéro de séquence de fichier utilisé sur le support. Dans la table file, affectez au premier fichier du nouvel armoire un numéro de séquence supérieur à celui-ci. Attribuez des numéros de séquence à tous les fichiers restants dans le même ordre que dans le fichier CAB. Pour obtenir une description des champs d’enregistrement restants, consultez [table file](file-table.md).
5.  Ajoutez un enregistrement à la [table des médias](media-table.md) pour le cabinet. Spécifiez une valeur dans le champ dipatinage de ce nouvel enregistrement qui est supérieure à la plus grande valeur de dépatinage déjà présente dans la table. Placez le nom de l’armoire dans le champ Cabinet. Ce nom doit se présenter sous la forme d’un type de données [CAB](cabinet.md) . Préfixez le nom avec le signe dièse « \# » si le fichier cab est un flux de données stocké dans le fichier .msi. Notez que si le fichier cab est un flux de données, le nom du fichier cab est sensible à la casse. Si le fichier cab est un fichier distinct, le nom du fichier n’est pas sensible à la casse.
6.  Déterminez le numéro de séquence de fichier le plus grand dans le nouvel armoire en vérifiant la colonne séquence de la table de fichiers mise à jour. Entrez une valeur supérieure à celle-ci dans le champ LastSequence du nouvel enregistrement de la table multimédia. Pour obtenir une description des champs d’enregistrement restants, consultez [table des médias](media-table.md).
7.  Vous pouvez stocker le fichier cab dans le package d’installation à l’aide d’un outil tel que Msidb.exe ou à l’aide des [fonctions de base de données](database-functions.md)du programme d’installation. Les quatre étapes suivantes expliquent comment ajouter le fichier cab à partir d’un programme à l’aide des fonctions de base de données.
8.  pour ajouter le fichier cab au package d’installation à partir d’un programme, ouvrez une vue sur la [ \_ table Flux](-streams-table.md) de la base de données à l’aide de [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa).
9.  utilisez [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) pour définir la colonne name de la \_ table Flux sur le nom figurant dans la colonne Cabinet de la [table Media](media-table.md). Omettez le signe dièse : \# .
10. utilisez [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) pour définir la colonne de données de la \_ table Flux sur les données de l’armoire.
11. utilisez [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour mettre à jour l’enregistrement dans la \_ table Flux.
12. Pour utiliser Msidb.exe pour ajouter le fichier CAB Mycab.cab au package d’installation nommé Mydatabase.msi, utilisez la ligne de commande suivante : Msidb.exe-d mydatabase.msi-a mycab.cab. Dans ce cas, la colonne Cabinet de la table Media doit contenir la chaîne : \#mycab.cab.

 

 



