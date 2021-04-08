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
# <a name="obtaining-and-setting-the-video-format"></a><span data-ttu-id="bf27b-105">Obtention et définition du format vidéo</span><span class="sxs-lookup"><span data-stu-id="bf27b-105">Obtaining and Setting the Video Format</span></span>

<span data-ttu-id="bf27b-106">La structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) est de longueur variable pour tenir compte des formats de données standard et compressés.</span><span class="sxs-lookup"><span data-stu-id="bf27b-106">The [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure is of variable length to accommodate standard and compressed data formats.</span></span> <span data-ttu-id="bf27b-107">Étant donné que cette structure est de longueur variable, les applications doivent toujours interroger la taille de la structure et allouer de la mémoire avant de récupérer le format vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="bf27b-107">Because this structure is of variable length, applications must always query the size of the structure and allocate memory before retrieving the current video format.</span></span> <span data-ttu-id="bf27b-108">L’exemple suivant utilise la macro [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) pour récupérer la taille de la mémoire tampon, puis appelle la macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) pour récupérer le format vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="bf27b-108">The following example uses the [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macro to retrieve the buffer size and then calls the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) macro to retrieve the current video format.</span></span>


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



<span data-ttu-id="bf27b-109">Les applications peuvent utiliser la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) (ou le message [**WM \_ Cap \_ Set \_ VIDEOFORMAT**](wm-cap-set-videoformat.md) ) pour envoyer une structure d’en-tête [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) à la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="bf27b-109">Applications can use the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro (or the [**WM\_CAP\_SET\_VIDEOFORMAT**](wm-cap-set-videoformat.md) message) to send a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) header structure to the capture window.</span></span> <span data-ttu-id="bf27b-110">Étant donné que les formats vidéo sont spécifiques aux appareils, votre application doit vérifier la valeur de retour pour déterminer si le format a été accepté.</span><span class="sxs-lookup"><span data-stu-id="bf27b-110">Because video formats are device specific, your application should check the return value to determine if the format was accepted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf27b-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf27b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf27b-112">Utilisation de la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="bf27b-112">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 