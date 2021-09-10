---
title: Énumération des pilotes de capture installés
description: Énumération des pilotes de capture installés
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- capGetDriverDescription fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a053b2de7a69a712914926dbd2ab72be9d1732
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367836"
---
# <a name="enumerating-installed-capture-drivers"></a>Énumération des pilotes de capture installés

L’exemple suivant utilise la fonction [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) pour obtenir les noms et les versions des pilotes de capture installés.


```C++
char szDeviceName[80];
char szDeviceVersion[80];

for (wIndex = 0; wIndex < 10; wIndex++) 
{
    if (capGetDriverDescription(
            wIndex, 
            szDeviceName, 
            sizeof (szDeviceName), 
            szDeviceVersion, 
            sizeof (szDeviceVersion)
        )) 
    {
        // Append name to list of installed capture drivers
        // and then let the user select a driver to use.
    }
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




