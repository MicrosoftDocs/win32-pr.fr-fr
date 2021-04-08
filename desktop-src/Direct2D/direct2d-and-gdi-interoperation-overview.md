---
title: Vue d’ensemble de l’interopérabilité de Direct2D et GDI
description: Décrit comment utiliser Direct2D et GDI ensemble.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, interopérabilité GDI
- Direct2D, interopérabilité
- interopérabilité, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interopérabilité, Graphics Device Interface (GDI)
- Direct3D, interopérabilité
- Direct3D, interopérabilité de Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729661"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a><span data-ttu-id="223e0-111">Vue d’ensemble de l’interopérabilité de Direct2D et GDI</span><span class="sxs-lookup"><span data-stu-id="223e0-111">Direct2D and GDI Interoperability Overview</span></span>

<span data-ttu-id="223e0-112">Cette rubrique explique comment utiliser Direct2D et [GDI](/windows/desktop/gdi/windows-gdi) ensemble.</span><span class="sxs-lookup"><span data-stu-id="223e0-112">This topic describes how to use Direct2D and [GDI](/windows/desktop/gdi/windows-gdi) together.</span></span> <span data-ttu-id="223e0-113">Il existe deux façons de combiner Direct2D avec GDI : vous pouvez écrire du contenu GDI dans une cible de rendu compatible avec GDI Direct2D, ou vous pouvez écrire du contenu Direct2D dans un [contexte de périphérique (DC) GDI](/windows/desktop/gdi/device-contexts).</span><span class="sxs-lookup"><span data-stu-id="223e0-113">There are two ways to combine Direct2D with GDI: you can write GDI content to a Direct2D GDI-compatible render target, or you can write Direct2D content to a [GDI Device Context (DC)](/windows/desktop/gdi/device-contexts).</span></span>

