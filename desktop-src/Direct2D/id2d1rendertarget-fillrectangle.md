---
title: Méthodes ID2D1RenderTarget FillRectangle (D2d1 \_ 1. h)
description: Peint l’intérieur du rectangle spécifié.
ms.assetid: 08e498f9-b564-4da6-ba9b-bff08964ce08
keywords:
- Méthodes FillRectangle Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 21339e535aec294b3737f8a81ce313d524004bcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541007"
---
# <a name="id2d1rendertargetfillrectangle-methods"></a><span data-ttu-id="89a4a-104">ID2D1RenderTarget :: FillRectangle, méthodes</span><span class="sxs-lookup"><span data-stu-id="89a4a-104">ID2D1RenderTarget::FillRectangle methods</span></span>

<span data-ttu-id="89a4a-105">Peint l’intérieur du rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="89a4a-105">Paints the interior of the specified rectangle.</span></span>

### <a name="overload-list"></a><span data-ttu-id="89a4a-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="89a4a-106">Overload list</span></span>



| <span data-ttu-id="89a4a-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="89a4a-107">Method</span></span>                                                                                                               | <span data-ttu-id="89a4a-108">Description</span><span class="sxs-lookup"><span data-stu-id="89a4a-108">Description</span></span>                                                 |
|:---------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------|
| <span data-ttu-id="89a4a-109">[**FillRectangle (D2D1 \_ rect \_ F&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="89a4a-109">[**FillRectangle(D2D1\_RECT\_F&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush))</span></span>  | <span data-ttu-id="89a4a-110">Peint l’intérieur du rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="89a4a-110">Paints the interior of the specified rectangle.</span></span> <br/> |
| <span data-ttu-id="89a4a-111">[**FillRectangle (D2D1 \_ rect \_ F \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="89a4a-111">[**FillRectangle(D2D1\_RECT\_F\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush))</span></span> | <span data-ttu-id="89a4a-112">Peint l’intérieur du rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="89a4a-112">Paints the interior of the specified rectangle.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="89a4a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="89a4a-113">Remarks</span></span>

<span data-ttu-id="89a4a-114">Cette méthode ne retourne pas de code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="89a4a-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="89a4a-115">Pour déterminer si une opération de dessin (par exemple, **FillRectangle**) a échoué, vérifiez les résultats retournés par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="89a4a-115">To determine whether a drawing operation (such as **FillRectangle**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="89a4a-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="89a4a-116">Examples</span></span>

<span data-ttu-id="89a4a-117">L’exemple suivant utilise un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) pour dessiner et remplir plusieurs rectangles.</span><span class="sxs-lookup"><span data-stu-id="89a4a-117">The following example uses an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) to draw and fill several rectangles.</span></span> <span data-ttu-id="89a4a-118">Cet exemple produit la sortie représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="89a4a-118">This example produces the output shown in the following illustration.</span></span>

![illustration de deux rectangles sur un arrière-plan de grille](images/drawrectangleexample-small.png)


```C++
// This method discards device-specific
// resources if the Direct3D device dissapears during execution and
// recreates the resources the next time it's invoked.
HRESULT DemoApp::OnRender()
{
    HRESULT hr = S_OK;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();

        // Draw a grid background.
        int width = static_cast<int>(rtSize.width);
        int height = static_cast<int>(rtSize.height);

        for (int x = 0; x < width; x += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y < height; y += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        // Draw two rectangles.
        D2D1_RECT_F rectangle1 = D2D1::RectF(
            rtSize.width/2 - 50.0f,
            rtSize.height/2 - 50.0f,
            rtSize.width/2 + 50.0f,
            rtSize.height/2 + 50.0f
            );

        D2D1_RECT_F rectangle2 = D2D1::RectF(
            rtSize.width/2 - 100.0f,
            rtSize.height/2 - 100.0f,
            rtSize.width/2 + 100.0f,
            rtSize.height/2 + 100.0f
            );


        // Draw a filled rectangle.
        m_pRenderTarget->FillRectangle(&amp;rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&amp;rectangle2, m_pCornflowerBlueBrush);

        hr = m_pRenderTarget->EndDraw();
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="89a4a-120">Pour obtenir un didacticiel connexe, consultez [création d’une application Direct2D simple](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="89a4a-120">For a related tutorial, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89a4a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89a4a-121">Requirements</span></span>



| <span data-ttu-id="89a4a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89a4a-122">Requirement</span></span> | <span data-ttu-id="89a4a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="89a4a-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a4a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="89a4a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="89a4a-125"><dt>D2d1 \_ 1. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89a4a-125"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="89a4a-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="89a4a-126">Library</span></span><br/> | <dl> <span data-ttu-id="89a4a-127"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89a4a-127"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="89a4a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="89a4a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="89a4a-129"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a4a-129"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="89a4a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89a4a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a4a-131">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="89a4a-131">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="89a4a-132">Création d’une application Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="89a4a-132">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

<span data-ttu-id="89a4a-133">�</span><span class="sxs-lookup"><span data-stu-id="89a4a-133">�</span></span>

<span data-ttu-id="89a4a-134">�</span><span class="sxs-lookup"><span data-stu-id="89a4a-134">�</span></span>
