---
description: Une application peut tronquer ou étendre un fichier en appelant SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Troncation ou extension des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521133"
---
# <a name="truncating-or-extending-files"></a><span data-ttu-id="ec584-103">Troncation ou extension des fichiers</span><span class="sxs-lookup"><span data-stu-id="ec584-103">Truncating or Extending Files</span></span>

<span data-ttu-id="ec584-104">Une application peut tronquer ou étendre un fichier en appelant [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span><span class="sxs-lookup"><span data-stu-id="ec584-104">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span> <span data-ttu-id="ec584-105">Cette fonction définit le marqueur de fin de fichier à la position actuelle du pointeur de fichier.</span><span class="sxs-lookup"><span data-stu-id="ec584-105">This function sets the end-of-file marker to the current position of the file pointer.</span></span>

<span data-ttu-id="ec584-106">Notez que lorsqu’un fichier est étendu, le contenu entre les anciens et les nouveaux emplacements de fin de fichier n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="ec584-106">Note that when a file is extended, the contents between the old and new end-of-file locations are not defined.</span></span>

 

 



