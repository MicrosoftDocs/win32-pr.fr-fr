---
title: Comment créer un pinceau de dégradé radial
description: Montre comment créer un pinceau de dégradé radial à l’aide de Direct2D.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1932dc6506c625332d61f4e549ae2dd169060731bfbea344f64c3aa826540ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569263"
---
# <a name="how-to-create-a-radial-gradient-brush"></a>Comment créer un pinceau de dégradé radial

Pour créer un pinceau de dégradé radial, utilisez la méthode [**ID2DRenderTarget :: CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) et spécifiez les propriétés de pinceau de dégradé radial et la collection de points de dégradé. Certaines surcharges vous permettent de spécifier les propriétés de pinceau. Le code suivant montre comment créer un pinceau de dégradé radial pour remplir un cercle et un pinceau noir Uni pour dessiner le contour du cercle.

Le code génère la sortie illustrée dans l’illustration suivante.

![illustration d’un cercle rempli d’un pinceau de dégradé radial](images/brushes-ovw-radials.png)

1.  Déclarez une variable de type [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  Créez un tableau de structures de [**\_ \_ point de dégradé d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) à placer dans la collection d’arrêts de dégradé. La structure du **\_ \_ point de dégradé d2d1** contient la position et la couleur d’un point de dégradé. La position indique la position relative du point de dégradé dans le pinceau. La valeur est comprise dans la plage \[ 0.0 f, 1.0 f \] , comme indiqué dans le code suivant.

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

    

3.  Utilisez la méthode [**ID2D1RenderTarget :: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) pour créer la collection [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir d’un tableau précédemment déclaré de structures de [**\_ \_ point de dégradé d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Utilisez ensuite [**CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) pour créer un pinceau de dégradé radial.

    > [!Note]  
    > à partir de Windows 8, vous pouvez utiliser la méthode [**ID2D1DeviceContext :: CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) pour créer une collection [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) à la place de la méthode [**ID2D1RenderTarget :: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) . Cette interface ajoute des dégradés de haute couleur et l’interpolation des dégradés dans les couleurs droites ou prmultiplied. Pour plus d’informations, consultez la page **ID2DDeviceContext :: CreateGradientStopCollection** .

     

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

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 