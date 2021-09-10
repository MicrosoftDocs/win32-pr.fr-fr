---
title: aperçu de la vidéo (Windows multimédia)
description: cet exemple dans Windows multimédia utilise capPreviewRate pour définir la fréquence d’affichage des frames pour le mode aperçu et capPreview pour placer la fenêtre de capture en mode aperçu.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview macro)
- capPreviewRate macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc3aaeb9a8ff0f040218fca4822af93ab8bfe29
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368068"
---
# <a name="previewing-video-windows-multimedia"></a>aperçu de la vidéo (Windows multimédia)

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

 

 