<span data-ttu-id="223e0-114">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="223e0-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="223e0-115">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="223e0-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="223e0-116">Dessiner du contenu Direct2D dans un contexte de périphérique GDI</span><span class="sxs-lookup"><span data-stu-id="223e0-116">Draw Direct2D Content to a GDI Device Context</span></span>](#draw-direct2d-content-to-a-gdi-device-context)
-   [<span data-ttu-id="223e0-117">ID2D1DCRenderTargets, les transformations GDI et les versions de langue de droite à gauche de Windows</span><span class="sxs-lookup"><span data-stu-id="223e0-117">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [<span data-ttu-id="223e0-118">Dessiner du contenu GDI sur une cible de rendu Direct2D GDI-Compatible</span><span class="sxs-lookup"><span data-stu-id="223e0-118">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [<span data-ttu-id="223e0-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="223e0-119">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="223e0-120">Prérequis</span><span class="sxs-lookup"><span data-stu-id="223e0-120">Prerequisites</span></span>

<span data-ttu-id="223e0-121">Cette vue d’ensemble suppose que vous êtes familiarisé avec les opérations de dessin Direct2D de base.</span><span class="sxs-lookup"><span data-stu-id="223e0-121">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="223e0-122">Pour obtenir un didacticiel, consultez le Guide de [démarrage rapide de Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="223e0-122">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="223e0-123">Elle suppose également que vous êtes familiarisé avec les opérations de dessin GDI.</span><span class="sxs-lookup"><span data-stu-id="223e0-123">It also assumes that you are familiar with GDI drawing operations.</span></span>

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a><span data-ttu-id="223e0-124">Dessiner du contenu Direct2D dans un contexte de périphérique GDI</span><span class="sxs-lookup"><span data-stu-id="223e0-124">Draw Direct2D Content to a GDI Device Context</span></span>

<span data-ttu-id="223e0-125">Pour dessiner du contenu Direct2D sur un contrôleur de contexte GDI, vous utilisez un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="223e0-125">To draw Direct2D content to a GDI DC, you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span> <span data-ttu-id="223e0-126">Pour créer une cible de rendu DC, vous utilisez la méthode [**ID2D1Factory :: CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="223e0-126">To create a DC render target, you use the [**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) method.</span></span> <span data-ttu-id="223e0-127">Cette méthode prend deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="223e0-127">This method takes two parameters.</span></span>

<span data-ttu-id="223e0-128">Le premier paramètre, une structure de [**\_ Propriétés de \_ cible \_ de rendu d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , spécifie le rendu, la communication à distance, les PPP, le format de pixel et les informations d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="223e0-128">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure, specifies rendering, remoting, DPI, pixel format, and usage information.</span></span> <span data-ttu-id="223e0-129">Pour permettre à la cible de rendu DC de fonctionner avec GDI, définissez le format DXGI sur [dxgi \_ \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) et le mode Alpha sur d2d1 mode Alpha [**\_ \_ \_ prémultiplié**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ou **d2d1 \_ \_ mode Alpha \_ Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="223e0-129">To enable the DC render target to work with GDI, set the DXGI format to [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) and the alpha mode to [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="223e0-130">Le deuxième paramètre est l’adresse du pointeur qui reçoit la référence de la cible de rendu DC.</span><span class="sxs-lookup"><span data-stu-id="223e0-130">The second parameter is the address of the pointer that receive the DC render target reference.</span></span>

<span data-ttu-id="223e0-131">Le code suivant crée une cible de rendu DC.</span><span class="sxs-lookup"><span data-stu-id="223e0-131">The following code creates a DC render target.</span></span>


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



<span data-ttu-id="223e0-132">Dans le code précédent, *m \_ pD2DFactory* est un pointeur vers [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), et *m \_ pDCRT* est un pointeur vers un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="223e0-132">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pDCRT* is a pointer to an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span>

<span data-ttu-id="223e0-133">Avant de pouvoir effectuer le rendu avec la cible de rendu DC, vous devez utiliser sa méthode [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) pour l’associer à un contrôleur de périphérique (DC) GDI.</span><span class="sxs-lookup"><span data-stu-id="223e0-133">Before you can render with the DC render target, you must use its [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method to associate it with a GDI DC.</span></span> <span data-ttu-id="223e0-134">Vous effectuez cette opération chaque fois que vous utilisez un autre contrôleur de domaine ou la taille de la zone que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="223e0-134">You do this each time you use a different DC, or the size of the area you want to draw to changes.</span></span>

<span data-ttu-id="223e0-135">La méthode [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) prend deux paramètres, *HDC* et *pSubRect*.</span><span class="sxs-lookup"><span data-stu-id="223e0-135">The [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method takes two parameters, *hDC* and *pSubRect*.</span></span> <span data-ttu-id="223e0-136">Le paramètre *HDC* fournit un handle vers le contexte de périphérique qui reçoit la sortie de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="223e0-136">The *hDC* parameter provides a handle to the device context that receives the output of the render target.</span></span> <span data-ttu-id="223e0-137">Le paramètre *pSubRect* est un rectangle qui décrit la partie du contexte de périphérique dans laquelle le contenu est affiché.</span><span class="sxs-lookup"><span data-stu-id="223e0-137">The *pSubRect* parameter is a rectangle that describes the portion of the device context to which content is rendered.</span></span> <span data-ttu-id="223e0-138">La cible de rendu du contrôleur de domaine met à jour sa taille pour correspondre à la zone de contexte de périphérique décrite par *pSubRect*, si elle change de taille.</span><span class="sxs-lookup"><span data-stu-id="223e0-138">The DC render target updates its size to match the device context area described by *pSubRect*, should it change size.</span></span>

<span data-ttu-id="223e0-139">Le code suivant lie un contrôleur de périphérique à une cible de rendu DC.</span><span class="sxs-lookup"><span data-stu-id="223e0-139">The following code binds a DC to a DC render target.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="223e0-140">C++</span><span class="sxs-lookup"><span data-stu-id="223e0-140">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="223e0-141">Une fois que vous avez associé la cible de rendu DC à un contrôleur de périphérique, vous pouvez l’utiliser pour dessiner.</span><span class="sxs-lookup"><span data-stu-id="223e0-141">After you associate the DC render target with a DC, you can use it to draw.</span></span> <span data-ttu-id="223e0-142">Le code suivant dessine le contenu Direct2D et GDI à l’aide d’un contrôleur de périphérique.</span><span class="sxs-lookup"><span data-stu-id="223e0-142">The following code draws Direct2D and GDI content using a DC.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="223e0-143">Ce code produit des sorties comme indiqué dans l’illustration suivante (des légendes ont été ajoutées pour mettre en évidence la différence entre le rendu Direct2D et le rendu GDI.)</span><span class="sxs-lookup"><span data-stu-id="223e0-143">This code produces outputs as shown in the following illustration (callouts have been added to highlight the difference between Direct2D and GDI rendering.)</span></span>

![illustration de deux graphiques circulaires rendus avec Direct2D et GDI](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a><span data-ttu-id="223e0-145">ID2D1DCRenderTargets, les transformations GDI et les versions de langue de droite à gauche de Windows</span><span class="sxs-lookup"><span data-stu-id="223e0-145">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>

<span data-ttu-id="223e0-146">Quand vous utilisez un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), celui-ci affiche le contenu Direct2D dans une image bitmap interne, puis restitue le bitmap dans le DC avec GDI.</span><span class="sxs-lookup"><span data-stu-id="223e0-146">When you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), it renders Direct2D content to an internal bitmap, and then renders the bitmap to the DC with GDI.</span></span>

<span data-ttu-id="223e0-147">GDI peut appliquer une transformation GDI (via la méthode [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) ) ou un autre effet au même contrôleur de service que celui utilisé par la cible de rendu, auquel cas GDI transforme la bitmap produite par Direct2D.</span><span class="sxs-lookup"><span data-stu-id="223e0-147">It's possible for GDI to apply a GDI transform (through the [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) method) or other effect to the same DC used by the render target, in which case GDI transforms the bitmap produced by Direct2D.</span></span> <span data-ttu-id="223e0-148">L’utilisation d’une transformation GDI pour transformer le contenu Direct2D risque de dégrader la qualité visuelle de la sortie, car vous transformez une bitmap pour laquelle l’anticrénelage et le positionnement de sous-pixel ont déjà été calculés.</span><span class="sxs-lookup"><span data-stu-id="223e0-148">Using a GDI transform to transform the Direct2D content has the potential to degrade the visual quality of the output, because you're transforming a bitmap for which antialiasing and subpixel positioning have already been calculated.</span></span>

<span data-ttu-id="223e0-149">Par exemple, supposons que vous utilisez la cible de rendu pour dessiner une scène qui contient des géométries et du texte avec un alias.</span><span class="sxs-lookup"><span data-stu-id="223e0-149">For example, suppose you use the render target to draw a scene that contains antialiased geometries and text.</span></span> <span data-ttu-id="223e0-150">Si vous utilisez une transformation GDI pour appliquer une transformation d’échelle au DC et que vous mettez à l’échelle la scène de manière à ce qu’elle soit 10 fois supérieure, vous verrez des contours et des arêtes en escalier.</span><span class="sxs-lookup"><span data-stu-id="223e0-150">If you use a GDI transform to apply a scale transform to the DC and scale the scene so that it's 10 times larger, you'll see pixelization and jagged edges.</span></span> <span data-ttu-id="223e0-151">(Si, toutefois, vous avez appliqué une transformation similaire à l’aide de Direct2D, la qualité visuelle de la scène n’est pas dégradée.)</span><span class="sxs-lookup"><span data-stu-id="223e0-151">(If, however, you applied a similar transform using Direct2D, the visual quality of the scene would not be degraded.)</span></span>

<span data-ttu-id="223e0-152">Dans certains cas, il peut ne pas être évident que GDI effectue un traitement supplémentaire qui peut dégrader la qualité du contenu Direct2D.</span><span class="sxs-lookup"><span data-stu-id="223e0-152">In some cases, it might not be obvious that GDI is performing additional processing that might degrade the quality of the Direct2D content.</span></span> <span data-ttu-id="223e0-153">Par exemple, sur une version de Windows de droite à gauche (RTL), le contenu rendu par un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) peut être inversé horizontalement lorsque GDI le copie à son emplacement de destination.</span><span class="sxs-lookup"><span data-stu-id="223e0-153">For example, on a right-to-left (RTL) build of Windows, content rendered by an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) might be horizontally inverted when GDI copies it to its destination.</span></span> <span data-ttu-id="223e0-154">Le fait que le contenu soit inversé dépend des paramètres actuels du contrôleur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="223e0-154">Whether the content is actually inverted depends on the current settings of the DC.</span></span>

<span data-ttu-id="223e0-155">Selon le type de contenu rendu, vous pouvez empêcher l’inversion.</span><span class="sxs-lookup"><span data-stu-id="223e0-155">Depending on the type of content being rendered, you might want to prevent the inversion.</span></span> <span data-ttu-id="223e0-156">Si le contenu Direct2D comprend du texte ClearType, cette inversion dégradera la qualité du texte.</span><span class="sxs-lookup"><span data-stu-id="223e0-156">If the Direct2D content includes ClearType text, this inversion will degrade the quality of the text.</span></span>

<span data-ttu-id="223e0-157">Vous pouvez contrôler le comportement de rendu RTL à l’aide de la fonction GDI [**setLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) .</span><span class="sxs-lookup"><span data-stu-id="223e0-157">You can control RTL rendering behavior by using the [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI function.</span></span> <span data-ttu-id="223e0-158">Pour empêcher la mise en miroir, appelez la fonction de la fonction GDI **setLayout** et spécifiez **Layout \_ BITMAPORIENTATIONPRESERVED** comme seule valeur pour le deuxième paramètre (ne l’associez pas à la **disposition \_ RTL**), comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="223e0-158">To prevent the mirroring, call the **SetLayout** GDI function and specify **LAYOUT\_BITMAPORIENTATIONPRESERVED** as the only value for the second parameter (do not combine it with **LAYOUT\_RTL**), as shown in the following example:</span></span>


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a><span data-ttu-id="223e0-159">Dessiner du contenu GDI sur une cible de rendu Direct2D GDI-Compatible</span><span class="sxs-lookup"><span data-stu-id="223e0-159">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>

<span data-ttu-id="223e0-160">La section précédente décrit comment écrire du contenu Direct2D sur un contrôleur de périphérique (DC) GDI.</span><span class="sxs-lookup"><span data-stu-id="223e0-160">The previous section describes how to write Direct2D content to a GDI DC.</span></span> <span data-ttu-id="223e0-161">Vous pouvez également écrire du contenu GDI dans une cible de rendu compatible GDI Direct2D.</span><span class="sxs-lookup"><span data-stu-id="223e0-161">You can also write GDI content to a Direct2D GDI-compatible render target.</span></span> <span data-ttu-id="223e0-162">Cette approche est utile pour les applications qui s’affichent principalement avec Direct2D, mais qui ont un modèle d’extensibilité ou tout autre contenu hérité qui requiert la possibilité d’effectuer un rendu avec GDI.</span><span class="sxs-lookup"><span data-stu-id="223e0-162">This approach is useful for applications that primarily render with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span>

<span data-ttu-id="223e0-163">Pour afficher le contenu GDI sur une cible de rendu de Direct2D compatible GDI, utilisez un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), qui fournit l’accès à un contexte de périphérique qui peut accepter des appels de dessin GDI.</span><span class="sxs-lookup"><span data-stu-id="223e0-163">To render GDI content to a Direct2D GDI-compatible render target, use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which provides access to a device context that can accept GDI draw calls.</span></span> <span data-ttu-id="223e0-164">Contrairement à d’autres interfaces, un objet **ID2D1GdiInteropRenderTarget** n’est pas créé directement.</span><span class="sxs-lookup"><span data-stu-id="223e0-164">Unlike other interfaces, an **ID2D1GdiInteropRenderTarget** object is not created directly.</span></span> <span data-ttu-id="223e0-165">Utilisez plutôt la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) d’une instance de cible de rendu existante.</span><span class="sxs-lookup"><span data-stu-id="223e0-165">Instead, use the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of an existing render target instance.</span></span> <span data-ttu-id="223e0-166">Le code suivant illustre comment procéder :</span><span class="sxs-lookup"><span data-stu-id="223e0-166">The following code shows how to do this:</span></span>


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



<span data-ttu-id="223e0-167">Dans le code précédent, *m \_ pD2DFactory* est un pointeur vers [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), et *m \_ pGDIRT* est un pointeur vers un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span><span class="sxs-lookup"><span data-stu-id="223e0-167">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pGDIRT* is a pointer to an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span></span>

<span data-ttu-id="223e0-168">Notez que l’indicateur de [**\_ \_ \_ \_ \_ compatibilité GDI**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) de l’utilisation de la cible de rendu d2d1 est spécifié lors de la création de la cible de rendu compatible avec GDI HWND.</span><span class="sxs-lookup"><span data-stu-id="223e0-168">Notice that the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag is specified when creating the Hwnd GDI-compatible render target.</span></span> <span data-ttu-id="223e0-169">Si un format de pixel est requis, utilisez le [ \_ format dxgi \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="223e0-169">If a pixel format is required, use [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="223e0-170">Si vous avez besoin d’un mode alpha, utilisez l’option [**d2d1 \_ alpha mode \_ \_ Premultiplied**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ou **d2d1 \_ alpha \_ mode \_ ignore**.</span><span class="sxs-lookup"><span data-stu-id="223e0-170">If an alpha mode is required, use [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="223e0-171">Notez que la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) fonctionne toujours.</span><span class="sxs-lookup"><span data-stu-id="223e0-171">Note that the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method always succeeds.</span></span> <span data-ttu-id="223e0-172">Pour tester si les méthodes de l’interface [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) fonctionnent pour une cible de rendu donnée, créez un [**d2d1 propriétés de la \_ \_ cible \_ de rendu**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) qui spécifie la compatibilité GDI et le format de pixel approprié, puis appelez la méthode [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) de la cible de rendu pour voir si la cible de rendu est compatible GDI.</span><span class="sxs-lookup"><span data-stu-id="223e0-172">To test whether the [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) interface's methods will work for a given render target, create a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) that specifies GDI compatibility and the appropriate pixel format, and then call the render target's [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) method to see whether the render target is GDI-compatible.</span></span>

<span data-ttu-id="223e0-173">L’exemple suivant montre comment dessiner un graphique à secteurs (contenu GDI) vers la cible de rendu compatible avec la GDI HWND.</span><span class="sxs-lookup"><span data-stu-id="223e0-173">The following example shows how to draw a pie chart (GDI content) to the Hwnd GDI-compatible render target.</span></span>


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



<span data-ttu-id="223e0-174">Le code génère des graphiques comme indiqué dans l’illustration suivante avec des légendes pour mettre en évidence la différence de qualité de rendu.</span><span class="sxs-lookup"><span data-stu-id="223e0-174">The code outputs charts as shown in the following illustration with callouts to highlight the rendering quality difference.</span></span> <span data-ttu-id="223e0-175">Le graphique à secteurs droit (contenu GDI) a une qualité de rendu inférieure à celle du graphique à secteurs gauche (contenu Direct2D).</span><span class="sxs-lookup"><span data-stu-id="223e0-175">The right pie chart (GDI content) has lower rendering quality than the left pie chart (Direct2D content).</span></span> <span data-ttu-id="223e0-176">Cela est dû au fait que Direct2D est apte à effectuer le rendu avec l’anticrénelage</span><span class="sxs-lookup"><span data-stu-id="223e0-176">This is because Direct2D is capable of rendering with antialiasing</span></span>

![illustration de deux graphiques circulaires rendus dans une cible de rendu de Direct2D compatible GDI](images/gdicontentind2d.png)

## <a name="related-topics"></a><span data-ttu-id="223e0-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="223e0-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="223e0-179">**ID2D1Factory::CreateDCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="223e0-179">**ID2D1Factory::CreateDCRenderTarget**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[<span data-ttu-id="223e0-180">**ID2D1DCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="223e0-180">**ID2D1DCRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[<span data-ttu-id="223e0-181">**ID2D1GdiInteropRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="223e0-181">**ID2D1GdiInteropRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[<span data-ttu-id="223e0-182">**Propriétés de la \_ cible de rendu d2d1 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="223e0-182">**D2D1\_RENDER\_TARGET\_PROPERTIES**</span></span>](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[<span data-ttu-id="223e0-183">Contextes de périphérique GDI</span><span class="sxs-lookup"><span data-stu-id="223e0-183">GDI Device Contexts</span></span>](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[<span data-ttu-id="223e0-184">SDK GDI</span><span class="sxs-lookup"><span data-stu-id="223e0-184">GDI SDK</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 