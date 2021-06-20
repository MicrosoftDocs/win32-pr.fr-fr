---
title: Aperçu de la vidéo (Windows Multimedia)
description: Cet exemple dans Windows Multimedia utilise capPreviewRate pour définir la fréquence d’affichage des frames pour le mode Aperçu et capPreview pour placer la fenêtre de capture en mode aperçu.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview macro)
- capPreviewRate macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc3aaeb9a8ff0f040218fca4822af93ab8bfe29
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405542"
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

 

 




