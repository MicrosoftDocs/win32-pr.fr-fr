---
title: Comment créer un pinceau de couleur unie
description: Montre comment créer un pinceau de couleur unie à l’aide de Direct2D.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bc6fbf5df42386f5e0e5a843a1906d36d4fc8c71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941073"
---
# <a name="how-to-create-a-solid-color-brush"></a><span data-ttu-id="568a7-103">Comment créer un pinceau de couleur unie</span><span class="sxs-lookup"><span data-stu-id="568a7-103">How to Create a Solid Color Brush</span></span>

<span data-ttu-id="568a7-104">Pour créer un pinceau de couleur unie, utilisez la méthode [**ID2DRenderTarget :: CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) et spécifiez la couleur avec laquelle vous souhaitez peindre.</span><span class="sxs-lookup"><span data-stu-id="568a7-104">To create a solid color brush, use the [**ID2DRenderTarget::CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method and specify the color with which you want to paint.</span></span> <span data-ttu-id="568a7-105">Certaines surcharges **CreateSolidColorBrush** vous permettent également de spécifier l’opacité du pinceau.</span><span class="sxs-lookup"><span data-stu-id="568a7-105">Some of the **CreateSolidColorBrush** overloads also enable you to specify the opacity of the brush.</span></span>

<span data-ttu-id="568a7-106">Le code suivant montre comment créer un pinceau Uni vert jaune pour remplir un carré et un pinceau noir Uni pour dessiner le contour du carré.</span><span class="sxs-lookup"><span data-stu-id="568a7-106">The following code shows how to create a solid yellow-green brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="568a7-107">Le code génère la sortie illustrée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="568a7-107">The code produces the output shown in the following illustration.</span></span>

![illustration d’un rectangle rempli d’une couleur unie jaune-vert](images/brushes-ovw-solidcolor.png)

1.  <span data-ttu-id="568a7-109">Déclarez deux pointeurs [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) : un pour peindre le noir et un pour peindre jaune vert.</span><span class="sxs-lookup"><span data-stu-id="568a7-109">Declare two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pointers: one for painting black and one for painting yellow green.</span></span>
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  <span data-ttu-id="568a7-110">Appelez la méthode [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pour créer les pinceaux :</span><span class="sxs-lookup"><span data-stu-id="568a7-110">Call the [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method to create the brushes:</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
            &m_pBlackBrush
            );
    }

    // Create a solid color brush with its rgb value 0x9ACD32.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
            &m_pYellowGreenBrush
            );
    }
    ```

    

3.  <span data-ttu-id="568a7-111">Appelez la méthode [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) pour peindre l’intérieur du rectangle avec le pinceau vert jaune et la méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) pour peindre le contour du rectangle avec le pinceau noir :</span><span class="sxs-lookup"><span data-stu-id="568a7-111">Call the [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the rectangle with the yellow green brush and the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the rectangle with the black brush:</span></span>
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="568a7-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="568a7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="568a7-113">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="568a7-113">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 