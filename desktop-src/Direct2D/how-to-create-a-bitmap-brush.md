---
title: Comment créer un pinceau bitmap
description: Montre comment créer un pinceau bitmap à l’aide de Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8f28735368916d1abd0c1c9aa091dec4fd93f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510484"
---
# <a name="how-to-create-a-bitmap-brush"></a><span data-ttu-id="e11d4-103">Comment créer un pinceau bitmap</span><span class="sxs-lookup"><span data-stu-id="e11d4-103">How to Create a Bitmap Brush</span></span>

<span data-ttu-id="e11d4-104">Pour créer un pinceau bitmap, utilisez la méthode [**ID2D1RenderTarget :: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) et spécifiez les propriétés du pinceau bitmap.</span><span class="sxs-lookup"><span data-stu-id="e11d4-104">To create a bitmap brush, use the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the bitmap brush properties.</span></span> <span data-ttu-id="e11d4-105">Certaines surcharges vous permettent de spécifier les propriétés de pinceau.</span><span class="sxs-lookup"><span data-stu-id="e11d4-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="e11d4-106">Le code suivant montre comment créer un pinceau bitmap pour remplir un carré et un pinceau noir Uni pour dessiner le contour du carré.</span><span class="sxs-lookup"><span data-stu-id="e11d4-106">The following code shows how to create a bitmap brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="e11d4-107">Le code génère la sortie illustrée dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="e11d4-107">The code produces the output shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="e11d4-108">À compter de Windows 8, vous pouvez utiliser la méthode [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) sur l’interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pour créer un [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) à la place d’un **ID2D1BitmapBrush**.</span><span class="sxs-lookup"><span data-stu-id="e11d4-108">Starting with Windows 8, you can use the [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface to create a [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) instead of a **ID2D1BitmapBrush**.</span></span> <span data-ttu-id="e11d4-109">**ID2D1BitmapBrush1** ajoute des modes de mise à l’échelle de haute qualité au pinceau bitmap.</span><span class="sxs-lookup"><span data-stu-id="e11d4-109">**ID2D1BitmapBrush1** adds high-quality scaling modes to the bitmap brush.</span></span>

 

![capture d’écran d’un carré rempli d’une image bitmap de plante](images/brushes-ovw-bitmap.png)

1.  <span data-ttu-id="e11d4-111">Déclarez une variable de type [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="e11d4-111">Declare a variable of type [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  <span data-ttu-id="e11d4-112">Charger une image bitmap à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="e11d4-112">Load a bitmap from a resource.</span></span> <span data-ttu-id="e11d4-113">Pour plus d’informations, consultez [Comment charger une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="e11d4-113">For more information, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
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

    

3.  <span data-ttu-id="e11d4-114">Choisissez les modes d’extension ([**d2d1 \_ Extend \_ mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) et le mode d’interpolation ([**\_ \_ \_ mode d’interpolation de bitmap d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) du pinceau bitmap, puis appelez la méthode [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) pour créer un pinceau, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e11d4-114">Choose the extend modes ([**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) and interpolation mode ([**D2D1\_BITMAP\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) of the bitmap brush and then call the [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method to create a brush, as shown in the following code.</span></span>
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e11d4-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e11d4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e11d4-116">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="e11d4-116">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 