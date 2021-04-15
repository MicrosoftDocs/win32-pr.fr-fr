---
description: Windows stocke les données dans des opérations de lecture et d’écriture de fichiers dans des mémoires tampons de données gérées par le système pour optimiser les performances du disque.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Vidage du System-Buffered des données d’e/s sur le disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529998"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a><span data-ttu-id="059ec-103">Vidage du System-Buffered des données d’e/s sur le disque</span><span class="sxs-lookup"><span data-stu-id="059ec-103">Flushing System-Buffered I/O Data to Disk</span></span>

<span data-ttu-id="059ec-104">Windows stocke les données dans des opérations de lecture et d’écriture de fichiers dans des mémoires tampons de données gérées par le système pour optimiser les performances du disque.</span><span class="sxs-lookup"><span data-stu-id="059ec-104">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span> <span data-ttu-id="059ec-105">Quand une application écrit dans un fichier, le système met généralement en mémoire tampon les données et écrit les données sur le disque régulièrement.</span><span class="sxs-lookup"><span data-stu-id="059ec-105">When an application writes to a file, the system usually buffers the data and writes the data to the disk on a regular basis.</span></span> <span data-ttu-id="059ec-106">Une application peut forcer le système d’exploitation à écrire le contenu de ces mémoires tampons de données sur le disque à l’aide de la fonction [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .</span><span class="sxs-lookup"><span data-stu-id="059ec-106">An application can force the operating system to write the contents of these data buffers to the disk by using the [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) function.</span></span> <span data-ttu-id="059ec-107">Une application peut également spécifier que les opérations d’écriture doivent contourner la mémoire tampon de données et écrire directement sur le disque en définissant l’indicateur de **fichier sans indicateur de \_ mise en \_ \_ mémoire tampon** lors de la création ou de l’ouverture du fichier à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="059ec-107">Alternatively, an application can specify that write operations are to bypass the data buffer and write directly to the disk by setting the **FILE\_FLAG\_NO\_BUFFERING** flag when the file is created or opened using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

<span data-ttu-id="059ec-108">S’il y a des données dans la mémoire tampon interne lorsque le fichier est fermé, le système d’exploitation n’écrit pas automatiquement le contenu de la mémoire tampon sur le disque avant de fermer le fichier.</span><span class="sxs-lookup"><span data-stu-id="059ec-108">If there is data in the internal buffer when the file is closed, the operating system does not automatically write the contents of the buffer to the disk before closing the file.</span></span> <span data-ttu-id="059ec-109">Si l’application ne force pas le système d’exploitation à écrire le tampon sur le disque avant de fermer le fichier, l’algorithme de mise en cache détermine le moment où la mémoire tampon est écrite.</span><span class="sxs-lookup"><span data-stu-id="059ec-109">If the application does not force the operating system to write the buffer to disk before closing the file, the caching algorithm determines when the buffer is written.</span></span>

> [!Note]  
> <span data-ttu-id="059ec-110">L’accès à une mémoire tampon de données pendant qu’une opération de lecture ou d’écriture l’utilise peut corrompre la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="059ec-110">Accessing a data buffer while a read or write operation is using it may corrupt the buffer.</span></span> <span data-ttu-id="059ec-111">Les applications ne doivent pas lire, écrire, réallouer ou libérer la mémoire tampon de données utilisée par une opération de lecture ou d’écriture jusqu’à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="059ec-111">Applications must not read from, write to, reallocate, or free the data buffer that a read or write operation is using until the operation completes.</span></span>

 

 

 



