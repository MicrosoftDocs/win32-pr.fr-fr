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
# <a name="direct2d-and-gdi-interoperability-overview"></a>Vue d’ensemble de l’interopérabilité de Direct2D et GDI

Cette rubrique explique comment utiliser Direct2D et [GDI](/windows/desktop/gdi/windows-gdi) ensemble. Il existe deux façons de combiner Direct2D avec GDI : vous pouvez écrire du contenu GDI dans une cible de rendu compatible avec GDI Direct2D, ou vous pouvez écrire du contenu Direct2D dans un [contexte de périphérique (DC) GDI](/windows/desktop/gdi/device-contexts).

Cette rubrique contient les sections suivantes.

-   [Conditions préalables](#prerequisites)
-   [Dessiner du contenu Direct2D dans un contexte de périphérique GDI](#draw-direct2d-content-to-a-gdi-device-context)
-   [ID2D1DCRenderTargets, les transformations GDI et les versions de langue de droite à gauche de Windows](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [Dessiner du contenu GDI sur une cible de rendu Direct2D GDI-Compatible](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Cette vue d’ensemble suppose que vous êtes familiarisé avec les opérations de dessin Direct2D de base. Pour obtenir un didacticiel, consultez le Guide de [démarrage rapide de Direct2D](direct2d-quickstart.md). Elle suppose également que vous êtes familiarisé avec les opérations de dessin GDI.

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a>Dessiner du contenu Direct2D dans un contexte de périphérique GDI

Pour dessiner du contenu Direct2D sur un contrôleur de contexte GDI, vous utilisez un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). Pour créer une cible de rendu DC, vous utilisez la méthode [**ID2D1Factory :: CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) . Cette méthode prend deux paramètres.

Le premier paramètre, une structure de [**\_ Propriétés de \_ cible \_ de rendu d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , spécifie le rendu, la communication à distance, les PPP, le format de pixel et les informations d’utilisation. Pour permettre à la cible de rendu DC de fonctionner avec GDI, définissez le format DXGI sur [dxgi \_ \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) et le mode Alpha sur d2d1 mode Alpha [**\_ \_ \_ prémultiplié**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ou **d2d1 \_ \_ mode Alpha \_ Ignorer**.

Le deuxième paramètre est l’adresse du pointeur qui reçoit la référence de la cible de rendu DC.

Le code suivant crée une cible de rendu DC.


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



Dans le code précédent, *m \_ pD2DFactory* est un pointeur vers [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), et *m \_ pDCRT* est un pointeur vers un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).

Avant de pouvoir effectuer le rendu avec la cible de rendu DC, vous devez utiliser sa méthode [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) pour l’associer à un contrôleur de périphérique (DC) GDI. Vous effectuez cette opération chaque fois que vous utilisez un autre contrôleur de domaine ou la taille de la zone que vous souhaitez modifier.

La méthode [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) prend deux paramètres, *HDC* et *pSubRect*. Le paramètre *HDC* fournit un handle vers le contexte de périphérique qui reçoit la sortie de la cible de rendu. Le paramètre *pSubRect* est un rectangle qui décrit la partie du contexte de périphérique dans laquelle le contenu est affiché. La cible de rendu du contrôleur de domaine met à jour sa taille pour correspondre à la zone de contexte de périphérique décrite par *pSubRect*, si elle change de taille.

Le code suivant lie un contrôleur de périphérique à une cible de rendu DC.


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
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



Une fois que vous avez associé la cible de rendu DC à un contrôleur de périphérique, vous pouvez l’utiliser pour dessiner. Le code suivant dessine le contenu Direct2D et GDI à l’aide d’un contrôleur de périphérique.


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



Ce code produit des sorties comme indiqué dans l’illustration suivante (des légendes ont été ajoutées pour mettre en évidence la différence entre le rendu Direct2D et le rendu GDI.)

![illustration de deux graphiques circulaires rendus avec Direct2D et GDI](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a>ID2D1DCRenderTargets, les transformations GDI et les versions de langue de droite à gauche de Windows

Quand vous utilisez un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), celui-ci affiche le contenu Direct2D dans une image bitmap interne, puis restitue le bitmap dans le DC avec GDI.

GDI peut appliquer une transformation GDI (via la méthode [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) ) ou un autre effet au même contrôleur de service que celui utilisé par la cible de rendu, auquel cas GDI transforme la bitmap produite par Direct2D. L’utilisation d’une transformation GDI pour transformer le contenu Direct2D risque de dégrader la qualité visuelle de la sortie, car vous transformez une bitmap pour laquelle l’anticrénelage et le positionnement de sous-pixel ont déjà été calculés.

Par exemple, supposons que vous utilisez la cible de rendu pour dessiner une scène qui contient des géométries et du texte avec un alias. Si vous utilisez une transformation GDI pour appliquer une transformation d’échelle au DC et que vous mettez à l’échelle la scène de manière à ce qu’elle soit 10 fois supérieure, vous verrez des contours et des arêtes en escalier. (Si, toutefois, vous avez appliqué une transformation similaire à l’aide de Direct2D, la qualité visuelle de la scène n’est pas dégradée.)

Dans certains cas, il peut ne pas être évident que GDI effectue un traitement supplémentaire qui peut dégrader la qualité du contenu Direct2D. Par exemple, sur une version de Windows de droite à gauche (RTL), le contenu rendu par un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) peut être inversé horizontalement lorsque GDI le copie à son emplacement de destination. Le fait que le contenu soit inversé dépend des paramètres actuels du contrôleur de l’objet.

Selon le type de contenu rendu, vous pouvez empêcher l’inversion. Si le contenu Direct2D comprend du texte ClearType, cette inversion dégradera la qualité du texte.

Vous pouvez contrôler le comportement de rendu RTL à l’aide de la fonction GDI [**setLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) . Pour empêcher la mise en miroir, appelez la fonction de la fonction GDI **setLayout** et spécifiez **Layout \_ BITMAPORIENTATIONPRESERVED** comme seule valeur pour le deuxième paramètre (ne l’associez pas à la **disposition \_ RTL**), comme illustré dans l’exemple suivant :


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a>Dessiner du contenu GDI sur une cible de rendu Direct2D GDI-Compatible

La section précédente décrit comment écrire du contenu Direct2D sur un contrôleur de périphérique (DC) GDI. Vous pouvez également écrire du contenu GDI dans une cible de rendu compatible GDI Direct2D. Cette approche est utile pour les applications qui s’affichent principalement avec Direct2D, mais qui ont un modèle d’extensibilité ou tout autre contenu hérité qui requiert la possibilité d’effectuer un rendu avec GDI.

Pour afficher le contenu GDI sur une cible de rendu de Direct2D compatible GDI, utilisez un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), qui fournit l’accès à un contexte de périphérique qui peut accepter des appels de dessin GDI. Contrairement à d’autres interfaces, un objet **ID2D1GdiInteropRenderTarget** n’est pas créé directement. Utilisez plutôt la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) d’une instance de cible de rendu existante. Le code suivant illustre comment procéder :


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



Dans le code précédent, *m \_ pD2DFactory* est un pointeur vers [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), et *m \_ pGDIRT* est un pointeur vers un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).

