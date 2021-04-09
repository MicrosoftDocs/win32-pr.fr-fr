---
title: Comment dessiner une image bitmap
description: Montre comment afficher des bitmaps avec Direct2D.
ms.assetid: 9c6fc8b1-47ba-46fa-b812-2636cd8ff2b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfa13b75b4fe34ce6ff2b80598fac35f8483a2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842381"
---
# <a name="how-to-draw-a-bitmap"></a><span data-ttu-id="977cd-103">Comment dessiner une image bitmap</span><span class="sxs-lookup"><span data-stu-id="977cd-103">How to Draw a Bitmap</span></span>

<span data-ttu-id="977cd-104">Pour afficher un bitmap, utilisez la méthode [**ID2D1RenderTarget ::D rawbitmap**](id2d1rendertarget-drawbitmap.md) .</span><span class="sxs-lookup"><span data-stu-id="977cd-104">To render a bitmap, use the [**ID2D1RenderTarget::DrawBitmap**](id2d1rendertarget-drawbitmap.md) method.</span></span> <span data-ttu-id="977cd-105">L’exemple suivant montre comment utiliser la méthode **DrawBitmap** pour dessiner un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="977cd-105">The following example shows how to use the **DrawBitmap** method to draw an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="977cd-106">Elle crée la sortie représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="977cd-106">It creates the output shown in the following illustration.</span></span>

![illustration d’une image bitmap d’origine et des bitmaps résultantes avec des paramètres et des transformations d’opacité différents](images/drawbitmapexample.png)

<span data-ttu-id="977cd-108">Tout d’abord, créez un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="977cd-108">First, create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="977cd-109">L’exemple suivant charge une image bitmap à partir du fichier de ressources de l’application et la stocke sous la forme *m \_ pBitmap*.</span><span class="sxs-lookup"><span data-stu-id="977cd-109">The following example loads a bitmap from the application's resource file and stores it as *m\_pBitmap*.</span></span> <span data-ttu-id="977cd-110">(Pour voir comment la `LoadResourceBitmap` méthode est implémentée, reportez-vous à [la rubrique chargement d’une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md).)</span><span class="sxs-lookup"><span data-stu-id="977cd-110">(To see how the `LoadResourceBitmap` method is implemented, refer to [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).)</span></span>


```C++
// Create a bitmap from an application resource.
hr = LoadResourceBitmap(
    m_pRenderTarget,
    m_pWICFactory,
    L"SampleImage",
    L"Image",
    200,
    0,
    &m_pBitmap
    );
```



<span data-ttu-id="977cd-111">Créez le [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) dans la même méthode que celle où vous avez créé la cible de rendu que vous allez utiliser pour dessiner la bitmap, puis libérez l’image bitmap lorsque la cible de rendu est libérée.</span><span class="sxs-lookup"><span data-stu-id="977cd-111">Create the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) in the same method where you created the render target that you will use to draw the bitmap, and release the bitmap when the render target is released.</span></span>

<span data-ttu-id="977cd-112">Une fois la bitmap créée, affichez-la.</span><span class="sxs-lookup"><span data-stu-id="977cd-112">Once the bitmap is created, render it.</span></span> <span data-ttu-id="977cd-113">L’exemple suivant utilise la méthode [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) pour restituer une bitmap plusieurs fois à l’aide de différents paramètres de taille et d’opacité.</span><span class="sxs-lookup"><span data-stu-id="977cd-113">The following example uses the [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) method to render a bitmap several times using different size and opacity settings.</span></span>


```C++
HRESULT DrawBitmapExample::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        // Paint a grid background.
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
            m_pGridPatternBitmapBrush
            );

        // Retrieve the size of the bitmap.
        D2D1_SIZE_F size = m_pBitmap->GetSize();

        D2D1_POINT_2F upperLeftCorner = D2D1::Point2F(100.f, 10.f);

        // Draw a bitmap.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + size.width,
                upperLeftCorner.y + size.height)
            );

        // Draw the next bitmap below the first one.
        upperLeftCorner.y = upperLeftCorner.y + size.height + 10.f;

        // Scale the bitmap to half its size using the linear
        // interoplation mode and draw it.
        float scaledWidth = size.width / 2.f;
        float scaledHeight = size.height / 2.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw the bitmap at half its size and half its opacity.
        upperLeftCorner.y = upperLeftCorner.y + size.height / 2.f + 10.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw a series of bitmaps with different opacity and
        // rotation angles.
        upperLeftCorner.y = upperLeftCorner.y + scaledHeight + 20.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        D2D1_POINT_2F lowerLeftCorner = D2D1::Point2F(upperLeftCorner.x, upperLeftCorner.y + scaledHeight);
        D2D1_POINT_2F imageCenter = D2D1::Point2F(
            upperLeftCorner.x + scaledWidth / 2,
            upperLeftCorner.y + scaledHeight / 2
            );

        // Rotate the next bitmap by -20 degrees.
        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-20, imageCenter)
            );

        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.75,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-45, imageCenter)
            );

        // Make the last bitmap fully opaque.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



<span data-ttu-id="977cd-114">La méthode [**DrawBitmap**](id2d1rendertarget-drawbitmap.md) ne retourne pas de code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="977cd-114">The [**DrawBitmap**](id2d1rendertarget-drawbitmap.md) method does not return an error code if it fails.</span></span> <span data-ttu-id="977cd-115">Pour déterminer si une opération de dessin (telle que **DrawBitmap**) a échoué, vérifiez le résultat retourné par la méthode [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="977cd-115">To determine whether a drawing operation (such as **DrawBitmap**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method, as shown in the following example.</span></span>


```C++
hr = m_pRenderTarget->EndDraw();
```



<span data-ttu-id="977cd-116">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="977cd-116">Code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="977cd-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="977cd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="977cd-118">**DrawBitmap**</span><span class="sxs-lookup"><span data-stu-id="977cd-118">**DrawBitmap**</span></span>](id2d1rendertarget-drawbitmap.md)
</dt> <dt>

[<span data-ttu-id="977cd-119">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="977cd-119">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="977cd-120">Chargement d’une image bitmap à partir d’une ressource</span><span class="sxs-lookup"><span data-stu-id="977cd-120">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 