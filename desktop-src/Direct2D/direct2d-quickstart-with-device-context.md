---
title: Démarrage rapide de Direct2D pour Windows 8
description: résume les étapes requises pour dessiner avec Direct2D pour Windows 8 et fournit un exemple de code. Direct2D est une API de code natif pour la création de graphiques 2D.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, exemple de code de rectangle de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43442e57ed0949bdf39fc05ce1a69fded42b4b3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113305"
---
# <a name="direct2d-quickstart-for-windows-8"></a>Démarrage rapide de Direct2D pour Windows 8

Direct2D est une API en mode immédiat et en code natif pour la création de graphiques 2D. cette rubrique montre comment utiliser Direct2D pour dessiner sur un [**Windows :: UI :: Core :: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

Cette rubrique contient les sections suivantes :

-   [Dessin d’un rectangle simple](#drawing-a-simple-rectangle)
-   [Étape 1 : inclure l’en-tête Direct2D](#step-1-include-direct2d-header)
-   [Étape 2 : créer un ID2D1Factory1](#step-2-create-an-id2d1factory1)
-   [Étape 3 : créer un ID2D1Device et un ID2D1DeviceContext](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [Étape 4 : créer un pinceau](#step-4-create-a-brush)
-   [Étape 5 : dessiner le rectangle](#step-5-draw-the-rectangle)
-   [Exemple de code](#example-code)

## <a name="drawing-a-simple-rectangle"></a>Dessin d’un rectangle simple

Pour dessiner un rectangle à l’aide de [GDI](/windows/desktop/gdi/windows-gdi), vous pouvez gérer le message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , comme indiqué dans le code suivant.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



Le code permettant de dessiner le même rectangle avec Direct2D est similaire : il crée des ressources de dessin, décrit une forme à dessiner, dessine la forme, puis libère les ressources de dessin. Les sections qui suivent décrivent chacune de ces étapes en détail.

## <a name="step-1-include-direct2d-header"></a>Étape 1 : inclure l’en-tête Direct2D

En plus des en-têtes requis pour l’application, incluez les en-têtes d2d1. h et d2d1 \_ 1. h.

## <a name="step-2-create-an-id2d1factory1"></a>Étape 2 : créer un ID2D1Factory1

L’un des premiers éléments d’un exemple Direct2D est la création d’un [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



L’interface [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) est le point de départ pour l’utilisation de Direct2D ; Utilisez un **ID2D1Factory1** pour créer des ressources Direct2D.

Lorsque vous créez une fabrique, vous pouvez spécifier s’il s’agit d’un thread multiple ou d’un thread unique. (Pour plus d’informations sur les fabriques multithread, consultez les notes sur la [**page de référence ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) Cet exemple crée une fabrique à thread unique.

En général, votre application doit créer la fabrique une seule fois et la conserver pendant toute la durée de vie de l’application.

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a>Étape 3 : créer un ID2D1Device et un ID2D1DeviceContext

Après avoir créé une fabrique, utilisez-la pour créer un appareil Direct2D, puis utilisez l’appareil pour créer un contexte de périphérique Direct2D. Pour créer ces objets Direct2D, vous devez disposer d’un [**appareil Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , d’un [**appareil dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)et d’une [**chaîne de permutation dxgi**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1). Pour plus d’informations sur la création des composants requis [, consultez contextes de périphériques et](devices-and-device-contexts.md) de périphériques.


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Un contexte de périphérique est un appareil qui peut effectuer des opérations de dessin et créer des ressources de dessin dépendant de l’appareil, telles que des pinceaux. Vous utilisez également le contexte de périphérique pour lier un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à une surface DXGI à utiliser comme cible de rendu. Le contexte de périphérique peut être rendu sur différents types de cibles.

Le code ci-dessous déclare les propriétés de la bitmap qui établit un lien vers une chaîne de permutation DXGI qui est restituée à un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow). La méthode [**ID2D1DeviceContext :: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) obtient une surface Direct2D à partir de la surface DXGI. Ainsi, toute donnée rendue au [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) cible est rendue à la surface de la chaîne de permutation.

Une fois que vous avez la surface Direct2D, utilisez la méthode [**ID2D1DeviceContext :: SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) pour la définir en tant que cible de rendu active.


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a>Étape 4 : créer un pinceau

À l’instar d’une fabrique, un contexte de périphérique peut créer des ressources de dessin. Dans cet exemple, le contexte de périphérique crée un pinceau.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



Un pinceau est un objet qui peint une zone, telle que le trait d’une forme ou le remplissage d’une géométrie. Dans cet exemple, le pinceau peint une zone avec une couleur unie prédéfinie, noire.

Direct2D fournit également d’autres types de pinceaux : les pinceaux de dégradé pour peindre des dégradés linéaires et radiaux, un [**pinceau bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pour peindre avec des bitmaps et des modèles, et à partir de Windows 8, un [**pinceau d’image**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) pour peindre avec une image rendue.

Certaines API de dessin fournissent des stylets pour dessiner des contours et des pinceaux pour remplir des formes. Direct2D est différent : il ne fournit pas d’objet Pen, mais utilise un pinceau pour dessiner des contours et des formes de remplissage. lors du dessin de contours, utilisez l’interface [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) , ou à partir de Windows 8 l’interface [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) , avec un pinceau pour contrôler les opérations de traçage de chemin.

Un pinceau peut uniquement être utilisé avec la cible de rendu qui l’a créé et avec d’autres cibles de rendu dans le même domaine de ressource. En général, vous devez créer des pinceaux une seule fois et les conserver pendant toute la durée de vie de la cible de rendu qui les a créés. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) est l’exception solitaire ; étant donné qu’il est relativement peu coûteux à créer, vous pouvez créer un **ID2D1SolidColorBrush** chaque fois que vous dessinez un cadre, sans toucher aux performances perceptibles. Vous pouvez également utiliser un seul **ID2D1SolidColorBrush** et modifier sa couleur ou son opacité chaque fois que vous l’utilisez.

## <a name="step-5-draw-the-rectangle"></a>Étape 5 : dessiner le rectangle

Ensuite, utilisez le contexte de périphérique pour dessiner le rectangle.


```C++
 
m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



La méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) accepte deux paramètres : le rectangle à dessiner et le pinceau à utiliser pour peindre le contour du rectangle. Si vous le souhaitez, vous pouvez également spécifier les options largeur du trait, motif des tirets, jointure de ligne et extrémité de fin.

Vous devez appeler la méthode [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) avant d’émettre des commandes de dessin, et vous devez appeler la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) une fois que vous avez terminé d’émettre des commandes de dessin. La méthode **EndDraw** retourne un **HRESULT** qui indique si les commandes de dessin ont réussi. Si elle échoue, la fonction d’assistance ThrowIfFailed lèvera une exception.

La méthode [**IDXGISwapChain ::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) replaced permute la surface de la mémoire tampon avec la surface de l’écran pour afficher le résultat.

## <a name="example-code"></a>Exemple de code

Le code de cette rubrique montre les éléments de base d’une application Direct2D. Par souci de concision, la rubrique omet l’infrastructure d’application et le code de gestion des erreurs qui est caractéristique d’une application bien écrite.

 

 