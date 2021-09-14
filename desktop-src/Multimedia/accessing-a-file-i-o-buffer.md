---
title: Accès à un tampon d’e/s de fichier
description: Accès à un tampon d’e/s de fichier
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- e/s de fichier multimédia, accès aux mémoires tampons
- e/s de fichier, accès aux mémoires tampons
- entrée et sortie (e/s), accès aux mémoires tampons
- E/s (entrée et sortie), accès aux mémoires tampons
- accès aux mémoires tampons d’e/s
- e/s mises en mémoire tampon
- mmioSetInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c89b2376f1bae68d55c76d7731b6ee78f6bf7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007301"
---
# <a name="accessing-a-file-io-buffer"></a>Accès à un tampon d’e/s de fichier

L’exemple suivant accède directement à une mémoire tampon d’e/s pour lire des données à partir d’un fichier Waveform-Audio.


```C++
HMMIO    hmmio; 
MMIOINFO mmioinfo; 
DWORD    dwDataSize; 
DWORD    dwCount; 
HPSTR    hptr; 

// Get information about the file I/O buffer. 
if (mmioGetInfo(hmmio, &mmioinfo, 0)) 
{ 
    Error("Failed to get I/O buffer info."); 
    . 
    . 
    . 
    mmioClose(hmmio, 0); 
    return; 
} 
 
// Read the entire file by directly reading the file I/O buffer. 
// When the end of the I/O buffer is reached, advance the buffer. 

for (dwCount = dwDataSize, hptr = lpData; dwCount  0; dwCount--) 
{ 
    // Check to see if the I/O buffer must be advanced. 
    if (mmioinfo.pchNext == mmioinfo.pchEndRead) 
    { 
        if(mmioAdvance(hmmio, &mmioinfo, MMIO_READ)) 
        { 
            Error("Failed to advance buffer."); 
            . 
            . 
            . 
            mmioClose(hmmio, 0); 
            return; 
        } 
    } 
 
    // Get a character from the buffer. 
    *hptr++ = *mmioinfo.pchNext++; 
} 
 
// End direct buffer access and close the file. 
mmioSetInfo(hmmio, &mmioinfo, 0); 
mmioClose(hmmio, 0); 

```



Lorsque vous avez terminé d’accéder à une mémoire tampon d’e/s de fichier, appelez la fonction [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) , en passant une adresse de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) remplie par la fonction [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) . Si vous avez écrit dans la mémoire tampon, définissez l' \_ indicateur de modification MMIO dans le membre **dwFlags** de la structure **MMIOINFO** avant d’appeler **mmioSetInfo**. Dans le cas contraire, la mémoire tampon n’est pas vidée sur le disque.

 

 