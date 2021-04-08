---
title: Activation de la superposition vidéo
description: Activation de la superposition vidéo
ms.assetid: f0b4f24c-3e35-4a18-ac77-8cae7083b0fe
keywords:
- capDriverGetCaps macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce51a3b7c77fbb161007ddde7dfe91c36152121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675270"
---
# <a name="enabling-video-overlay"></a>Activation de la superposition vidéo

L’exemple suivant utilise la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) pour déterminer si un pilote de capture a des fonctionnalités de superposition ; Si c’est le cas, la macro active la superposition.


```C++
CAPDRIVERCAPS CapDrvCaps; 

capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 

if (CapDrvCaps.fHasOverlay) 
    capOverlay(hWndC, TRUE);
 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




