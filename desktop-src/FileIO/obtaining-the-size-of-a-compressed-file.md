---
description: Pour obtenir la taille compressée d’un fichier, utilisez la fonction GetCompressedFileSize.
ms.assetid: c6bfd221-f125-48b4-b38b-822a23639c40
title: Obtention de la taille d’un fichier compressé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4954a53184e55341838fef7cd70f01639f13bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527046"
---
# <a name="obtaining-the-size-of-a-compressed-file"></a><span data-ttu-id="024a4-103">Obtention de la taille d’un fichier compressé</span><span class="sxs-lookup"><span data-stu-id="024a4-103">Obtaining the Size of a Compressed File</span></span>

<span data-ttu-id="024a4-104">Utilisez la fonction [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) pour obtenir la taille compressée d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="024a4-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the compressed size of a file.</span></span> <span data-ttu-id="024a4-105">Si le fichier est compressé, sa taille compressée est inférieure à sa taille non compressée.</span><span class="sxs-lookup"><span data-stu-id="024a4-105">If the file is compressed, its compressed size will be less than its uncompressed size.</span></span> <span data-ttu-id="024a4-106">Utilisez la fonction [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) pour déterminer la taille non compressée d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="024a4-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the uncompressed size of a file.</span></span>

 

 



