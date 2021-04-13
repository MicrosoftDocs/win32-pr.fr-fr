---
title: Comment créer un pinceau de dégradé radial
description: Montre comment créer un pinceau de dégradé radial à l’aide de Direct2D.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe3509a80f80132f4a5e5d65f62476be1cac61d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199283"
---
# <a name="how-to-create-a-radial-gradient-brush"></a><span data-ttu-id="18a6f-103">Comment créer un pinceau de dégradé radial</span><span class="sxs-lookup"><span data-stu-id="18a6f-103">How to Create a Radial Gradient Brush</span></span>

<span data-ttu-id="18a6f-104">Pour créer un pinceau de dégradé radial, utilisez la méthode [**ID2DRenderTarget :: CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) et spécifiez les propriétés de pinceau de dégradé radial et la collection de points de dégradé.</span><span class="sxs-lookup"><span data-stu-id="18a6f-104">To create a radial gradient brush, use the [**ID2DRenderTarget::CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) method and specify the radial gradient brush properties and the gradient stop collection.</span></span> <span data-ttu-id="18a6f-105">Certaines surcharges vous permettent de spécifier les propriétés de pinceau.</span><span class="sxs-lookup"><span data-stu-id="18a6f-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="18a6f-106">Le code suivant montre comment créer un pinceau de dégradé radial pour remplir un cercle et un pinceau noir Uni pour dessiner le contour du cercle.</span><span class="sxs-lookup"><span data-stu-id="18a6f-106">The following code shows how to create a radial gradient brush to fill a circle, and a solid black brush to draw the outline of the circle.</span></span>

<span data-ttu-id="18a6f-107">Le code génère la sortie illustrée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="18a6f-107">The code produces the output shown in the following illustration.</span></span>

![illustration d’un cercle rempli d’un pinceau de dégradé radial](images/brushes-ovw-radials.png)

1.  <span data-ttu-id="18a6f-109">Déclarez une variable de type [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="18a6f-109">Declare a variable of type [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  <span data-ttu-id="18a6f-110">Créez un tableau de structures de [**\_ \_ point de dégradé d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) à placer dans la collection d’arrêts de dégradé.</span><span class="sxs-lookup"><span data-stu-id="18a6f-110">Create an array of [**D2D1\_GRADIENT\_STOP**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures to put in the gradient stop collection.</span></span> <span data-ttu-id="18a6f-111">La structure du **\_ \_ point de dégradé d2d1** contient la position et la couleur d’un point de dégradé.</span><span class="sxs-lookup"><span data-stu-id="18a6f-111">The **D2D1\_GRADIENT\_STOP** structure contains the position and color of a gradient stop.</span></span> <span data-ttu-id="18a6f-112">La position indique la position relative du point de dégradé dans le pinceau.</span><span class="sxs-lookup"><span data-stu-id="18a6f-112">The position indicates the relative position of the gradient stop in the brush.</span></span> <span data-ttu-id="18a6f-113">La valeur est comprise dans la plage \[ 0.0 f, 1.0 f \] , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="18a6f-113">The value is in the range \[0.0f, 1.0f\], as shown in the following code.</span></span>

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

    

3.  <span data-ttu-id="18a6f-114">Utilisez la méthode [**ID2D1RenderTarget :: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) pour créer la collection [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir d’un tableau précédemment déclaré de structures de [**\_ \_ point de dégradé d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="18a6f-114">Use the [**ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) method to create the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) collection from a previously declared array of [**D2D1\_GRADIENT\_STOP**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures.</span></span> <span data-ttu-id="18a6f-115">Utilisez ensuite [**CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) pour créer un pinceau de dégradé radial.</span><span class="sxs-lookup"><span data-stu-id="18a6f-115">Then, Use the [**CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) to create a radial gradient brush.</span></span>

    > [!Note]  
    > <span data-ttu-id="18a6f-116">À compter de Windows 8, vous pouvez utiliser la méthode [**ID2D1DeviceContext :: CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) pour créer une collection [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) à la place de la méthode [**ID2D1RenderTarget :: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) .</span><span class="sxs-lookup"><span data-stu-id="18a6f-116">Starting with Windows 8, you can use the [**ID2D1DeviceContext::CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) method to create a [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) collection instead of the [**ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) method.</span></span> <span data-ttu-id="18a6f-117">Cette interface ajoute des dégradés de haute couleur et l’interpolation des dégradés dans les couleurs droites ou prmultiplied.</span><span class="sxs-lookup"><span data-stu-id="18a6f-117">This interface adds high-color gradients and the interpolation of gradients in either straight or prmultiplied colors.</span></span> <span data-ttu-id="18a6f-118">Pour plus d’informations, consultez la page **ID2DDeviceContext :: CreateGradientStopCollection** .</span><span class="sxs-lookup"><span data-stu-id="18a6f-118">See the **ID2DDeviceContext::CreateGradientStopCollection** page for more information.</span></span>

     

    ```C++
    // The center of the gradient is in the center of the box.
    // The gradient origin offset was set to zero(0, 0) or center in this case.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateRadialGradientBrush(
            D2D1::RadialGradientBrushProperties(
                D2D1::Point2F(75, 75),
                D2D1::Point2F(0, 0),
                75,
                75),
            pGradientStops,
            &m_pRadialGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
    m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="18a6f-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18a6f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18a6f-120">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="18a6f-120">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 