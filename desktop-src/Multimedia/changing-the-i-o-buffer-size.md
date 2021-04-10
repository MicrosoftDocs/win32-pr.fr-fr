---
title: Modification de la taille de la mémoire tampon d’e/s
description: Modification de la taille de la mémoire tampon d’e/s
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- e/s de fichier multimédia, modification de la taille de la mémoire tampon
- e/s de fichier, modification de la taille de la mémoire tampon
- entrée et sortie (e/s), modification de la taille de la mémoire tampon
- E/s (entrée et sortie), modification de la taille de la mémoire tampon
- modification de la taille des tampons d’e/s
- e/s non mises en mémoire tampon
- e/s mises en mémoire tampon
- mmioSetBuffer fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2171f4f09b933a3de5ec1e99750261fdda2f80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031247"
---
# <a name="changing-the-io-buffer-size"></a><span data-ttu-id="e48ca-111">Modification de la taille de la mémoire tampon d’e/s</span><span class="sxs-lookup"><span data-stu-id="e48ca-111">Changing the I/O Buffer Size</span></span>

<span data-ttu-id="e48ca-112">L’exemple suivant ouvre un fichier nommé SAMPLE.TXT pour les e/s non mises en mémoire tampon, puis active les e/s mises en mémoire tampon avec une mémoire tampon de 16 Ko interne à l’aide de la fonction [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) .</span><span class="sxs-lookup"><span data-stu-id="e48ca-112">The following example opens a file named SAMPLE.TXT for unbuffered I/O, and then enables buffered I/O with an internal 16K buffer using the [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) function.</span></span>


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("SAMPLE.TXT", NULL, MMIO_READ)) != NULL) 
{ 
    // File opened successfully; request an I/O buffer. 
    if (mmioSetBuffer(hFile, NULL, 16384L, 0)) 
        // Buffer cannot be allocated. 
    else 
        // Buffer allocated successfully. 
} 
else 
    // File cannot be opened. 
```



 

 