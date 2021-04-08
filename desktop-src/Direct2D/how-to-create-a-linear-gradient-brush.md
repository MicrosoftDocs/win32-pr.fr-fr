---
title: Comment créer un pinceau de dégradé linéaire
description: Montre comment créer un pinceau de dégradé linéaire à l’aide de Direct2D.
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 3a50a6e3ab421e2275644051ed647d5c4501f8e0
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103843025"
---
# <a name="how-to-create-a-linear-gradient-brush"></a><span data-ttu-id="ecbc3-103">Comment créer un pinceau de dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="ecbc3-103">How to Create a Linear Gradient Brush</span></span>

<span data-ttu-id="ecbc3-104">Pour créer un pinceau de dégradé linéaire, utilisez la méthode [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) et spécifiez les propriétés de pinceau de dégradé linéaire et la collection de points de dégradé.</span><span class="sxs-lookup"><span data-stu-id="ecbc3-104">To create a linear gradient brush, use the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and specify the linear gradient brush properties and the gradient stop collection.</span></span> <span data-ttu-id="ecbc3-105">Certaines surcharges vous permettent de spécifier les propriétés de pinceau.</span><span class="sxs-lookup"><span data-stu-id="ecbc3-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="ecbc3-106">Le code suivant montre comment créer un pinceau de dégradé linéaire pour remplir un carré, et un pinceau noir Uni pour dessiner le contour du carré.</span><span class="sxs-lookup"><span data-stu-id="ecbc3-106">The following code shows how to create a linear gradient brush to fill a square, and a solid black brush to draw the outline of the square.</span></span>

<span data-ttu-id="ecbc3-107">Le code génère la sortie illustrée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="ecbc3-107">The code produces the output shown in the following illustration.</span></span>

![illustration d’un carré rempli d’un pinceau de dégradé linéaire](images/brushes-ovw-lineargradient.png)

1.  <span data-ttu-id="ecbc3-109">Déclarez une variable de type [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="ecbc3-109">Declare a variable of type [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  <span data-ttu-id="ecbc3-110">Utilisez la méthode [**ID2D1RenderTarget :: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) pour créer la collection [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) avec un tableau déclaré de structures de [**\_ \_ point de dégradé d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="ecbc3-110">Use the [**ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) method to create the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) collection with a declared array of [**D2D1\_GRADIENT\_STOP**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures, as shown in the following code.</span></span>
    > [!Note]  
    > <span data-ttu-id="ecbc3-111">À compter de Windows 8, vous pouvez utiliser la méthode [**ID2D1DeviceContext :: CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) pour créer une collection [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) à la place.</span><span class="sxs-lookup"><span data-stu-id="ecbc3-111">Starting with Windows 8, you can use the [**ID2D1DeviceContext::CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) method to create a [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) collection instead.</span></span> <span data-ttu-id="ecbc3-112">Cette interface ajoute des dégradés de haute couleur et l’interpolation des dégradés dans les couleurs droites ou prmultiplied.</span><span class="sxs-lookup"><span data-stu-id="ecbc3-112">This interface adds high-color gradients and the interpolation of gradients in either straight or prmultiplied colors.</span></span> <span data-ttu-id="ecbc3-113">Pour plus d’informations, consultez la page **ID2DDeviceContext :: CreateGradientStopCollection** .</span><span class="sxs-lookup"><span data-stu-id="ecbc3-113">See the **ID2DDeviceContext::CreateGradientStopCollection** page for more information.</span></span>

     

    ```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
    ```

    

3.  <span data-ttu-id="ecbc3-114">Utilisez [**ID2D1RenderTarget :: CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) pour créer un pinceau de dégradé linéaire, remplissez le carré avec le pinceau, puis dessinez le carré avec le pinceau de couleur noir.</span><span class="sxs-lookup"><span data-stu-id="ecbc3-114">Use the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) to create a linear gradient brush, fill the square with the brush, and draw the square with the black color brush.</span></span>
    ```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ecbc3-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ecbc3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecbc3-116">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="ecbc3-116">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 
