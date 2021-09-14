---
title: Comment créer un pinceau de couleur unie
description: Montre comment créer un pinceau de couleur unie à l’aide de Direct2D.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bc6fbf5df42386f5e0e5a843a1906d36d4fc8c71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113122"
---
# <a name="how-to-create-a-solid-color-brush"></a>Comment créer un pinceau de couleur unie

Pour créer un pinceau de couleur unie, utilisez la méthode [**ID2DRenderTarget :: CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) et spécifiez la couleur avec laquelle vous souhaitez peindre. Certaines surcharges **CreateSolidColorBrush** vous permettent également de spécifier l’opacité du pinceau.

Le code suivant montre comment créer un pinceau Uni vert jaune pour remplir un carré et un pinceau noir Uni pour dessiner le contour du carré. Le code génère la sortie illustrée dans l’illustration suivante.

![illustration d’un rectangle rempli d’une couleur unie jaune-vert](images/brushes-ovw-solidcolor.png)

1.  Déclarez deux pointeurs [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) : un pour peindre le noir et un pour peindre jaune vert.
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  Appelez la méthode [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pour créer les pinceaux :
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

    

3.  Appelez la méthode [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) pour peindre l’intérieur du rectangle avec le pinceau vert jaune et la méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) pour peindre le contour du rectangle avec le pinceau noir :
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 