---
title: Rendu à l’aide de Direct2D
description: Direct2D fournit des méthodes pour le rendu de texte avec une mise en forme décrite par uniquement un IDWriteTextFormat ou un IDWriteTextLayout à une surface Direct2D.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58af17e15bcb9bd52461a2da3110982fb04e4c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031781"
---
# <a name="render-using-direct2d"></a><span data-ttu-id="9ad2f-103">Rendu à l’aide de Direct2D</span><span class="sxs-lookup"><span data-stu-id="9ad2f-103">Render Using Direct2D</span></span>

<span data-ttu-id="9ad2f-104">Direct2D fournit des méthodes pour le rendu de texte avec une mise en forme décrite par uniquement un [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) à une surface Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9ad2f-104">Direct2D provides methods for rendering either text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) or an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to a Direct2D surface.</span></span>

## <a name="rendering-text-described-by-idwritetextformat"></a><span data-ttu-id="9ad2f-105">Rendu du texte décrit par IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="9ad2f-105">Rendering Text Described by IDWriteTextFormat</span></span>

<span data-ttu-id="9ad2f-106">Pour afficher une chaîne à l’aide d’un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pour décrire la mise en forme de la chaîne entière, utilisez la méthode [**ID2D1RenderTarget ::D Rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) fournie par [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="9ad2f-106">To render a string using an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to describe the formatting for the entire string, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method provided by [Direct2D](../direct2d/direct2d-portal.md).</span></span>

1.  <span data-ttu-id="9ad2f-107">Définissez la zone pour la disposition du texte en extrayant les dimensions de la zone de rendu et créez un rectangle [Direct2D](../direct2d/direct2d-portal.md) qui a les mêmes dimensions.</span><span class="sxs-lookup"><span data-stu-id="9ad2f-107">Define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="9ad2f-108">Utilisez la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) et l’objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pour afficher du texte à l’écran.</span><span class="sxs-lookup"><span data-stu-id="9ad2f-108">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="9ad2f-109">La méthode **ID2D1RenderTarget ::D rawtext** accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9ad2f-109">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="9ad2f-110">Chaîne à restituer.</span><span class="sxs-lookup"><span data-stu-id="9ad2f-110">A string to render.</span></span>
    -   <span data-ttu-id="9ad2f-111">Pointeur vers une interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="9ad2f-111">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="9ad2f-112">Rectangle de disposition [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9ad2f-112">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="9ad2f-113">Pointeur vers une interface qui expose [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span><span class="sxs-lookup"><span data-stu-id="9ad2f-113">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a><span data-ttu-id="9ad2f-114">Rendu d’un objet de disposition IDWriteText</span><span class="sxs-lookup"><span data-stu-id="9ad2f-114">Rendering a IDWriteText Layout Object</span></span>

<span data-ttu-id="9ad2f-115">Pour dessiner le texte avec les paramètres de disposition du texte spécifiés par l’objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , modifiez le code de la méthode MultiformattedText ::D rawtext de sorte qu’il utilise [**IDWriteTextLayout ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span><span class="sxs-lookup"><span data-stu-id="9ad2f-115">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="9ad2f-116">Delcare une variable [**d2d1 \_ point \_ 2F**](../direct2d/d2d1-point-2f.md) et définissez-la sur le point supérieur gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9ad2f-116">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="9ad2f-117">Dessinez le texte à l’écran en appelant la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) de la cible de rendu [Direct2D](../direct2d/direct2d-portal.md) et en passant le pointeur [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="9ad2f-117">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 