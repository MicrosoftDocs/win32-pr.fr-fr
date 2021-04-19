---
title: Méthodes ID2D1RenderTarget FillRoundedRectangle (D2d1. h)
description: Peint l’intérieur du rectangle arrondi spécifié.
ms.assetid: 9c4765b0-858f-4a20-b044-0acf87a1f131
keywords:
- Méthodes FillRoundedRectangle Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 2abc39ed364de0653813aab14ee5777ccf3c4e08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539588"
---
# <a name="id2d1rendertargetfillroundedrectangle-methods"></a><span data-ttu-id="d863f-104">ID2D1RenderTarget :: FillRoundedRectangle, méthodes</span><span class="sxs-lookup"><span data-stu-id="d863f-104">ID2D1RenderTarget::FillRoundedRectangle methods</span></span>

<span data-ttu-id="d863f-105">Peint l’intérieur du rectangle arrondi spécifié.</span><span class="sxs-lookup"><span data-stu-id="d863f-105">Paints the interior of the specified rounded rectangle.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d863f-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="d863f-106">Overload list</span></span>



| <span data-ttu-id="d863f-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="d863f-107">Method</span></span>                                                                                                                                          | <span data-ttu-id="d863f-108">Description</span><span class="sxs-lookup"><span data-stu-id="d863f-108">Description</span></span>                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span data-ttu-id="d863f-109">[**FillRoundedRectangle (D2D1 \_ \_ , rectangle arrondi&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="d863f-109">[**FillRoundedRectangle(D2D1\_ROUNDED\_RECT&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))</span></span>  | <span data-ttu-id="d863f-110">Peint l’intérieur du rectangle arrondi spécifié.</span><span class="sxs-lookup"><span data-stu-id="d863f-110">Paints the interior of the specified rounded rectangle.</span></span> <br/> |
| <span data-ttu-id="d863f-111">[**FillRoundedRectangle (D2D1 \_ arrondit \_ \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="d863f-111">[**FillRoundedRectangle(D2D1\_ROUNDED\_RECT\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))</span></span> | <span data-ttu-id="d863f-112">Peint l’intérieur du rectangle arrondi spécifié.</span><span class="sxs-lookup"><span data-stu-id="d863f-112">Paints the interior of the specified rounded rectangle.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="d863f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d863f-113">Remarks</span></span>

<span data-ttu-id="d863f-114">Cette méthode ne retourne pas de code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="d863f-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="d863f-115">Pour déterminer si une opération de dessin (telle que **FillRoundedRectangle**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="d863f-115">To determine whether a drawing operation (such as **FillRoundedRectangle**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="d863f-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="d863f-116">Examples</span></span>

<span data-ttu-id="d863f-117">L’exemple suivant utilise les méthodes [**DrawRoundedRectangle**](id2d1rendertarget-drawroundedrectangle.md) et **FillRoundedRectangle** pour définir le contour et le remplissage d’un rectangle à coins arrondis.</span><span class="sxs-lookup"><span data-stu-id="d863f-117">The following example uses the [**DrawRoundedRectangle**](id2d1rendertarget-drawroundedrectangle.md) and **FillRoundedRectangle** methods to outline and fill a rounded rectangle.</span></span> <span data-ttu-id="d863f-118">Cet exemple produit la sortie représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d863f-118">This example produces the output shown in the following illustration.</span></span>

![illustration de quatre rectangles arrondis avec différents styles et remplissages de trait](images/drawroundedrectangle-scr.png)


```C++
//  Called whenever the application needs to display the client
//  window.
HRESULT DrawAndFillRoundedRectangleExample::OnRender()
{
    HRESULT hr;

    // Create the render target and brushes if they
    // don't already exists.
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

        // Define a rounded rectangle.
        D2D1_ROUNDED_RECT roundedRect = D2D1::RoundedRect(
            D2D1::RectF(20.f, 20.f, 150.f, 100.f),
            10.f,
            10.f
            );

        // Draw the rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f);

        // Apply a translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 0.f));

        // Draw the rounded rectangle again, this time with a dashed stroke.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(0.f, 150.f));

        // Draw, then fill the rounded rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 150.f));

        // Fill, then draw the rounded rectangle.
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

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



## <a name="requirements"></a><span data-ttu-id="d863f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d863f-120">Requirements</span></span>



| <span data-ttu-id="d863f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d863f-121">Requirement</span></span> | <span data-ttu-id="d863f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d863f-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d863f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d863f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d863f-124"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="d863f-124"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="d863f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d863f-125">Library</span></span><br/> | <dl> <span data-ttu-id="d863f-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d863f-126"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="d863f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d863f-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="d863f-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d863f-128"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d863f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d863f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d863f-130">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="d863f-130">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="d863f-131">Comment dessiner et remplir une forme de base</span><span class="sxs-lookup"><span data-stu-id="d863f-131">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> <dt>

[<span data-ttu-id="d863f-132">**D2D1::RoundedRect**</span><span class="sxs-lookup"><span data-stu-id="d863f-132">**D2D1::RoundedRect**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1roundedrectanglegeometry-getroundedrect)
</dt> </dl>

<span data-ttu-id="d863f-133">�</span><span class="sxs-lookup"><span data-stu-id="d863f-133">�</span></span>

<span data-ttu-id="d863f-134">�</span><span class="sxs-lookup"><span data-stu-id="d863f-134">�</span></span>
