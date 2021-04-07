---
description: La fonction GetFileSize récupère la taille d’un fichier.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Détermination de la taille d’un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7205c47fe25b223dbcc12322516ff2b162fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952127"
---
# <a name="determining-the-size-of-a-file"></a><span data-ttu-id="49a91-103">Détermination de la taille d’un fichier</span><span class="sxs-lookup"><span data-stu-id="49a91-103">Determining the Size of a File</span></span>

<span data-ttu-id="49a91-104">La fonction [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) récupère la taille d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="49a91-104">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span>

<span data-ttu-id="49a91-105">Étant donné que l’implémentation de fichiers du système de fichiers NTFS autorise plusieurs flux dans un fichier, toute application que vous écrivez et qui accède à des fichiers doit tenir compte du fait que le créateur du fichier peut inclure plusieurs flux dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="49a91-105">Because the NTFS file system implementation of files allows for multiple streams within a file, any application you write that accesses files must account for the possibility that the creator of the file can include multiple streams in the file.</span></span> <span data-ttu-id="49a91-106">Si plusieurs flux ne sont pas vérifiés dans un fichier, l’application peut sous-estimer la taille totale du fichier, entre autres erreurs.</span><span class="sxs-lookup"><span data-stu-id="49a91-106">If multiple streams are not checked for in a file, the application can underestimate the total size of the file, among other errors.</span></span>

 

 



