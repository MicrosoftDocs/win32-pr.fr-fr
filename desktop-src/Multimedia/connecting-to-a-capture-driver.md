---
title: Connexion à un pilote de capture
description: Connexion à un pilote de capture
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- capDriverDisconnect macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34e606c439143400f1ea1845db37e7faf93009350254c173c4003400c3996f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144862"
---
# <a name="connecting-to-a-capture-driver"></a>Connexion à un pilote de capture

L’exemple suivant connecte la fenêtre de capture avec le handle *hWndC* au pilote msvideo, puis les déconnecte à l’aide de la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) :


```C++
fOK = SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0, 0L); 
// 
// Or, use the macro to connect to the MSVIDEO driver: 
// fOK = capDriverConnect(hWndC, 0); 
// 
// Place code to set up and capture video here. 
// 
capDriverDisconnect (hWndC); 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




