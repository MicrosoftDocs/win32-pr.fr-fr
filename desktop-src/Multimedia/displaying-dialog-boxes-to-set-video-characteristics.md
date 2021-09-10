---
title: Affichage des boîtes de dialogue pour définir les caractéristiques de la vidéo
description: Affichage des boîtes de dialogue pour définir les caractéristiques de la vidéo
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- CAPDRIVERCAPS, structure
- capDriverGetCaps macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73eea12d69a3d23b0345bee3495d32cbb1ad0ffe
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367820"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a>Affichage des boîtes de dialogue pour définir les caractéristiques de la vidéo

Chaque pilote de capture peut fournir jusqu’à trois boîtes de dialogue différentes utilisées pour contrôler les aspects de la numérisation vidéo et du processus de capture. L’exemple suivant montre comment afficher ces boîtes de dialogue. Avant d’afficher chaque boîte de dialogue, l’exemple appelle la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) et vérifie la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) retournée pour voir si le pilote de capture peut l’afficher.


```C++
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

CAPDRIVERCAPS CapDriverCaps = { }; 
CAPSTATUS     CapStatus = { };

capDriverGetCaps(hWndC, &CapDriverCaps, sizeof(CAPDRIVERCAPS)); 
 
// Video source dialog box. 
if (CapDriverCaps.fHasDlgVideoSource)
{
    capDlgVideoSource(hWndC); 
}
 
// Video format dialog box. 
if (CapDriverCaps.fHasDlgVideoFormat) 
{
    capDlgVideoFormat(hWndC); 

    // Are there new image dimensions?
    capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS));

    // If so, notify the parent of a size change.
} 
 
// Video display dialog box. 
if (CapDriverCaps.fHasDlgVideoDisplay)
{
    capDlgVideoDisplay(hWndC); 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> <dt>

[**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




