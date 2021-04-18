---
title: Préallocation d’espace disque pour le fichier de capture
description: Préallocation d’espace disque pour le fichier de capture
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- Message WM_CAP_FILE_ALLOCATE
- capFileAlloc macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309854"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a><span data-ttu-id="de8ae-105">Préallocation d’espace disque pour le fichier de capture</span><span class="sxs-lookup"><span data-stu-id="de8ae-105">Disk Space Preallocation for the Capture File</span></span>

<span data-ttu-id="de8ae-106">Préallouer de l’espace disque pour le fichier de capture crée un fichier d’une taille spécifiée sur le disque avant le démarrage d’une opération de capture.</span><span class="sxs-lookup"><span data-stu-id="de8ae-106">Preallocating disk space for the capture file builds a file of a specified size on the disk before the start of a capture operation.</span></span> <span data-ttu-id="de8ae-107">La préallocation d’un fichier de capture réduit le traitement nécessaire lorsque la capture est en cours et entraîne moins de frames supprimés.</span><span class="sxs-lookup"><span data-stu-id="de8ae-107">Preallocating a capture file reduces the processing required while capture is in progress and results in fewer dropped frames.</span></span> <span data-ttu-id="de8ae-108">Vous pouvez préallouer un fichier de capture à l’aide du message d' [**\_ \_ \_ allocation de fichier WM Cap**](wm-cap-file-allocate.md) (ou de la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) ).</span><span class="sxs-lookup"><span data-stu-id="de8ae-108">You can preallocate a capture file by using the [**WM\_CAP\_FILE\_ALLOCATE**](wm-cap-file-allocate.md) message (or the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro).</span></span>

<span data-ttu-id="de8ae-109">En règle générale, votre application doit préallouer suffisamment d’espace disque pour contenir le plus grand fichier de capture prévu.</span><span class="sxs-lookup"><span data-stu-id="de8ae-109">Typically, your application should preallocate enough disk space to contain the largest capture file anticipated.</span></span> <span data-ttu-id="de8ae-110">La préallocation de l’espace disque ne limite pas la taille du fichier capturé.</span><span class="sxs-lookup"><span data-stu-id="de8ae-110">Preallocating disk space does not restrict the size of the captured file.</span></span> <span data-ttu-id="de8ae-111">La taille du fichier est automatiquement augmentée si les données capturées dépassent l’espace alloué.</span><span class="sxs-lookup"><span data-stu-id="de8ae-111">The file size is automatically enlarged if the captured data exceeds the allocated space.</span></span> <span data-ttu-id="de8ae-112">Les opérations d’écriture ultérieures dans le fichier de capture réutilisent les portions d’espace disque allouées pour le fichier, ce qui permet de conserver la taille et la fragmentation du fichier.</span><span class="sxs-lookup"><span data-stu-id="de8ae-112">Subsequent write operations to the capture file reuse the portions of disk space allocated for the file, preserving the size and fragmentation of the file.</span></span>

<span data-ttu-id="de8ae-113">Vous pouvez également améliorer les performances de capture en défragmentant le fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="de8ae-113">You can also improve capture performance by defragmenting the capture file.</span></span> <span data-ttu-id="de8ae-114">Pour défragmenter le fichier, utilisez un utilitaire de défragmentation tel que le Défragmenteur de disque.</span><span class="sxs-lookup"><span data-stu-id="de8ae-114">To defragment the file, use a defragmentation utility such as Disk Defragmenter.</span></span> <span data-ttu-id="de8ae-115">Si vous utilisez un fichier de capture défragmenté et que vous l’agrandissez plus tard, vous devez défragmenter le fichier agrandi.</span><span class="sxs-lookup"><span data-stu-id="de8ae-115">If you use a defragmented capture file and later enlarge it, you should defragment the enlarged file.</span></span> <span data-ttu-id="de8ae-116">L’agrandissement d’un fichier de capture défragmenté peut fragmenter la partie développée du fichier et réduire les performances de l’opération de capture.</span><span class="sxs-lookup"><span data-stu-id="de8ae-116">Enlarging a defragmented capture file can fragment the expanded portion of the file and reduce performance in the capture operation.</span></span>

<span data-ttu-id="de8ae-117">Vous pouvez également améliorer les performances à l’aide d’un disque non compressé pour la capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="de8ae-117">You might also improve performance by using an uncompressed disk for video capture.</span></span> <span data-ttu-id="de8ae-118">La compression des données pendant la capture peut limiter le débit des captures sur le disque.</span><span class="sxs-lookup"><span data-stu-id="de8ae-118">Compressing data during capture can limit capture throughput to the disk.</span></span>

<span data-ttu-id="de8ae-119">Une application peut réserver un fichier de capture permanent pour éliminer le temps nécessaire à la préallocation et à la défragmentation d’un fichier chaque fois qu’il est démarré.</span><span class="sxs-lookup"><span data-stu-id="de8ae-119">An application can reserve a permanent capture file to eliminate the time required to preallocate and defragment a file each time it is started.</span></span> <span data-ttu-id="de8ae-120">Comme un fichier de capture peut nécessiter un espace disque considérable et que la préallocation d’un fichier de capture supprime toutes les données d’un fichier de capture existant, une application doit permettre à l’utilisateur de décider si le fichier est permanent ou temporaire.</span><span class="sxs-lookup"><span data-stu-id="de8ae-120">Because a capture file can require considerable disk space, and preallocating a capture file removes all data from an existing capture file, an application should let the user decide if the file is permanent or temporary.</span></span>

 

 




