---
title: Polices de couleur
description: Cette rubrique décrit les polices de couleur, leur prise en charge dans DirectWrite et Direct2D, et comment les utiliser dans votre application.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104563967"
---
# <a name="color-fonts"></a>Polices de couleur

Cette rubrique décrit les polices de couleur, leur prise en charge dans DirectWrite et Direct2D, et comment les utiliser dans votre application.

Ce document contient les éléments suivants :

-   [Que sont les polices de couleur ?](#what-are-color-fonts)
-   [Pourquoi utiliser des polices de couleur ?](#why-use-color-fonts)
-   [Quels types de polices de couleurs Windows prend-il en charge ?](#what-kinds-of-color-fonts-does-windows-support)
-   [Utilisation des polices de couleur](#using-color-fonts)
    -   [Utilisation des polices de couleur dans une application XAML](#using-color-fonts-in-a-xaml-app)
    -   [Utilisation des polices de couleur dans Microsoft Edge](#using-color-fonts-in-microsoft-edge)
    -   [Utilisation des polices de couleur avec DirectWrite et Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Utilisation des polices de couleur avec Win2D](#using-color-fonts-with-win2d)
-   [Rubriques connexes](#related-topics)

## <a name="what-are-color-fonts"></a>Que sont les polices de couleur ?

Les polices de couleur, également appelées polices multicolores ou polices chromatiques, sont une technologie de police qui permet aux concepteurs de polices d’utiliser plusieurs couleurs dans chaque glyphe. Les polices de couleur activent les scénarios de texte multicolore dans les applications et les sites Web avec moins de code et une prise en charge de système d’exploitation plus robuste que les techniques ad hoc implémentées au-dessus du système de rendu de texte.

Les polices que vous connaissez sans doute ne sont pas des polices de couleurs. Ces polices définissent uniquement la forme des glyphes qu’elles contiennent, soit avec des contours vectoriels, soit avec des images bitmap monochromatiques. Au moment du tracé, un convertisseur de texte remplit la forme de glyphe à l’aide d’une couleur unique (la couleur de police) spécifiée par l’application ou le document en cours de rendu. Les polices de couleur, quant à elles, contiennent des informations de couleur en plus des informations de forme. Certaines approches permettent aux concepteurs de polices d’offrir plusieurs palettes de couleurs, ce qui donne la flexibilité de la police de couleur artistique.

L’exemple suivant montre un glyphe issu de la police de couleur Segoe UI Emoji. Le glyphe est rendu en monochrome à gauche et dans la couleur à droite.

![Affiche des glyphes côte à côte, le glyphe gauche rendu en monochrome, le droit dans la police de couleur d’Emoji Segoe U I.](images/color-font-cat.png)

Les polices de couleur incluent généralement des informations de secours pour les plateformes qui ne prennent pas en charge les polices de couleur ou pour les scénarios dans lesquels la fonctionnalité de couleur a été désactivée. Sur ces plateformes, les polices de couleur sont rendues en tant que polices monochromatiques standard.

## <a name="why-use-color-fonts"></a>Pourquoi utiliser des polices de couleur ?

Historiquement, les concepteurs et les développeurs ont utilisé diverses techniques pour obtenir du texte multicolore. Par exemple, les sites Web utilisent souvent des images raster au lieu de texte pour afficher des en-têtes enrichis. Cette approche permet une flexibilité artistique, mais les graphiques raster ne sont pas adaptés à toutes les tailles d’affichage et ne fournissent pas les mêmes fonctionnalités d’accessibilité que le texte réel. Une autre technique courante consiste à superposer plusieurs polices monochromatiques dans différentes couleurs de police, mais cela nécessite généralement un code de disposition supplémentaire à gérer.

Les polices de couleur offrent un moyen d’obtenir ces effets visuels avec toute la simplicité et les fonctionnalités des polices standard. Le texte affiché dans une police de couleur est identique à un autre texte : il peut être copié et collé, il peut être analysé par les outils d’accessibilité, et ainsi de suite.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>Quels types de polices de couleurs Windows prend-il en charge ?

La [spécification OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) définit plusieurs manières d’incorporer des informations de couleur dans une police. À compter de la mise à jour anniversaire de Windows 10, DirectWrite et Direct2D (et les infrastructures Windows qui s’y basent) prennent en charge toutes ces approches. Elles sont résumées dans le tableau ci-dessous :



| Technique                                                                                                                        | Description                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Colr](/typography/opentype/spec/colr) / Tables [CPAL](/typography/opentype/spec/cpal) | Utilise des couches de vecteurs de couleur, dont les formes sont définies de la même façon que les contours de glyphe de couleur unique. **Remarque :** Prise en charge à partir de Windows 8.1. <br/>                                                                                                                                                 |
| Table [SVG](/typography/opentype/spec/svg)                                                                 | Utilise des images vectorielles créées dans le format graphique vectoriel Scalable. **Remarque :** À compter de la mise à jour anniversaire de Windows 10, DirectWrite prend en charge un sous-ensemble de la spécification SVG complète. Le rendu de tout le contenu SVG n’est pas garanti dans une police OpenType SVG. Pour plus d’informations, consultez [prise en charge SVG](../direct2d/svg-support.md) . <br/> |
| [CBDT](/typography/opentype/spec/cbdt) / Tables [CBLC](/typography/opentype/spec/cblc) | Utilise des images bitmap de couleur incorporées.                                                                                                                                                                                                                                                                                |
| table [sbix](/typography/opentype/spec/sbix)                                                               | Utilise des images bitmap de couleur incorporées.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Utilisation des polices de couleur

Du point de vue des utilisateurs, les polices de couleur sont simplement des polices. Par exemple, ils peuvent généralement être installés et désinstallés du système de la même façon que les polices monochromatiques, et ils sont rendus sous forme de texte normal et sélectionnable.

Du point de vue du développeur, les polices de couleur sont généralement utilisées de la même façon que les polices monochromatiques. Dans les infrastructures XAML et Microsoft Edge, vous pouvez définir le style de votre texte avec les polices de couleur de la même façon que les polices standard, et par défaut, votre texte est rendu en couleur. Toutefois, si votre application appelle directement les API Direct2D (ou API Win2D) pour restituer le texte, elle doit explicitement demander le rendu des polices de couleurs.

### <a name="using-color-fonts-in-a-xaml-app"></a>Utilisation des polices de couleur dans une application XAML

Les éléments de texte de la plateforme XAML (tels que [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)et [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) prennent en charge les polices de couleur par défaut. Il vous suffit de définir le style de votre texte avec une police de couleur, et les glyphes de couleur sont rendus en couleur. L’exemple de code suivant montre une façon de styliser un TextBlock avec une police de couleur empaquetée avec votre application. La même technique s’applique aux polices normales.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Si vous ne souhaitez pas que votre élément de texte XAML restitue le texte multicolore, affectez la valeur false à sa propriété [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) .

### <a name="using-color-fonts-in-microsoft-edge"></a>Utilisation des polices de couleur dans Microsoft Edge

Les polices de couleur sont rendues par défaut dans les sites Web et les applications Web s’exécutant sur Microsoft Edge, y compris le contrôle XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) . Utilisez simplement HTML et CSS pour appliquer un style à votre texte avec une police de couleur, et les glyphes de couleur sont rendus en couleur.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Utilisation des polices de couleur avec DirectWrite et Direct2D

Votre application peut utiliser des méthodes de dessin de texte de niveau supérieur de Direct2D ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) et [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) ou elle peut utiliser des techniques de niveau inférieur pour dessiner des exécutions de glyphes directement. Dans les deux cas, votre application requiert des modifications de code afin de gérer correctement les glyphes de couleurs. Si votre application utilise les API de la valeur de Direct2D s **DrawText** et **DrawTextLayout** , Notez que celles-ci ne restituent pas les glyphes de couleur par défaut. Cela permet d’éviter des changements de comportement inattendus dans les applications de rendu de texte qui ont été conçues avant la prise en charge des polices de couleur.

Pour accepter le rendu des glyphes de couleurs, transmettez l’indicateur de dessin [**d2d1 \_ \_ \_ options \_ activer \_ \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) les options de police de couleur à la méthode de dessin. L’exemple de code suivant montre comment appeler Direct2D s DrawText, méthode pour restituer une chaîne dans une police de couleur :


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



Si votre application utilise des API de niveau inférieur pour gérer les exécutions de glyphe directement, elle continuera à fonctionner en présence de polices de couleur, mais elle ne pourra pas dessiner de glyphes de couleur sans logique supplémentaire.

Pour gérer correctement les glyphes de couleur, votre application doit :

1.  Transmettez les informations d’exécution du glyphe à [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), ainsi qu’un paramètre de [**formats d' \_ \_ image \_ de glyphe DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) qui indique le ou les types de glyphes de couleur que l’application est prêt à gérer. Si des glyphes de couleur sont présents (selon la police et les **formats d' \_ \_ image de \_ glyphe DWRITE** demandés), DirectWrite fractionne l’exécution du glyphe principal en différentes exécutions de glyphes de couleurs, accessibles via l’objet [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) retourné à l’étape 4.
2.  Vérifiez le HRESULT retourné par [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) pour déterminer si des exécutions de glyphes de couleurs ont été détectées. Un **HRESULT** de **DWRITE \_ E \_ nocolor** n’indique aucune exécution de glyphe de couleur applicable.
3.  Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) n’a signalé aucune exécution de glyphes de couleurs (en retournant **DWRITE \_ E \_ nocolor**), l’exécution de glyphe entière est traitée comme monochromatique et votre application doit la dessiner comme vous le souhaitez (par exemple, à l’aide de [**ID2D1DeviceContext ::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).
4.  Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) signale la présence d’exécutions de glyphes de couleurs, votre application doit ignorer l’exécution du glyphe principal et utiliser à la place les exécutions de glyphes de couleur retournées par TranslateColorGlyphRun. Pour ce faire, itérez au sein de l’objet [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) retourné, en récupérant chaque exécution de glyphe de couleur et en le dessinant en fonction de son format d’image de glyphe (par exemple, vous pouvez utiliser [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) et [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) pour dessiner des glyphes de bitmap de couleur et des glyphes SVG, respectivement).

L’exemple de code suivant illustre la structure générale de cette procédure :


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a>Utilisation des polices de couleur avec Win2D

À l’instar de Direct2D, les API de dessin de texte Win2D s ne restituent pas les glyphes de couleur par défaut. Pour accepter le rendu des glyphes de couleurs, définissez l’indicateur options [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) dans l’objet de format de texte que votre application passe à la méthode de dessin de texte. L’exemple de code suivant montre comment restituer une chaîne dans une police de couleur à l’aide de Win2D :


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a>Rubriques connexes

[Exemple de glyphe de couleur DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**Interface IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**IDWriteFactory4 :: TranslateColorGlyphRun, méthode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**ID2D1DeviceContext4 ::D méthode rawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

