---
title: Obtention des fonctionnalités d’un pilote de capture
description: Obtention des fonctionnalités d’un pilote de capture
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- Message WM_CAP_DRIVER_GET_CAPS
- capDriverGetCaps macro)
- CAPDRIVERCAPS, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6f717f1a7c19878ceeca2cccc2db309be3e62e0febf90dcb23376db73eed17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806569"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a>Obtention des fonctionnalités d’un pilote de capture

Le message [**WM \_ Cap Driver to Cap \_ \_ \_**](wm-cap-driver-get-caps.md) retourne les fonctionnalités du pilote de capture et du matériel sous-jacent dans la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) . Chaque fois qu’une application connecte un nouveau pilote de capture à la fenêtre de capture, elle doit mettre à jour la structure **CAPDRIVERCAPS** . L’exemple suivant utilise la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) pour obtenir les fonctionnalités du pilote de capture.


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




