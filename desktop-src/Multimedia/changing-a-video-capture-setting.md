---
title: Modification d’un paramètre de capture vidéo
description: Modification d’un paramètre de capture vidéo
ms.assetid: a5fe7e1e-084d-4102-91d4-ffe5d1d0e5c8
keywords:
- capCaptureGetSetup macro)
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b3f2629325c67bcad1fed26a9fed4d053372392
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367799"
---
# <a name="changing-a-video-capture-setting"></a>Modification d’un paramètre de capture vidéo

L’exemple suivant utilise les macros [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) et [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) pour modifier la fréquence de capture à partir de la valeur par défaut (15 images par seconde) à 10 images par seconde.


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




