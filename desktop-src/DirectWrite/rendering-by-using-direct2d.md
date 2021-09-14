---
title: Rendu à l’aide de Direct2D
description: Direct2D fournit des méthodes pour le rendu de texte avec une mise en forme décrite par uniquement un IDWriteTextFormat ou un IDWriteTextLayout à une surface Direct2D.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58af17e15bcb9bd52461a2da3110982fb04e4c0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009978"
---
# <a name="render-using-direct2d"></a>Rendu à l’aide de Direct2D

Direct2D fournit des méthodes pour le rendu de texte avec une mise en forme décrite par uniquement un [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) à une surface Direct2D.

## <a name="rendering-text-described-by-idwritetextformat"></a>Rendu du texte décrit par IDWriteTextFormat

Pour afficher une chaîne à l’aide d’un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pour décrire la mise en forme de la chaîne entière, utilisez la méthode [**ID2D1RenderTarget ::D Rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) fournie par [Direct2D](../direct2d/direct2d-portal.md).

1.  Définissez la zone pour la disposition du texte en extrayant les dimensions de la zone de rendu et créez un rectangle [Direct2D](../direct2d/direct2d-portal.md) qui a les mêmes dimensions.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Utilisez la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) et l’objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pour afficher du texte à l’écran. La méthode **ID2D1RenderTarget ::D rawtext** accepte les paramètres suivants :
    -   Chaîne à restituer.
    -   Pointeur vers une interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .
    -   Rectangle de disposition [Direct2D](../direct2d/direct2d-portal.md) .
    -   Pointeur vers une interface qui expose [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a>Rendu d’un objet de disposition IDWriteText

Pour dessiner le texte avec les paramètres de disposition du texte spécifiés par l’objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , modifiez le code de la méthode MultiformattedText ::D rawtext de sorte qu’il utilise [**IDWriteTextLayout ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Delcare une variable [**d2d1 \_ point \_ 2F**](../direct2d/d2d1-point-2f.md) et définissez-la sur le point supérieur gauche de la fenêtre.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Dessinez le texte à l’écran en appelant la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) de la cible de rendu [Direct2D](../direct2d/direct2d-portal.md) et en passant le pointeur [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 