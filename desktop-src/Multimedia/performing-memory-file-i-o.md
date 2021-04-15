---
title: Exécution des e/s de fichier de mémoire
description: Exécution des e/s de fichier de mémoire
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- e/s de fichier multimédia, mémoire
- e/s de fichier, mémoire
- entrée et sortie (e/s), mémoire
- E/s (entrée et sortie), mémoire
- e/s de mémoire
- mmioOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462962"
---
# <a name="performing-memory-file-io"></a><span data-ttu-id="22c44-109">Exécution des e/s de fichier de mémoire</span><span class="sxs-lookup"><span data-stu-id="22c44-109">Performing Memory File I/O</span></span>

<span data-ttu-id="22c44-110">Les services d’e/s de fichier multimédia vous permettent de traiter un bloc de mémoire comme un fichier.</span><span class="sxs-lookup"><span data-stu-id="22c44-110">The multimedia file I/O services let you treat a block of memory as a file.</span></span> <span data-ttu-id="22c44-111">Cela peut être utile si vous avez déjà une image de fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="22c44-111">This can be useful if you already have a file image in memory.</span></span> <span data-ttu-id="22c44-112">Les fichiers mémoire vous permettent de réduire le nombre de conditions de cas spéciaux dans votre code, car, à des fins d’e/s, vous pouvez traiter les fichiers de mémoire comme s’il s’agissait de fichiers sur disque.</span><span class="sxs-lookup"><span data-stu-id="22c44-112">Memory files let you reduce the number of special-case conditions in your code because, for I/O purposes, you can treat memory files as if they were disk-based files.</span></span> <span data-ttu-id="22c44-113">Vous pouvez également utiliser des fichiers de mémoire avec le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="22c44-113">You can also use memory files with the clipboard.</span></span>

<span data-ttu-id="22c44-114">Comme pour les mémoires tampons d’e/s, les fichiers mémoire peuvent utiliser la mémoire allouée par l’application ou par le gestionnaire d’e/s de fichier.</span><span class="sxs-lookup"><span data-stu-id="22c44-114">As with I/O buffers, memory files can use memory allocated by the application or by the file I/O manager.</span></span> <span data-ttu-id="22c44-115">En outre, les fichiers mémoire peuvent être développables ou non développables.</span><span class="sxs-lookup"><span data-stu-id="22c44-115">In addition, memory files can be either expandable or nonexpandable.</span></span> <span data-ttu-id="22c44-116">Lorsque le gestionnaire d’e/s de fichier atteint la fin d’un fichier mémoire extensible, il étend le fichier de mémoire à un incrément prédéfini.</span><span class="sxs-lookup"><span data-stu-id="22c44-116">When the file I/O manager reaches the end of an expandable memory file, it expands the memory file by a predefined increment.</span></span>

<span data-ttu-id="22c44-117">Pour ouvrir un fichier de mémoire, utilisez la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) avec le paramètre *SzFilename* défini sur **null** et l' \_ indicateur MMIO ReadWrite définis dans le paramètre *dwOpenFlags* .</span><span class="sxs-lookup"><span data-stu-id="22c44-117">To open a memory file, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function with the *szFilename* parameter set to **NULL** and the MMIO\_READWRITE flag set in the *dwOpenFlags* parameter.</span></span> <span data-ttu-id="22c44-118">Définissez le paramètre *lpmmioinfo* pour qu’il pointe vers une structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) qui a été configurée comme suit :</span><span class="sxs-lookup"><span data-stu-id="22c44-118">Set the *lpmmioinfo* parameter to point to an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure that has been set up as follows:</span></span>

1.  <span data-ttu-id="22c44-119">Affectez la valeur **null** au membre **pIOProc** .</span><span class="sxs-lookup"><span data-stu-id="22c44-119">Set the **pIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="22c44-120">Définissez le membre **fccIOProc** sur FourCC \_ MEM.</span><span class="sxs-lookup"><span data-stu-id="22c44-120">Set the **fccIOProc** member to FOURCC\_MEM.</span></span>
3.  <span data-ttu-id="22c44-121">Définissez le membre **pchBuffer** pour qu’il pointe vers le bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="22c44-121">Set the **pchBuffer** member to point to the memory block.</span></span> <span data-ttu-id="22c44-122">Pour demander que le gestionnaire d’e/s de fichier alloue le bloc de mémoire, affectez à **pchBuffer** la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="22c44-122">To request that the file I/O manager allocate the memory block, set **pchBuffer** to **NULL**.</span></span>
4.  <span data-ttu-id="22c44-123">Définissez le membre **cchBuffer** sur la taille initiale du bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="22c44-123">Set the **cchBuffer** member to the initial size of the memory block.</span></span>
5.  <span data-ttu-id="22c44-124">Définissez le membre **adwInfo** sur la taille d’expansion minimale du bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="22c44-124">Set the **adwInfo** member to the minimum expansion size of the memory block.</span></span> <span data-ttu-id="22c44-125">Pour un fichier de mémoire non développable, affectez à **adwInfo** la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="22c44-125">For a nonexpandable memory file, set **adwInfo** to **NULL**.</span></span>
6.  <span data-ttu-id="22c44-126">Affectez la valeur zéro à tous les autres membres.</span><span class="sxs-lookup"><span data-stu-id="22c44-126">Set all other members to zero.</span></span>

<span data-ttu-id="22c44-127">Il n’existe aucune restriction quant à l’allocation de mémoire pour une utilisation en tant que fichier mémoire non développable.</span><span class="sxs-lookup"><span data-stu-id="22c44-127">There are no restrictions on allocating memory for use as a nonexpandable memory file.</span></span>

 

 