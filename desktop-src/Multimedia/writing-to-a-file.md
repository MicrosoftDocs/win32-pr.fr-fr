---
title: Écriture dans un fichier
description: Écriture dans un fichier
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- AVIFileWriteData fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509395"
---
# <a name="writing-to-a-file"></a><span data-ttu-id="70669-104">Écriture dans un fichier</span><span class="sxs-lookup"><span data-stu-id="70669-104">Writing to a File</span></span>

<span data-ttu-id="70669-105">Vous pouvez écrire des informations supplémentaires dans un fichier qui a été ouvert avec des privilèges d’écriture à l’aide de la fonction [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) .</span><span class="sxs-lookup"><span data-stu-id="70669-105">You can write supplementary information to a file that has been opened with write privileges by using the [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) function.</span></span> <span data-ttu-id="70669-106">Cette fonction copie les informations à partir d’une mémoire tampon fournie par l’application et les place dans un ou plusieurs segments du fichier.</span><span class="sxs-lookup"><span data-stu-id="70669-106">This function copies the information from an application-supplied buffer and places it in one or more chunks in the file.</span></span> <span data-ttu-id="70669-107">Le segment « INFO » est un type de bloc RIFF courant dans lequel la fonction stocke des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="70669-107">The "INFO" chunk is a common RIFF chunk type in which the function stores supplementary information.</span></span> <span data-ttu-id="70669-108">Pour obtenir une description des fichiers RIFF et des segments de données, consultez [services de format de fichier](resource-interchange-file-format-services.md)de l’échange de ressources.</span><span class="sxs-lookup"><span data-stu-id="70669-108">For a description of RIFF files and their data chunks, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

 

 




