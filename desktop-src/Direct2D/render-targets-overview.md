---
title: Vue d’ensemble des cibles de rendu
description: Décrit les différents types de cibles de rendu Direct2D et comment les utiliser.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, cibles de rendu
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112561"
---
# <a name="render-targets-overview"></a>Vue d’ensemble des cibles de rendu

Une cible de rendu est une ressource qui hérite de l’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Une cible de rendu crée des ressources pour dessiner et effectue des opérations de dessin réelles. Cette rubrique décrit les différents types de cibles de rendu Direct2D et comment les utiliser.

-   [Cibles de rendu](#render-targets-overview)
    -   [Fonctionnalités de la cible de rendu](#render-target-features)
    -   [Afficher les ressources cibles](#render-target-resources)
    -   [Commandes de dessin](#drawing-commands)
    -   [Gestion des erreurs](#error-handling)
-   [Exemple : afficher le contenu dans une fenêtre](#example-render-content-to-a-window)

## <a name="render-targets"></a>Cibles de rendu

Une cible de rendu est une ressource qui hérite de l’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Une cible de rendu crée des ressources pour dessiner et effectue des opérations de dessin réelles. Il existe plusieurs types de cibles de rendu qui peuvent être utilisées pour restituer des graphiques des manières suivantes :

-   Les objets [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) affichent le contenu dans une fenêtre.
-   Les objets [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) sont rendus dans un contexte de périphérique GDI.
-   Les objets cibles de rendu bitmap affichent le contenu dans une image bitmap hors écran.
-   Les objets cibles de rendu DXGI sont rendus sur une surface DXGI pour une utilisation avec Direct3D.

Étant donné qu’une cible de rendu est associée à un appareil de rendu particulier, il s’agit d’une ressource dépendante de l’appareil qui cesse de fonctionner si l’appareil est supprimé.

### <a name="render-target-features"></a>Fonctionnalités de la cible de rendu

Vous pouvez spécifier si une cible de rendu utilise l’accélération matérielle et si l’affichage à distance est rendu par un ordinateur local ou distant. Les cibles de rendu peuvent être configurées pour le rendu avec ou sans alias. Pour le rendu des scènes avec un grand nombre de primitives, un développeur peut également restituer des graphiques 2D en mode alias et utiliser l’anticrénelage à plusieurs échantillons D3D pour obtenir une plus grande évolutivité.

Les cibles de rendu peuvent également regrouper des opérations de dessin dans des couches représentées par l’interface [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) . Les couches sont utiles pour la collecte des opérations de dessin à combiner lors du rendu d’un frame. Pour certains scénarios, il peut s’agir d’une alternative utile au rendu d’une cible de rendu bitmap, puis de la réutilisation du contenu de l’image bitmap, car les coûts d’allocation pour la superposition sont inférieurs à ceux d’un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Les cibles de rendu peuvent créer de nouvelles cibles de rendu qui sont compatibles avec elles-mêmes, ce qui est utile pour le rendu non-écran intermédiaire tout en conservant les diverses propriétés de cible de rendu qui ont été définies sur le d’origine.

Il est également possible d’effectuer un rendu à l’aide de GDI sur une cible de rendu Direct2D en appelant [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur une cible de rendu pour [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), qui contient des méthodes [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) et [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) qui peuvent être utilisées pour récupérer un contexte de périphérique GDI. Le rendu via GDI est possible uniquement si la cible de rendu a été créée avec l’indicateur de [**\_ \_ \_ \_ \_ compatibilité GDI**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) de l’utilisation de la cible de rendu d2d1 définie. Cela est utile pour les applications qui sont principalement rendues avec Direct2D, mais qui ont un modèle d’extensibilité ou tout autre contenu hérité qui requiert la possibilité d’effectuer un rendu avec GDI. Pour plus d’informations, consultez [vue d’ensemble de l’interopérabilité Direct2D et GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Afficher les ressources cibles

À l’instar d’une fabrique, une cible de rendu peut créer des ressources de dessin. Toutes les ressources créées par une cible de rendu sont des ressources dépendantes de l’appareil (tout comme la cible de rendu). Une cible de rendu peut créer les types de ressources suivants :

-   Images bitmap
-   Pinceaux
-   Calques
-   Maillages

### <a name="drawing-commands"></a>Commandes de dessin

Pour afficher le contenu, vous utilisez les méthodes de dessin de la cible de rendu. Avant de commencer à dessiner, vous appelez la méthode [**ID2D1RenderTarget :: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Une fois que vous avez terminé le dessin, vous appelez la méthode [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Entre ces appels, vous utilisez des méthodes de dessin et de remplissage pour restituer les ressources de dessin. La plupart des méthodes de dessin et de remplissage prennent une forme (une primitive ou une géométrie) et un pinceau pour remplir ou mettre en relief la forme.

Les cibles de rendu fournissent des méthodes pour le découpage, l’application de masques d’opacité et la transformation de l’espace de coordonnées.

Direct2D utilise un système de coordonnées gauche : les valeurs positives de l’axe des x continuent à droite et les valeurs positives de l’axe des y s’effectuent vers le bas.

### <a name="error-handling"></a>Gestion des erreurs

Les commandes de dessin de la cible de rendu n’indiquent pas si l’opération demandée a réussi. Pour déterminer s’il existe des erreurs de dessin, appelez la méthode de [**vidage**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) de la cible de rendu ou la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) pour obtenir un **HRESULT**.

## <a name="example-render-content-to-a-window"></a>Exemple : afficher le contenu dans une fenêtre

L’exemple suivant utilise la méthode [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) pour créer un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



L’exemple suivant utilise le [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pour dessiner du texte dans la fenêtre.


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
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



Le code a été omis de cet exemple.

 

 