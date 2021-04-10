---
title: Installation des compresseurs et des décompresseurs
description: Installation des compresseurs et des décompresseurs
ms.assetid: 8bcca000-c4c7-47e7-a4c0-5d0d1750176f
keywords:
- Gestionnaire de compression vidéo (VCM), installation de compresseurs
- VCM (gestionnaire de compression vidéo), installation de compresseurs
- ICInstall fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8c3421b3d7f59e7f6b16150fcd0d641deaef17
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309678"
---
# <a name="installing-compressors-and-decompressors"></a>Installation des compresseurs et des décompresseurs

L’exemple suivant montre comment une application peut installer une fonction en tant que compresseur ou décompresseur à l’aide de la fonction [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) .


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




