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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368471"
---
# <a name="adding-palette-message-handlers"></a>Ajout de gestionnaires de messages de palette

L’exemple suivant illustre des gestionnaires de messages simples pour les messages [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) et [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) . L’exemple utilise la fonction [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) pour traiter le message **WM \_ QUERYNEWPALETTE** .

Votre application doit répondre au message [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) en invalidant la fenêtre de destination pour permettre à la fonction [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) de redessiner une image. Vous devez répondre au message [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) à l’aide de la fonction [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) pour réaliser la palette.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DrawDib](using-drawdib.md)
</dt> </dl>

 

 