---
title: Utilisation de Direct2D pour le rendu Server-Side
description: Décrit l’utilisation de Direct2D pour le rendu côté serveur.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, rendu côté serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382077"
---
# <a name="using-direct2d-for-server-side-rendering"></a>Utilisation de Direct2D pour le rendu Server-Side

Direct2D est bien adapté aux applications graphiques qui requièrent un rendu côté serveur sur Windows Server. Cette vue d’ensemble décrit les principes fondamentaux de l’utilisation de Direct2D pour le rendu côté serveur. Il contient les sections suivantes :

-   [Conditions requises pour le rendu Server-Side](#requirements-for-server-side-rendering)
-   [Options pour les API disponibles](#options-for-available-apis)
    -   [GDI](#gdi)
    -   [GDI+](#gdi)
    -   [Direct2D](#using-direct2d-for-server-side-rendering)
-   [Utilisation de Direct2D pour le rendu Server-Side](#how-to-use-direct2d-for-server-side-rendering)
    -   [Rendu logiciel](#software-rendering)
    -   [Traitement multithread](#multithreading)
    -   [Génération d’un fichier bitmap](#generating-a-bitmap-file)
-   [Conclusion](#conclusion)
-   [Rubriques connexes](#related-topics)

## <a name="requirements-for-server-side-rendering"></a>Conditions requises pour le rendu Server-Side

Voici un scénario classique pour un serveur de graphique : les graphiques et les graphiques sont rendus sur un serveur et remis en tant que bitmaps en réponse aux requêtes Web. Le serveur peut être équipé d’une carte graphique de bas niveau ou d’aucune carte graphique.

Ce scénario révèle trois exigences en matière d’applications. Tout d’abord, l’application doit gérer efficacement plusieurs requêtes simultanées, en particulier sur les serveurs multicœurs. Deuxièmement, l’application doit utiliser le rendu logiciel lors de l’exécution sur des serveurs avec une carte graphique de bas niveau ou aucune carte graphique. Enfin, l’application doit s’exécuter en tant que service dans la session 0 afin qu’il ne soit pas nécessaire qu’un utilisateur soit connecté. Pour plus d’informations sur la session 0, consultez [impact de l’isolation de la session 0 sur les services et les pilotes dans Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).

## <a name="options-for-available-apis"></a>Options pour les API disponibles

Il existe trois options pour le rendu côté serveur : GDI, GDI+ et Direct2D. À l’instar de GDI et GDI+, Direct2D est une API de rendu 2D native qui permet aux applications de mieux contrôler l’utilisation des périphériques graphiques. En outre, Direct2D prend en charge de façon unique une fabrique à thread unique et une fabrique multithread. Les sections suivantes comparent chaque API en termes de qualité de dessin et de rendu multithread côté serveur.

### <a name="gdi"></a>GDI

Contrairement à Direct2D et GDI+, GDI ne prend pas en charge les fonctionnalités de dessin de haute qualité. Par exemple, GDI ne prend pas en charge l’anticrénelage pour créer des courbes lissées et n’a qu’une prise en charge limitée de la transparence. En fonction des résultats des tests de performances graphiques sur Windows 7 et Windows Server 2008 R2, la mise à l’échelle de Direct2D est plus efficace que GDI, malgré la reconception des verrous dans GDI. Pour plus d’informations sur ces résultats de tests, consultez [ingénierie des performances graphiques de Windows 7](/archive/blogs/e7/engineering-windows-7-graphics-performance).

En outre, les applications utilisant GDI sont limitées aux descripteurs GDI 10240 par processus et 65536 Handles GDI par session. Cela est dû au fait que Windows en interne utilise un mot 16 bits pour stocker l’index des descripteurs pour chaque session.

### <a name="gdi"></a>GDI+

Bien que GDI+ prenne en charge l’anticrénelage et la fusion alpha pour un dessin de grande qualité, le principal problème avec GDI+ pour les scénarios de serveur est qu’il ne prend pas en charge l’exécution dans la session 0. Étant donné que la session 0 ne prend en charge que les fonctionnalités non interactives, les fonctions qui interagissent directement ou indirectement avec les appareils d’affichage recevront donc des erreurs. Les exemples de fonctions spécifiques incluent non seulement ceux qui traitent des appareils d’affichage, mais également ceux qui traitent indirectement des pilotes de périphérique.

Semblable à GDI, GDI+ est limité par son mécanisme de verrouillage. Les mécanismes de verrouillage dans GDI+ sont les mêmes dans Windows 7 et Windows Server 2008 R2, comme dans les versions précédentes.

### <a name="direct2d"></a>Direct2D

Direct2D est une API graphique à accélération matérielle, en mode immédiat, en 2D, qui offre des performances élevées et un rendu de haute qualité. Il offre une fabrique à thread unique et une fabrique multithread, ainsi que la mise à l’échelle linéaire d’un rendu logiciel à granularité de cours.

Pour ce faire, Direct2D définit une interface de fabrique racine. En règle générale, un objet créé sur une fabrique peut uniquement être utilisé avec d’autres objets créés à partir de la même fabrique. L’appelant peut demander une fabrique à thread unique ou multithread lorsqu’il est créé. Si une fabrique à thread unique est demandée, aucun verrouillage de threads n’est effectué. Si l’appelant demande une fabrique multithread, un verrou de thread à l’intérieur de l’usine est acquis à chaque fois qu’un appel est effectué dans Direct2D.

En outre, le verrouillage des threads dans Direct2D est plus granulaire que dans GDI et GDI+, afin que l’augmentation du nombre de threads ait un impact minimal sur les performances.

## <a name="how-to-use-direct2d-for-server-side-rendering"></a>Utilisation de Direct2D pour le rendu Server-Side

Les sections suivantes décrivent comment utiliser le rendu logiciel, comment utiliser de façon optimale une fabrique à thread unique et une fabrique multithread, et comment dessiner et enregistrer un dessin complexe dans un fichier.

### <a name="software-rendering"></a>Rendu logiciel

Les applications côté serveur utilisent le rendu logiciel en créant une cible de rendu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , avec le type de cible de rendu défini sur le type de cible de rendu d2d1 ou le type de \_ cible de \_ \_ \_ \_ rendu d2d1 \_ \_ \_ par défaut. Pour plus d’informations sur les cibles de rendu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , consultez la méthode [**ID2D1Factory :: CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) ; Pour plus d’informations sur les types de cibles de rendu, consultez [**\_ type de \_ cible \_ de rendu d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="multithreading"></a>Multithreading

Savoir comment créer et partager des usines et des cibles de rendu sur les threads peut avoir un impact significatif sur les performances d’une application. Les trois figures suivantes présentent trois approches différentes. L’approche optimale est illustrée à la figure 3.

![diagramme multithread de Direct2D avec une seule cible de rendu.](images/server-side-rendering-1.png)

Dans la figure 1, les différents threads partagent la même fabrique et la même cible de rendu. Cette approche peut entraîner des résultats imprévisibles lorsque plusieurs threads modifient simultanément l’état de la cible de rendu partagée, par exemple la définition simultanée de la matrice de transformation. Étant donné que le verrouillage interne dans Direct2D ne synchronise pas une ressource partagée comme les cibles de rendu, cette approche peut provoquer l’échec de l’appel [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) dans le thread 1, car dans le thread 2, l’appel de **BeginDraw** utilise déjà la cible de rendu partagée.

![diagramme multithread de Direct2D avec plusieurs cibles de rendu.](images/server-side-rendering-2.png)

Pour éviter les résultats imprévisibles de la figure 1, la figure 2 illustre une fabrique multithread avec chaque thread ayant sa propre cible de rendu. Cette approche fonctionne, mais elle fonctionne efficacement comme une application à thread unique. La raison en est que le verrou à l’échelle de l’usine s’applique uniquement au niveau de l’opération de dessin et que tous les appels de dessin dans la même fabrique sont donc sérialisés. Par conséquent, le thread 1 est bloqué lors d’une tentative d’entrée d’un appel de dessin, alors que le thread 2 est en train d’exécuter un autre appel de dessin.

![diagramme multithread de Direct2D avec plusieurs fabriques et plusieurs cibles de rendu.](images/server-side-rendering-3.png)

La figure 3 illustre l’approche optimale, où une fabrique à thread unique et une cible de rendu monothread sont utilisées. Dans la mesure où aucun verrouillage n’est effectué lors de l’utilisation d’une fabrique à thread unique, les opérations de dessin dans chaque thread peuvent s’exécuter simultanément pour obtenir des performances optimales.

### <a name="generating-a-bitmap-file"></a>Génération d’un fichier bitmap

Pour générer un fichier bitmap à l’aide du rendu logiciel, utilisez une cible de rendu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) . Utilisez un [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) pour écrire l’image bitmap dans un fichier. Utilisez [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) pour encoder la bitmap dans un format d’image spécifié. L’exemple de code suivant montre comment dessiner et enregistrer l’image suivante dans un fichier.

![exemple d’image de sortie.](images/saveasimagefile-sample.png)

Cet exemple de code crée d’abord un [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) et une cible de rendu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) . Il affiche ensuite un dessin avec du texte, une géométrie de tracé représentant une heure et un verre d’heure transformé en bitmap WIC. Il utilise ensuite [IWICStream :: InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) pour enregistrer l’image bitmap dans un fichier. Si votre application doit enregistrer l’image bitmap en mémoire, utilisez [IWICStream :: InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) à la place. Enfin, il utilise [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) pour encoder l’image bitmap.


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a>Conclusion

Comme indiqué dans l’exemple ci-dessus, l’utilisation de Direct2D pour le rendu côté serveur est simple et directe. En outre, il fournit un rendu de haute qualité et de haut niveau de parallèles qui peut s’exécuter dans des environnements à faibles privilèges du serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 