---
description: Les auteurs de package peuvent réduire la taille des packages d’installation en compressant les fichiers sources et en les incluant dans des fichiers CAB. L’image du fichier source peut être compressée, décompressée ou une combinaison des deux types.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Sources compressées et non compressées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7d35a5723261ab1c62866d185a8402a9607600cad906c2fb66ddc5dc85ac08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144450"
---
# <a name="compressed-and-uncompressed-sources"></a>Sources compressées et non compressées

Les auteurs de package peuvent réduire la taille des packages d’installation en compressant les fichiers sources et en les incluant dans des [fichiers CAB](cabinet-files.md). L’image du fichier source peut être compressée, décompressée ou une combinaison des deux types.

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Sources compressées
</dt> <dd>

Une source composée uniquement de fichiers compressés doit inclure le bit d’indicateur compressé dans la propriété [**Résumé du nombre de mots**](word-count-summary.md) . Les fichiers sources compressés doivent être stockés dans des fichiers CAB situés dans un flux de données à l’intérieur du fichier .msi ou dans un fichier CAB séparé situé à la racine de l’arborescence source. Toutes les armoires de la source doivent figurer dans la [table des médias](media-table.md).

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Sources non compressées
</dt> <dd>

Une source composée uniquement de fichiers sources non compressés doit omettre le bit de l’indicateur compressé dans la propriété [**Résumé du nombre de mots**](word-count-summary.md) . Tous les fichiers non compressés dans la source doivent exister dans l’arborescence source spécifiée par la [table de répertoires](directory-table.md).

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Sources mixtes 
</dt> <dd>

Pour mélanger des fichiers sources compressés et non compressés dans le même package, remplacez la valeur par défaut de la propriété [**Résumé du nombre de mots**](word-count-summary.md) en définissant les indicateurs de bits MsidbFileAttributesCompressed ou msidbFileAttributesNoncompressed sur des fichiers particuliers. Ces indicateurs de bits sont définis dans la colonne attributs de la [table file](file-table.md) si l’état de compression du fichier ne correspond pas à la valeur par défaut spécifiée par la propriété [**Résumé du nombre de mots**](word-count-summary.md) .

Par exemple, si l’indicateur de bit compressé est défini pour la propriété [**Résumé du nombre de mots**](word-count-summary.md) , tous les fichiers sont traités comme étant compressés dans un fichier CAB. Tous les fichiers non compressés dans la source doivent inclure msidbFileAttributesNoncompressed dans la colonne attributs de la [table file](file-table.md). Les fichiers non compressés doivent se trouver à la racine de l’arborescence source.

Si l’indicateur non compressé est défini pour la propriété [**Résumé du nombre de mots**](word-count-summary.md) , les fichiers sont considérés comme non compressés par défaut et tous les fichiers compressés doivent inclure des msidbFileAttributesCompressed dans la colonne attributs de la table de fichiers. Tous les fichiers compressés doivent être stockés dans des fichiers CAB situés dans un flux de données à l’intérieur du fichier .msi ou dans un fichier CAB séparé situé à la racine de l’arborescence source.

Pour plus d’informations, consultez [utilisation d’armoires et de sources compressées](using-cabinets-and-compressed-sources.md).

</dd> </dl>

 

 



