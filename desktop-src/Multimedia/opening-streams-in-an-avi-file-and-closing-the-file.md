---
title: ouverture de Flux dans un fichier AVI et fermeture du fichier
description: ouverture de Flux dans un fichier AVI et fermeture du fichier
ms.assetid: 3c6afa04-3d95-48cd-b468-7167bac07d46
keywords:
- AVIFileGetStream fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca06378862ec543e9da8f671eca50841c85d744
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363708"
---
# <a name="opening-streams-in-an-avi-file-and-closing-the-file"></a>ouverture de Flux dans un fichier AVI et fermeture du fichier

L’exemple suivant ouvre tous les flux d’un fichier AVI à l’aide de la fonction [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) . Si une erreur se produit, le fichier est fermé.


```C++
// InsertAVIFile - opens the streams in an AVI file. 
// 
// pfile - file-interface pointer from AVIFileOpen 
// 
// Global variables 
// gcpavi - count of the number of streams in an AVI file 
// gapavi[] = array of stream-interface pointers 
 
void InsertAVIFile(PAVIFILE pfile, HWND hwnd, LPSTR lpszFile) 
{ 
    int    i; 
    gcpavi = 0; 
 
    // Open the streams until a stream is not available. 
    for (i = gcpavi; i < MAXNUMSTREAMS; i++) { 
        gapavi[i] = NULL; 
        if (AVIFileGetStream(pfile, &gapavi[i], 0L, i - gcpavi) 
            != AVIERR_OK) 
        break; 
 
    if (gapavi[i] == NULL) 
        break; 
    } 
    // Display error message-stream not found. 
    if (gcpavi == i) 
    { 
        // Handle failure.
        if (pfile) // If file is open, close it 
            AVIFileRelease(pfile); 
        return; 
    } 
    else { 
        gcpavi = i - 1; 
    } 
 
//  . 
//  . Place functions to process data here. 
//  . 
} 
 
```



 

 




