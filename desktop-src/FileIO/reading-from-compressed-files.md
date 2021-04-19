---
description: Une application peut décompresser un fichier compressé une partie à la fois à l’aide des fonctions LZSeek et LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lire à partir de fichiers compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522135"
---
# <a name="reading-from-compressed-files"></a><span data-ttu-id="9ba8f-103">Lire à partir de fichiers compressés</span><span class="sxs-lookup"><span data-stu-id="9ba8f-103">Reading from Compressed Files</span></span>

<span data-ttu-id="9ba8f-104">Outre la décompression d’un fichier complet en une seule opération, une application peut décompresser un fichier compressé une partie à la fois à l’aide des fonctions [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) et [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) .</span><span class="sxs-lookup"><span data-stu-id="9ba8f-104">In addition to decompressing a complete file in a single operation, an application can decompress a compressed file a portion at a time by using the [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) and [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) functions.</span></span> <span data-ttu-id="9ba8f-105">Ces fonctions sont particulièrement utiles quand il est nécessaire d’extraire des parties de fichiers volumineux.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-105">These functions are particularly useful when it is necessary to extract parts of large files.</span></span> <span data-ttu-id="9ba8f-106">Par exemple, un fabricant de polices peut comporter des fichiers compressés contenant des métriques de police en plus des données de caractères.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-106">For example, a font manufacturer may have compressed files containing font metrics in addition to character data.</span></span> <span data-ttu-id="9ba8f-107">Pour utiliser les informations contenues dans ces fichiers, une application doit décompresser le fichier ; Toutefois, la plupart des applications utilisent uniquement une partie du fichier à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-107">To use the information in these files, an application would need to decompress the file; however, most applications would use only part of the file at any particular time.</span></span> <span data-ttu-id="9ba8f-108">Pour obtenir des informations sur les métriques de police, l’application extrait les données de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-108">To get information about font metrics, the application would extract data from the header.</span></span> <span data-ttu-id="9ba8f-109">Pour récupérer des informations à partir du texte, l’application repositionne le pointeur de fichier en appelant **LZSeek** et en extrayant les données de caractères en appelant **LZRead**.</span><span class="sxs-lookup"><span data-stu-id="9ba8f-109">To get information from the text, the application would reposition the file pointer by calling **LZSeek** and extract character data by calling **LZRead**.</span></span>

 

 



