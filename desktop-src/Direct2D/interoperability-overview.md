---
title: Vue d'ensemble de l'interopérabilité
description: Résume les différentes technologies que vous pouvez utiliser avec Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, interopérabilité GDI
- Direct2D, GDI+ interopération
- Direct2D, interopérabilité
- Direct2D, DirectWrite interopération
- interopérabilité, Direct2D
- interopérabilité, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interopérabilité, Graphics Device Interface (GDI)
- interopérabilité, GDI+
- interopérabilité DirectWrite
- interopérabilité, DirectWrite
- Composant Imagerie Windows (WIC)
- WIC (composant de création d’images Windows)
- interopérabilité, Windows composant d’imagerie (WIC)
- Direct2D, interopérabilité WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112677"
---
# <a name="interoperability-overview"></a>Vue d'ensemble de l'interopérabilité

L’une des fonctionnalités clés de Direct2d est l’activation de l’interopérabilité entre Direct2D et d’autres plateformes de rendu afin que les développeurs puissent utiliser les points forts spécifiques de chaque plateforme sans être forcés à compromettre en choisissant une plate-forme pour tous les besoins. Cette rubrique résume les différentes plateformes avec lesquelles Direct2D est interopérable. Elle contient les sections suivantes.

-   [Interopérabilité GDI](#gdi-interoperability)
-   [GDI+ Interopérabilité](#gdi-interoperability)
-   [Interopérabilité Direct3D](#direct3d-interoperability)
-   [DirectWrite Interopérabilité](#directwrite-interoperability)
-   [Windows Interopérabilité du composant de création d’images (WIC)](#windows-imaging-component-wic-interoperability)
-   [Rubriques connexes](#related-topics)

Le diagramme suivant résume les différentes plateformes avec lesquelles Direct2D est interopérable et répertorie des méthodes et des interfaces qui fournissent une interopérabilité.

![diagramme des plateformes avec lesquelles Direct2D interagit, y compris Direct3D 10,1, DirectWrite, WIC, GDI+ et GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>Interopérabilité GDI

Direct2D active l’interopérabilité bidirectionnelle avec GDI. Vous pouvez utiliser un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) pour écrire du contenu Direct2D dans un [contexte de périphérique](/windows/desktop/gdi/device-contexts) (DC) GDI, ou vous pouvez utiliser [**ID2D1GDIINTEROPRENDERTARGET**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) pour obtenir une représentation DC d’une cible de rendu.

Pour plus d’informations et d’exemples, consultez [vue d’ensemble de l’interopérabilité de Direct2D et GDI](direct2d-and-gdi-interoperation-overview.md).

## <a name="gdi-interoperability"></a>GDI+ Interopérabilité

vous pouvez utiliser GDI+ avec Direct2D de la même manière que GDI. vous pouvez utiliser un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) pour écrire du contenu Direct2D sur le même contrôleur de périphérique que votre contenu GDI+. Cette approche vous permet de commencer à ajouter du contenu Direct2D aux applications qui sont principalement rendues à l’aide de GDI+.

Vous pouvez également utiliser un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) pour fournir l’accès à un contrôleur de contexte GDI qui écrit à l’aide de Direct2D, puis utiliser la méthode [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) pour créer un objet. Cette approche est utile pour les applications qui s’affichent principalement avec Direct2D, mais qui ont un modèle d’extensibilité ou tout autre contenu hérité qui requiert la possibilité d’effectuer un rendu avec GDI+.

## <a name="direct3d-interoperability"></a>Interopérabilité Direct3D

Direct2D peut utiliser une cible de rendu de surface DXGI (créée par la méthode [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) pour écrire dans un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface). Cette action vous permet d’ajouter des interfaces et des arrière-plans 2D à des scènes 3D et d’utiliser le contenu Direct2D comme texture pour un modèle 3D. Direct2D peut également prendre un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) et utiliser la méthode [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) pour créer une représentation bitmap.

Pour plus d’informations et d’exemples, consultez [vue d’ensemble de l’interopérabilité de Direct2D et Direct3D](direct2d-and-direct3d-interoperation-overview.md).

## <a name="directwrite-interoperability"></a>DirectWrite Interopérabilité

Direct2D est étroitement intégré à DirectWrite. Direct2D facilite le rendu du contenu DirectWrite en fournissant les méthodes [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)et [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .

## <a name="windows-imaging-component-wic-interoperability"></a>Windows Interopérabilité du composant de création d’images (WIC)

Direct2D fournit les méthodes [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)et [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) pour manipuler les bitmaps WIC.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de l’interopérabilité de Direct2D et GDI](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Vue d’ensemble de l’interopérabilité entre Direct2D et Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 