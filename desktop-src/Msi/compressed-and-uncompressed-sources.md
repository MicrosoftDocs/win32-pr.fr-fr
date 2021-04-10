---
description: Les auteurs de package peuvent réduire la taille des packages d’installation en compressant les fichiers sources et en les incluant dans des fichiers CAB. L’image du fichier source peut être compressée, décompressée ou une combinaison des deux types.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Sources compressées et non compressées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dc706a73d52f1dac35c917bd6c178a543ab300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951424"
---
# <a name="compressed-and-uncompressed-sources"></a><span data-ttu-id="2a01a-104">Sources compressées et non compressées</span><span class="sxs-lookup"><span data-stu-id="2a01a-104">Compressed and Uncompressed Sources</span></span>

<span data-ttu-id="2a01a-105">Les auteurs de package peuvent réduire la taille des packages d’installation en compressant les fichiers sources et en les incluant dans des [fichiers CAB](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="2a01a-105">Package authors can reduce the size of their installation packages by compressing the source files and including them in [cabinet files](cabinet-files.md).</span></span> <span data-ttu-id="2a01a-106">L’image du fichier source peut être compressée, décompressée ou une combinaison des deux types.</span><span class="sxs-lookup"><span data-stu-id="2a01a-106">The source file image can be compressed, uncompressed, or a mixture of both types.</span></span>

<dl> <dt>

<span data-ttu-id="2a01a-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Sources compressées</span><span class="sxs-lookup"><span data-stu-id="2a01a-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Compressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="2a01a-108">Une source composée uniquement de fichiers compressés doit inclure le bit d’indicateur compressé dans la propriété [**Résumé du nombre de mots**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="2a01a-108">A source consisting entirely of compressed files should include the compressed flag bit in the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="2a01a-109">Les fichiers sources compressés doivent être stockés dans des fichiers CAB situés dans un flux de données à l’intérieur du fichier. msi ou dans un fichier CAB séparé situé à la racine de l’arborescence source.</span><span class="sxs-lookup"><span data-stu-id="2a01a-109">The compressed source files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span> <span data-ttu-id="2a01a-110">Toutes les armoires de la source doivent figurer dans la [table des médias](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a01a-110">All of the cabinets in the source must be listed in the [Media table](media-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a01a-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Sources non compressées</span><span class="sxs-lookup"><span data-stu-id="2a01a-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Uncompressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="2a01a-112">Une source composée uniquement de fichiers sources non compressés doit omettre le bit de l’indicateur compressé dans la propriété [**Résumé du nombre de mots**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="2a01a-112">A source consisting entirely of uncompressed source files should omit the compressed flag bit from the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="2a01a-113">Tous les fichiers non compressés dans la source doivent exister dans l’arborescence source spécifiée par la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a01a-113">All of the uncompressed files in the source must exist in the source tree specified by the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a01a-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Sources mixtes</span><span class="sxs-lookup"><span data-stu-id="2a01a-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Mixed Sources</span></span> 
</dt> <dd>

<span data-ttu-id="2a01a-115">Pour mélanger des fichiers sources compressés et non compressés dans le même package, remplacez la valeur par défaut de la propriété [**Résumé du nombre de mots**](word-count-summary.md) en définissant les indicateurs de bits MsidbFileAttributesCompressed ou msidbFileAttributesNoncompressed sur des fichiers particuliers.</span><span class="sxs-lookup"><span data-stu-id="2a01a-115">To mix compressed and uncompressed source files in the same package, override the [**Word Count Summary**](word-count-summary.md) property default by setting the msidbFileAttributesCompressed or msidbFileAttributesNoncompressed bit flags on particular files.</span></span> <span data-ttu-id="2a01a-116">Ces indicateurs de bits sont définis dans la colonne attributs de la [table file](file-table.md) si l’état de compression du fichier ne correspond pas à la valeur par défaut spécifiée par la propriété [**Résumé du nombre de mots**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="2a01a-116">These bit flags are set in the Attributes column of the [File table](file-table.md) if the compression state of the file does not match the default specified by the [**Word Count Summary**](word-count-summary.md) property.</span></span>

<span data-ttu-id="2a01a-117">Par exemple, si l’indicateur de bit compressé est défini pour la propriété [**Résumé du nombre de mots**](word-count-summary.md) , tous les fichiers sont traités comme étant compressés dans un fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="2a01a-117">For example, if the [**Word Count Summary**](word-count-summary.md) property has the compressed flag bit set, all files are treated as compressed into a cabinet.</span></span> <span data-ttu-id="2a01a-118">Tous les fichiers non compressés dans la source doivent inclure msidbFileAttributesNoncompressed dans la colonne attributs de la [table file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a01a-118">Any uncompressed files in the source must include msidbFileAttributesNoncompressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="2a01a-119">Les fichiers non compressés doivent se trouver à la racine de l’arborescence source.</span><span class="sxs-lookup"><span data-stu-id="2a01a-119">The uncompressed files must be located at the root of the source tree.</span></span>

<span data-ttu-id="2a01a-120">Si l’indicateur non compressé est défini pour la propriété [**Résumé du nombre de mots**](word-count-summary.md) , les fichiers sont considérés comme non compressés par défaut et tous les fichiers compressés doivent inclure des msidbFileAttributesCompressed dans la colonne attributs de la table de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2a01a-120">If the [**Word Count Summary**](word-count-summary.md) property has the uncompressed flag set, files are treated as uncompressed by default and any compressed files must include msidbFileAttributesCompressed in the Attributes column of the File table.</span></span> <span data-ttu-id="2a01a-121">Tous les fichiers compressés doivent être stockés dans des fichiers CAB situés dans un flux de données à l’intérieur du fichier. msi ou dans un fichier CAB séparé situé à la racine de l’arborescence source.</span><span class="sxs-lookup"><span data-stu-id="2a01a-121">All of the compressed files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span>

<span data-ttu-id="2a01a-122">Pour plus d’informations, consultez [utilisation d’armoires et de sources compressées](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="2a01a-122">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

</dd> </dl>

 

 



