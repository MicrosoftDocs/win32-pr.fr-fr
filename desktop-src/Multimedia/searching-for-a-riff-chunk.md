---
title: Recherche d’un bloc RIFF
description: Recherche d’un bloc RIFF
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- e/s de fichier multimédia, recherche de bloc RIFF
- e/s de fichier, recherche de bloc RIFF
- entrée et sortie (e/s), recherche de bloc RIFF
- E/s (entrée et sortie), recherche de bloc RIFF
- recherche du bloc RIFF
- RIFF (Resource Interchange File Format)
- RIFF (Resource Interchange File Format)
- E/S RIFF
- Bloc RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b45b2182e44ac84423c29a79fe29e96820d5bf2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368436"
---
# <a name="searching-for-a-riff-chunk"></a>Recherche d’un bloc RIFF

L’exemple suivant utilise la fonction [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) pour rechercher un bloc « riff » avec un type de formulaire « Wave » pour vérifier que le fichier qui vient d’être ouvert est un fichier Waveform-Audio.


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfoParent; 
MMCKINFO mmckinfoSubchunk; 
. 
. 
. 
// Locate a "RIFF" chunk with a "WAVE" form type to make 
// sure the file is a waveform-audio file. 
mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
    MMIO_FINDRIFF)) 
    // The file is not a waveform-audio file. 
else 
    // The file is a waveform-audio file 

```



 

 