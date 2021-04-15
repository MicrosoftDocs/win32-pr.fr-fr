---
title: Ouverture d’un fichier avec mmioOpen
description: Ouverture d’un fichier avec mmioOpen
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- e/s de fichier multimédia, ouverture de fichiers
- e/s de fichier, ouverture de fichiers
- entrée et sortie (e/s), ouverture de fichiers
- E/s (entrée et sortie), ouverture de fichiers
- e/s de fichier multimédia, fonction mmioOpen
- e/s de fichier, fonction mmioOpen
- entrée et sortie (e/s), fonction mmioOpen
- E/s (entrée et sortie), fonction mmioOpen
- mmioOpen fonction)
- ouverture de fichiers d’e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2123b73c5f3a93cbb6e72711a7137652f7534b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463122"
---
# <a name="opening-a-file-with-mmioopen"></a><span data-ttu-id="58ce9-113">Ouverture d’un fichier avec mmioOpen</span><span class="sxs-lookup"><span data-stu-id="58ce9-113">Opening a File with mmioOpen</span></span>

<span data-ttu-id="58ce9-114">Pour ouvrir un fichier pour les opérations d’e/s de base, définissez le paramètre *lpmmioinfo* de la fonction [**MmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="58ce9-114">To open a file for basic I/O operations, set the *lpmmioinfo* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to **NULL**.</span></span> <span data-ttu-id="58ce9-115">L’exemple suivant ouvre un fichier nommé « C : \\ samples \\SAMPLE1.TXT » pour la lecture et vérifie la valeur de retour pour Error.</span><span class="sxs-lookup"><span data-stu-id="58ce9-115">The following example opens a file named "C:\\SAMPLES\\SAMPLE1.TXT" for reading, and checks the return value for error.</span></span>


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



<span data-ttu-id="58ce9-116">Utilisez le paramètre *dwFlags* de **mmioOpen** pour spécifier des indicateurs pour l’ouverture d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="58ce9-116">Use the *dwFlags* parameter of **mmioOpen** to specify flags for opening a file.</span></span>

 

 