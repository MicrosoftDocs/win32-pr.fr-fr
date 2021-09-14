---
title: Comment créer un pinceau de dégradé linéaire
description: Montre comment créer un pinceau de dégradé linéaire à l’aide de Direct2D.
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 3a50a6e3ab421e2275644051ed647d5c4501f8e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113129"
---
# <a name="how-to-create-a-linear-gradient-brush"></a>Comment créer un pinceau de dégradé linéaire

Pour créer un pinceau de dégradé linéaire, utilisez la méthode [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) et spécifiez les propriétés de pinceau de dégradé linéaire et la collection de points de dégradé. Certaines surcharges vous permettent de spécifier les propriétés de pinceau. Le code suivant montre comment créer un pinceau de dégradé linéaire pour remplir un carré, et un pinceau noir Uni pour dessiner le contour du carré.

Le code génère la sortie illustrée dans l’illustration suivante.

![illustration d’un carré rempli d’un pinceau de dégradé linéaire](images/brushes-ovw-lineargradient.png)

1.  Déclarez une variable de type [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  Utilisez la méthode [**ID2D1RenderTarget :: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) pour créer la collection [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) avec un tableau déclaré de structures de [**\_ \_ point de dégradé d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) , comme indiqué dans le code suivant.
    > [!Note]  
    > à partir de Windows 8, vous pouvez utiliser la méthode [**ID2D1DeviceContext :: CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) pour créer une collection [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) à la place. Cette interface ajoute des dégradés de haute couleur et l’interpolation des dégradés dans les couleurs droites ou prmultiplied. Pour plus d’informations, consultez la page **ID2DDeviceContext :: CreateGradientStopCollection** .

     

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

    

3.  Utilisez [**ID2D1RenderTarget :: CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) pour créer un pinceau de dégradé linéaire, remplissez le carré avec le pinceau, puis dessinez le carré avec le pinceau de couleur noir.
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

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 
