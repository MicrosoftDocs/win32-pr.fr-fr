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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368404"
---
# <a name="changing-the-io-buffer-size"></a>Modification de la taille de la mémoire tampon d’e/s

L’exemple suivant ouvre un fichier nommé SAMPLE.TXT pour les e/s non mises en mémoire tampon, puis active les e/s mises en mémoire tampon avec une mémoire tampon de 16 Ko interne à l’aide de la fonction [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) .


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



 

 