Notez que l’indicateur de [**\_ \_ \_ \_ \_ compatibilité GDI**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) de l’utilisation de la cible de rendu d2d1 est spécifié lors de la création de la cible de rendu compatible avec GDI HWND. Si un format de pixel est requis, utilisez le [ \_ format dxgi \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Si vous avez besoin d’un mode alpha, utilisez l’option [**d2d1 \_ alpha mode \_ \_ Premultiplied**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ou **d2d1 \_ alpha \_ mode \_ ignore**.

Notez que la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) fonctionne toujours. Pour tester si les méthodes de l’interface [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) fonctionnent pour une cible de rendu donnée, créez un [**d2d1 propriétés de la \_ \_ cible \_ de rendu**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) qui spécifie la compatibilité GDI et le format de pixel approprié, puis appelez la méthode [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) de la cible de rendu pour voir si la cible de rendu est compatible GDI.

L’exemple suivant montre comment dessiner un graphique à secteurs (contenu GDI) vers la cible de rendu compatible avec la GDI HWND.


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



Le code génère des graphiques comme indiqué dans l’illustration suivante avec des légendes pour mettre en évidence la différence de qualité de rendu. Le graphique à secteurs droit (contenu GDI) a une qualité de rendu inférieure à celle du graphique à secteurs gauche (contenu Direct2D). Cela est dû au fait que Direct2D est apte à effectuer le rendu avec l’anticrénelage

![illustration de deux graphiques circulaires rendus dans une cible de rendu de Direct2D compatible GDI](images/gdicontentind2d.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[**Propriétés de la \_ cible de rendu d2d1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[Contextes de périphérique GDI](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[SDK GDI](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 