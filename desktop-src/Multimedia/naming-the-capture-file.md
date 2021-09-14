---
title: Attribution d’un nom au fichier de capture
description: Attribution d’un nom au fichier de capture
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- capFileSetCaptureFile macro)
- capFileAlloc macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ea091a36777e176124689ba57be6c0fb75d07d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119605"
---
# <a name="naming-the-capture-file"></a>Attribution d’un nom au fichier de capture

L’exemple suivant utilise la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) pour spécifier un autre nom de fichier (MYCAP.AVI) pour le fichier de capture et la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) pour préallouer un fichier de 5 Mo.


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




