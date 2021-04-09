---
description: Obtenir la taille allouée ou la taille totale d’un fichier à l’aide de la fonction GetCompressedFileSize ou GetFileSize.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Obtention de la taille d’un fichier partiellement alloué
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863054"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a><span data-ttu-id="d815e-103">Obtention de la taille d’un fichier partiellement alloué</span><span class="sxs-lookup"><span data-stu-id="d815e-103">Obtaining the Size of a Sparse File</span></span>

<span data-ttu-id="d815e-104">Utilisez la fonction [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) pour obtenir la taille réelle allouée sur le disque pour un fichier partiellement alloué.</span><span class="sxs-lookup"><span data-stu-id="d815e-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the actual size allocated on disk for a sparse file.</span></span> <span data-ttu-id="d815e-105">Ce total n’inclut pas la taille des régions qui ont été désallouées, car elles ont été remplies de zéros.</span><span class="sxs-lookup"><span data-stu-id="d815e-105">This total does not include the size of the regions which were deallocated because they were filled with zeros.</span></span> <span data-ttu-id="d815e-106">Utilisez la fonction [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) pour déterminer la taille totale d’un fichier, y compris la taille des régions éparses qui ont été désallouées.</span><span class="sxs-lookup"><span data-stu-id="d815e-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the total size of a file, including the size of the sparse regions that were deallocated.</span></span>

 

 



