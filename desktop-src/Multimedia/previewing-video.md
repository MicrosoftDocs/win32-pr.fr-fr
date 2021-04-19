---
title: Aperçu de la vidéo (Windows Multimedia)
description: Aperçu de la vidéo
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview macro)
- capPreviewRate macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79c8e24d30fd5141b5b1ac14de99d83e0b2bc620
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106510509"
---
# <a name="previewing-video-windows-multimedia"></a>Aperçu de la vidéo (Windows Multimedia)

L’exemple suivant utilise la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) pour définir la fréquence d’affichage des frames pour le mode aperçu à 66 millisecondes par image, puis utilise la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) pour placer la fenêtre de capture en mode aperçu.


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




