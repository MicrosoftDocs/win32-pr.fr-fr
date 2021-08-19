---
title: Énumération des pilotes de capture installés
description: Énumération des pilotes de capture installés
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- capGetDriverDescription fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8fe85103259354bcc3b42834ecaff03d660eb408cda8191e5e0abea7393d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988648"
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

 

 




