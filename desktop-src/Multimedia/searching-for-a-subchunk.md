---
title: Recherche d’un sous-segment
description: Recherche d’un sous-segment
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
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
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315113"
---
# <a name="searching-for-a-subchunk"></a>Recherche d’un sous-segment

L’exemple suivant utilise la fonction [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) pour rechercher le segment « fmt » dans le bloc « riff » de l’exemple précédent.


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



Pour rechercher un sous-bloc (autrement dit, tout segment autre qu’un bloc « RIFF » ou « LIST »), identifiez son segment parent dans le paramètre *lpckParent* de la fonction [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) .

Si vous ne spécifiez pas de bloc parent, la position actuelle du fichier doit se trouver au début d’un segment avant d’appeler la fonction **mmioDescend** . Si vous spécifiez un segment parent, la position actuelle du fichier peut se trouver n’importe où dans ce segment.

Si la recherche d’un sous-bloc échoue, la position actuelle du fichier n’est pas définie. Vous pouvez utiliser la fonction [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) et le membre **dwDataOffset** de la structure [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) décrivant le segment parent pour effectuer une recherche au début du bloc parent, comme dans l’exemple suivant :


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



Étant donné que **dwDataOffset** spécifie le décalage au début de la partie données du segment, vous devez rechercher 4 octets passés **dwDataOffset** pour définir la position du fichier après le type de formulaire.

 

 