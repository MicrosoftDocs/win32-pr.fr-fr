---
description: Le système de fichiers NTFS utilise la compression Lempel-Ziv, qui est un algorithme de compression sans perte.
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: Compression et décompression de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d1aa9d8d3540eff85413c03358fd1ba7e21300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524450"
---
# <a name="file-compression-and-decompression"></a>Compression et décompression de fichiers

Les volumes de système de fichiers NTFS prennent en charge la compression de fichiers sur une base individuelle. L’algorithme de compression de fichiers utilisé par le système de fichiers NTFS est Lempel-Ziv la compression. Il s’agit d’un algorithme de compression *sans perte* , ce qui signifie qu’aucune donnée n’est perdue lors de la compression et de la décompression du fichier, par opposition aux algorithmes de compression avec *perte* tels que JPEG, où certaines données sont perdues à chaque fois que la compression et la décompression des données se produisent.

La compression des données réduit la taille d’un fichier en réduisant les données redondantes. Dans un fichier texte, les données redondantes peuvent être fréquemment des caractères, tels que le caractère espace ou des voyelles courantes, telles que les lettres e et a ; Il peut également se produire souvent des chaînes de caractères. La compression de données crée une version compressée d’un fichier en réduisant les données redondantes.

Chaque type d’algorithme de compression de données réduit les données redondantes de manière unique. Par exemple, l' *algorithme d’encodage Huffman* affecte un code aux caractères d’un fichier en fonction de la fréquence à laquelle ces caractères se produisent. Un autre algorithme de compression, appelé *encodage* de la longueur d’exécution, génère une valeur en deux parties pour les caractères répétés : la première partie spécifie le nombre de fois où le caractère est répété, et la deuxième partie identifie le caractère. Un autre algorithme de compression, connu sous le nom d' *algorithme Lempel-Ziv*, convertit les chaînes de longueur variable en codes de longueur fixe qui consomment moins d’espace que les chaînes d’origine.

## <a name="the-ntfs-file-system-file-compression"></a>Compression de fichiers du système de fichiers NTFS

Sur le système de fichiers NTFS, la compression est effectuée en toute transparence. Cela signifie qu’il peut être utilisé sans qu’il soit nécessaire de modifier les applications existantes. Les octets compressés du fichier ne sont pas accessibles aux applications ; ils voient uniquement les données non compressées. Par conséquent, les applications qui ouvrent un fichier compressé peuvent y opérer comme si elles n’avaient pas été compressées. Toutefois, ces fichiers ne peuvent pas être copiés dans un autre système de fichiers.

Si vous compressez un fichier dont la taille est supérieure à 30 gigaoctets, la compression peut échouer.

Les rubriques suivantes identifient la compression des fichiers du système de fichiers NTFS :

-   [Attribut de compression](compression-attribute.md)
-   [État de compression](compression-state.md)
-   [Obtention de la taille d’un fichier compressé](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a>Bibliothèques de compression et de décompression de fichiers

Les bibliothèques de compression et de décompression de fichiers prennent un ou des fichiers existants et produisent un ou des fichiers qui sont des versions compressées des originaux. La compression est également sans perte, mais la compression n’est pas transparente pour les applications. Une application peut uniquement fonctionner sur ces fichiers à l’aide d’une bibliothèque de compression de fichier. En outre, les seules opérations que vous pouvez effectuer sur ces fichiers sont la création d’un fichier compressé à partir d’un original et la récupération des données d’origine à partir de la version décompressée. En règle générale, la modification n’est pas prise en charge et la recherche est limitée si elle est prise en charge.

En règle générale, une application appelle des fonctions dans Lz32.dll pour décompresser les données qui ont été compressées à l’aide de Compress.exe. Les fonctions peuvent également traiter des fichiers sans tenter de les décompresser.

Vous pouvez utiliser les fonctions de Lz32.dll pour décompresser un ou plusieurs fichiers. Vous pouvez également les utiliser pour décompresser des fichiers compressés une partie à la fois.

Les rubriques suivantes identifient la décompression de fichier fournie par les fonctions dans Lz32.dll :

-   [Décompression d’un fichier unique](decompressing-a-single-file.md)
-   [Décompression de plusieurs fichiers](decompressing-multiple-files.md)
-   [Lire à partir de fichiers compressés](reading-from-compressed-files.md)

## <a name="cabinets"></a>Boîtier

Les armoires sont créées par une bibliothèque de compression qui prend en charge des fonctionnalités telles que le fractionnement de disque et la compression de fichiers multiples. Pour plus d’informations, consultez le kit de développement logiciel (SDK) CAB : [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) .

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                             | Description                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Attribut de compression](compression-attribute.md)<br/>                                     | Sur un volume de système de fichiers NTFS, chaque fichier et répertoire a un *attribut de compression*.<br/>                                         |
| [État de compression](compression-state.md)<br/>                                             | Chaque fichier et répertoire sur un volume qui prend en charge la compression de fichiers et de répertoires individuels a un *État de compression*.<br/> |
| [Obtention de la taille d’un fichier compressé](obtaining-the-size-of-a-compressed-file.md)<br/> | Pour obtenir la taille compressée d’un fichier, utilisez la fonction GetCompressedFileSize.<br/>                                               |
| [Décompression d’un fichier unique](decompressing-a-single-file.md)<br/>                         | Une application peut décompresser un fichier compressé unique à l’aide des fonctions LZOpenFile, LZCopy et LZClose.<br/>                |
| [Décompression de plusieurs fichiers](decompressing-multiple-files.md)<br/>                       | Une application peut décompresser plusieurs fichiers à l’aide des fonctions LZOpenFile, LZCopy et LZClose.<br/>                          |
| [Lire à partir de fichiers compressés](reading-from-compressed-files.md)<br/>                     | Une application peut décompresser un fichier compressé une partie à la fois à l’aide des fonctions LZSeek et LZRead.<br/>                 |



 

 

