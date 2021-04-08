---
title: Obtention et définition du format vidéo
description: Obtention et définition du format vidéo
ms.assetid: 0e6baf24-7a79-45ab-9fc7-69334419956d
keywords:
- capGetVideoFormat macro)
- capGetVideoFormatSize macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6890c3a1d653d43d24c5baa0790cc0d26040685b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842258"
---
# <a name="obtaining-and-setting-the-video-format"></a>Obtention et définition du format vidéo

La structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) est de longueur variable pour tenir compte des formats de données standard et compressés. Étant donné que cette structure est de longueur variable, les applications doivent toujours interroger la taille de la structure et allouer de la mémoire avant de récupérer le format vidéo actuel. L’exemple suivant utilise la macro [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) pour récupérer la taille de la mémoire tampon, puis appelle la macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) pour récupérer le format vidéo actuel.


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



Les applications peuvent utiliser la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (ou le message [**WM \_ Cap \_ Set \_ VIDEOFORMAT**](wm-cap-set-videoformat.md) ) pour envoyer une structure d’en-tête [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) à la fenêtre de capture. Étant donné que les formats vidéo sont spécifiques aux appareils, votre application doit vérifier la valeur de retour pour déterminer si le format a été accepté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 