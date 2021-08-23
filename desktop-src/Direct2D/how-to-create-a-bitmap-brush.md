---
title: Comment créer un pinceau bitmap
description: Montre comment créer un pinceau bitmap à l’aide de Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274d359b8ad8298a4e45d01014a6e9b19aa58c4b81725c5d8c41ac931e24eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569293"
---
# <a name="how-to-create-a-bitmap-brush"></a>Comment créer un pinceau bitmap

Pour créer un pinceau bitmap, utilisez la méthode [**ID2D1RenderTarget :: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) et spécifiez les propriétés du pinceau bitmap. Certaines surcharges vous permettent de spécifier les propriétés de pinceau. Le code suivant montre comment créer un pinceau bitmap pour remplir un carré et un pinceau noir Uni pour dessiner le contour du carré. Le code génère la sortie illustrée dans la capture d’écran suivante.

> [!Note]  
> à partir de Windows 8, vous pouvez utiliser la méthode [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) sur l’interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pour créer un [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) à la place d’un **ID2D1BitmapBrush**. **ID2D1BitmapBrush1** ajoute des modes de mise à l’échelle de haute qualité au pinceau bitmap.

 

![capture d’écran d’un carré rempli d’une image bitmap de plante](images/brushes-ovw-bitmap.png)

1.  Déclarez une variable de type [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  Charger une image bitmap à partir d’une ressource. Pour plus d’informations, consultez [Comment charger une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md).
    ```C++
    // Create the bitmap to be used by the bitmap brush.
    if (SUCCEEDED(hr))
    {
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"FERN",
            L"Image",
            &m_pBitmap
            );
    ```

    

3.  Choisissez les modes d’extension ([**d2d1 \_ Extend \_ mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) et le mode d’interpolation ([**\_ \_ \_ mode d’interpolation de bitmap d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) du pinceau bitmap, puis appelez la méthode [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) pour créer un pinceau, comme illustré dans le code suivant.
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 