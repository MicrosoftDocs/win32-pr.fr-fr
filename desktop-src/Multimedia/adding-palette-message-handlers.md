---
title: Ajout de gestionnaires de messages de palette
description: Ajout de gestionnaires de messages de palette
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- DrawDib, palettes
- DrawDibRealize fonction)
- DrawDibDraw fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 679990dce5977430eb2a46fc3cd06622246d357f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381918"
---
# <a name="adding-palette-message-handlers"></a><span data-ttu-id="79eae-106">Ajout de gestionnaires de messages de palette</span><span class="sxs-lookup"><span data-stu-id="79eae-106">Adding Palette Message Handlers</span></span>

<span data-ttu-id="79eae-107">L’exemple suivant illustre des gestionnaires de messages simples pour les messages [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) et [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) .</span><span class="sxs-lookup"><span data-stu-id="79eae-107">The following example illustrates simple message handlers for the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages.</span></span> <span data-ttu-id="79eae-108">L’exemple utilise la fonction [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) pour traiter le message **WM \_ QUERYNEWPALETTE** .</span><span class="sxs-lookup"><span data-stu-id="79eae-108">The example uses the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to process the **WM\_QUERYNEWPALETTE** message.</span></span>

<span data-ttu-id="79eae-109">Votre application doit répondre au message [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) en invalidant la fenêtre de destination pour permettre à la fonction [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) de redessiner une image.</span><span class="sxs-lookup"><span data-stu-id="79eae-109">Your application should respond to the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message by invalidating the destination window to let the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function redraw an image.</span></span> <span data-ttu-id="79eae-110">Vous devez répondre au message [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) à l’aide de la fonction [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) pour réaliser la palette.</span><span class="sxs-lookup"><span data-stu-id="79eae-110">You should respond to the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) message by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to realize the palette.</span></span>


```C++
case WM_PALETTECHANGED: 
    if ((HWND)wParam == hwnd) 
        break; 
case WM_QUERYNEWPALETTE: 
    hdc = GetDC(hwnd); 
    f = DrawDibRealize(hdd, hdc, FALSE) > 0; 
    ReleaseDC(hwnd, hdc); 
    if (f) 
        InvalidateRect(hwnd, NULL, TRUE); 
    break; 

```



## <a name="related-topics"></a><span data-ttu-id="79eae-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79eae-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79eae-112">Utilisation de DrawDib</span><span class="sxs-lookup"><span data-stu-id="79eae-112">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 