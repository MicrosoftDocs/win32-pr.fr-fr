---
title: Didacticiel Prise en main avec DirectWrite
description: ce document vous montre comment utiliser DirectWrite et Direct2D pour créer du texte simple qui contient un format unique, puis du texte qui contient plusieurs formats.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, didacticiel
- DirectWrite, didacticiel de mise en route
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, interface IDWriteTextLayout
- Interface IDWriteTextLayout
- DirectWrite, interface IDWriteTypography
- Interface IDWriteTypography
- DirectWrite, interface IDWriteTextFormat
- Interface IDWriteTextFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ab22f611ea4658870990002bf98ac3c2ab9ffec32405ed8e67c32b819406496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083467"
---
# <a name="tutorial-getting-started-with-directwrite"></a>Didacticiel : Prise en main avec DirectWrite

ce document vous montre comment utiliser [DirectWrite](direct-write-portal.md) et [Direct2D](rendering-by-using-direct2d.md) pour créer du texte simple qui contient un format unique, puis du texte qui contient plusieurs formats.

Ce didacticiel contient les éléments suivants :

-   [Code source](#source-code)
-   [Dessiner du texte simple](#drawing-simple-text)
    -   [partie 1 : déclarer des ressources DirectWrite et Direct2D.](#part-1-declare-directwrite-and-direct2d-resources)
    -   [Partie 2 : créer des ressources indépendantes de l’appareil.](#part-2-create-device-independent-resources)
    -   [Partie 3 : créer des ressources Device-Dependent.](#part-3-create-device-dependent-resources)
    -   [Partie 4 : dessiner du texte à l’aide de la méthode DrawText de Direct2D.](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [Partie 5 : rendu du contenu de la fenêtre à l’aide de Direct2D](#part-5-render-the-window-contents-using-direct2d)
-   [Dessin de texte avec plusieurs formats.](#drawing-text-with-multiple-formats)
    -   [Partie 1 : créer une interface IDWriteTextLayout.](#part-1-create-an-idwritetextlayout-interface)
    -   [Partie 2 : application de la mise en forme avec IDWriteTextLayout.](#part-2-applying-formatting-with-idwritetextlayout)
    -   [Partie 3 : ajout de fonctionnalités typographiques avec IDWriteTypography.](#part-3-adding-typographic-features-with-idwritetypography)
    -   [Partie 4 : dessiner du texte à l’aide de la méthode Direct2D DrawTextLayout.](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a>Code source

le code source présenté dans cette vue d’ensemble est tiré de l' [exemple DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples). Chaque partie est implémentée dans une classe distincte (SimpleText et MultiformattedText) et s’affiche dans une fenêtre enfant distincte. Chaque classe représente une fenêtre Microsoft Win32. En plus de la méthode *WndProc* , chaque classe contient les méthodes suivantes :



| Fonction                              | Description                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| **CreateDeviceIndependentResources**  | Crée des ressources indépendantes des appareils, afin qu’elles puissent être réutilisées n’importe où.                      |
| **DiscardDeviceIndependentResources** | Libère les ressources indépendantes du périphérique une fois qu’elles ne sont plus nécessaires.                          |
| **CreateDeviceResources**             | Crée des ressources, telles que des pinceaux et des cibles de rendu, qui sont liées à un appareil particulier.        |
| **DiscardDeviceResources**            | Libère les ressources dépendantes de l’appareil une fois qu’elles ne sont plus nécessaires.                            |
| **DrawD2DContent**                    | Utilise [Direct2D](../direct2d/direct2d-portal.md) pour effectuer le rendu à l’écran.                              |
| **DrawText**                          | Dessine la chaîne de texte à l’aide de [Direct2D](../direct2d/direct2d-portal.md).                            |
| **OnResize**                          | Redimensionne la cible de rendu [Direct2D](../direct2d/direct2d-portal.md) lorsque la taille de la fenêtre est modifiée. |



 

vous pouvez utiliser l’exemple fourni ou suivre les instructions qui suivent pour ajouter [DirectWrite](direct-write-portal.md) et [Direct2D](rendering-by-using-direct2d.md) à votre propre application Win32. Pour plus d’informations sur l’exemple et les fichiers projet associés, consultez l' [exemple DirectWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="drawing-simple-text"></a>Dessiner du texte simple

cette section montre comment utiliser [DirectWrite](direct-write-portal.md) et [Direct2D](../direct2d/direct2d-portal.md) pour afficher du texte simple avec un format unique, comme illustré dans la capture d’écran suivante.

![capture d’écran de « Hello World using DirectWrite ! » dans un format unique](images/simplecropped.png)

Le fait de dessiner du texte simple à l’écran nécessite quatre composants :

-   Chaîne de caractères à afficher.
-   Une instance de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).
-   Dimensions de la zone devant contenir le texte.
-   Objet qui peut restituer le texte. Dans ce didacticiel. vous utilisez une cible de rendu [Direct2D](../direct2d/direct2d-portal.md) .

L’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) décrit le nom, la taille, le poids, le style et l’étirement de la famille de polices utilisés pour mettre en forme le texte, et il décrit les informations relatives aux paramètres régionaux. **IDWriteTextFormat** définit également des méthodes pour définir et obtenir les propriétés suivantes :

-   Interligne.
-   Alignement du texte par rapport aux bords gauche et droit de la zone de disposition.
-   Alignement du paragraphe par rapport au haut et au bas de la zone de disposition.
-   Sens de lecture.
-   Granularité de la suppression de texte pour le texte qui dépasse la zone de disposition.
-   Taquet de tabulation incrémentiel.
-   Sens du déroulement du paragraphe.

L’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) est requise pour dessiner du texte qui utilise les deux processus décrits dans ce document.

avant de pouvoir créer un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou tout autre objet [DirectWrite](direct-write-portal.md) , vous avez besoin d’une instance [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) . vous utilisez un **IDWriteFactory** pour créer des instances **IDWriteTextFormat** et d’autres objets DirectWrite. Pour obtenir une instance de fabrique, utilisez la fonction [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a>partie 1 : déclarer des ressources DirectWrite et Direct2D.

Dans cette partie, vous déclarez les objets que vous utiliserez ultérieurement pour créer et afficher du texte sous la forme de membres de données privés de votre classe. toutes les interfaces, fonctions et types de données pour [DirectWrite](direct-write-portal.md) sont déclarés dans le fichier d’en-tête *dwrite. h* , et ceux de [Direct2D](../direct2d/direct2d-portal.md) sont déclarés dans *d2d1. h*. Si vous ne l’avez pas encore fait, incluez ces en-têtes dans votre projet.

1.  Dans votre fichier d’en-tête de classe (SimpleText. h), déclarez des pointeurs vers des interfaces [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) et [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) en tant que membres privés.
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  Déclarez les membres pour contenir la chaîne de texte à restituer et la longueur de la chaîne.
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  Déclarez des pointeurs vers des interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)et [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pour le rendu du texte avec [Direct2D](../direct2d/direct2d-portal.md).
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a>Partie 2 : créer des ressources indépendantes de l’appareil.

[Direct2D](rendering-by-using-direct2d.md) fournit deux types de ressources : les ressources dépendantes de l’appareil et les ressources indépendantes du périphérique. Les ressources dépendantes de l’appareil sont associées à un périphérique de rendu et ne fonctionnent plus si l’appareil est supprimé. Les ressources indépendantes du périphérique, en revanche, peuvent être utilisées en dernier pour l’étendue de votre application.

les ressources de [DirectWrite](direct-write-portal.md) sont indépendantes des appareils.

Dans cette section, vous allez créer les ressources indépendantes du périphérique qui sont utilisées par votre application. Ces ressources doivent être libérées à l’aide d’un appel à la méthode **Release** de l’interface.

Certaines des ressources utilisées ne doivent être créées qu’une seule fois et ne sont pas liées à un appareil. L’initialisation de ces ressources est placée dans la méthode *SimpleText :: CreateDeviceIndependentResources* , qui est appelée lors de l’initialisation de la classe.

1.  À l’intérieur de la méthode *SimpleText :: CreateDeviceIndependentResources* dans le fichier d’implémentation de classe (SimpleText. cpp), appelez la fonction [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) pour créer une interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , qui est l’interface de fabrique racine pour tous les objets [Direct2D](../direct2d/direct2d-portal.md) . Vous utilisez la même fabrique pour instancier d’autres ressources Direct2D.
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  appelez la fonction [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) pour créer une interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , qui est l’interface de fabrique racine pour tous les objets [DirectWrite](direct-write-portal.md) . vous utilisez la même fabrique pour instancier d’autres ressources de DirectWrite.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  Initialisez la chaîne de texte et stockez sa longueur.

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  Créez un objet d’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) à l’aide de la méthode [**IDWriteFactory :: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) . Le **IDWriteTextFormat** spécifie la police, le poids, l’étirement, le style et les paramètres régionaux qui seront utilisés pour le rendu de la chaîne de texte.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  Centrez le texte horizontalement et verticalement en appelant les méthodes [**IDWriteTextFormat :: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) et [**IDWriteTextFormat :: SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) .
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

Dans cette partie, vous avez initialisé les ressources indépendantes du périphérique qui sont utilisées par votre application. Dans la partie suivante, vous initialisez les ressources dépendantes de l’appareil.

### <a name="part-3-create-device-dependent-resources"></a>Partie 3 : créer des ressources Device-Dependent.

Dans cette partie, vous créez un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) et un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pour le rendu de votre texte.

Une cible de rendu est un objet Direct2D qui crée des ressources de dessin et restitue des commandes de dessin sur un appareil de rendu. Un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) est une cible de rendu qui est restituée à un **HWND**.

L’une des ressources de dessin qu’une cible de rendu peut créer est un pinceau pour peindre des contours, des remplissages et du texte. Un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) peint avec une couleur unie.

Les interfaces [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) et [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) sont liées à un appareil de rendu lorsqu’elles sont créées et doivent être libérées et recréées si l’appareil n’est plus valide.

1.  À l’intérieur de la méthode SimpleText :: CreateDeviceResources, vérifiez si le pointeur de la cible de rendu a la **valeur null**. Si c’est le cas, récupérez la taille de la zone de rendu et créez un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) de cette taille. Utilisez **ID2D1HwndRenderTarget** pour créer un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  Dans la méthode SimpleText ::D iscardDeviceResources, libérez à la fois le pinceau et la cible de rendu.
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

Maintenant que vous avez créé une cible de rendu et un pinceau, vous pouvez les utiliser pour restituer votre texte.

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a>Partie 4 : dessiner du texte à l’aide de la méthode DrawText de Direct2D.

1.  Dans la méthode SimpleText ::D rawText de votre classe, définissez la zone pour la disposition du texte en extrayant les dimensions de la zone de rendu et créez un rectangle [Direct2D](../direct2d/direct2d-portal.md) qui a les mêmes dimensions.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Utilisez la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) et l’objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pour afficher du texte à l’écran. La méthode **ID2D1RenderTarget ::D rawtext** accepte les paramètres suivants :
    -   Chaîne à restituer.
    -   Pointeur vers une interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .
    -   Rectangle de disposition [Direct2D](../direct2d/direct2d-portal.md) .
    -   Pointeur vers une interface qui expose [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a>Partie 5 : rendu du contenu de la fenêtre à l’aide de Direct2D

Pour afficher le contenu de la fenêtre à l’aide de [Direct2D](../direct2d/direct2d-portal.md) lors de la réception d’un message de peinture, procédez comme suit :

1.  Créez les ressources dépendantes de l’appareil en appelant la méthode SimpleText :: CreateDeviceResources implémentée dans la partie 3.
2.  Appelez la méthode [**ID2D1HwndRenderTarget :: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) de la cible de rendu.
3.  Effacez la cible de rendu en appelant la méthode [**ID2D1HwndRenderTarget :: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) .
4.  Appelez la méthode SimpleText ::D rawText, implémentée dans la partie 4.
5.  Appelez la méthode [**ID2D1HwndRenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) de la cible de rendu.
6.  Si nécessaire, ignorez les ressources dépendantes de l’appareil afin qu’elles puissent être recréées lorsque la fenêtre est redessinée.


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



La classe SimpleText est implémentée dans SimpleText. h et SimpleText. cpp.

## <a name="drawing-text-with-multiple-formats"></a>Dessin de texte avec plusieurs formats.

cette section montre comment utiliser [DirectWrite](direct-write-portal.md) et [Direct2D](../direct2d/direct2d-portal.md) pour restituer du texte avec plusieurs formats, comme illustré dans la capture d’écran suivante.

![capture d’écran de « Hello World using DirectWrite ! », avec certaines parties dans différents styles, tailles et formats](images/multiformattedcropped.png)

Le code de cette section est implémenté en tant que classe MultiformattedText dans l' [exemple DWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples). Elle est basée sur les étapes de la section précédente.

Pour créer du texte à plusieurs mises en forme, vous utilisez l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en plus de l’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) introduite dans la section précédente. L’interface **IDWriteTextLayout** décrit la mise en forme et la mise en page d’un bloc de texte. En plus de la mise en forme par défaut spécifiée par un objet **IDWriteTextFormat** , la mise en forme de plages de texte spécifiques peut être modifiée à l’aide de **IDWriteTextLayout**. Cela comprend le nom de famille de polices, la taille, le poids, le style, l’étirement, le barré et le soulignement.

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) fournit également des méthodes de test de positionnement. Les métriques de test de positionnement retournées par ces méthodes sont relatives à la zone de disposition spécifiée lors de la création de l’objet d’interface **IDWriteTextLayout** à l’aide de la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) de l’interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

L’interface [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) est utilisée pour ajouter des fonctionnalités typographiques [OpenType](../intl/opentype-font-format.md) facultatives à une disposition de texte, telles que des lettres ornées et des ensembles de texte stylistiques alternatifs. Les fonctionnalités typographiques peuvent être ajoutées à une plage de texte spécifique dans une disposition de texte en appelant la méthode [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) de l’interface **IDWriteTypography** . Cette méthode reçoit une structure de [**\_ \_ fonctionnalité de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) en tant que paramètre qui contient une constante d’énumération de **\_ \_ \_ balise de fonctionnalité de police DWRITE** et un paramètre d’exécution **UInt32** . Vous trouverez une liste des fonctionnalités OpenType inscrites dans le [Registre de balises de disposition OpenType](https://www.microsoft.com/typography/otspec/features_ae.htm) sur Microsoft.com. pour obtenir les DirectWrite équivalentes des constantes d’énumération, consultez **\_ \_ \_ balise de fonctionnalité de police DWRITE**.

### <a name="part-1-create-an-idwritetextlayout-interface"></a>Partie 1 : créer une interface IDWriteTextLayout.

1.  Déclarez un pointeur vers une interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en tant que membre de la classe MultiformattedText.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  À la fin de la méthode MultiformattedText :: CreateDeviceIndependentResources, créez un objet d’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en appelant la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) . L’interface **IDWriteTextLayout** fournit des fonctionnalités de mise en forme supplémentaires, telles que la possibilité d’appliquer des formats différents aux portions de texte sélectionnées.
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a>Partie 2 : application de la mise en forme avec IDWriteTextLayout.

La mise en forme, telle que la taille de la police, le poids et le soulignement, peut être appliquée aux sous-chaînes du texte à afficher à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

1.  définissez la taille de police de la sous-chaîne « Di » de « DirectWrite » sur 100 en déclarant [**une \_ \_ plage de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) et en appelant la méthode [**IDWriteTextLayout :: SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) .
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  soulignez la sous-chaîne « DirectWrite » en appelant la méthode [**IDWriteTextLayout :: SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  affectez la valeur gras à l’épaisseur de la police pour la sous-chaîne « DirectWrite » en appelant la méthode [**IDWriteTextLayout :: SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) .
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a>Partie 3 : ajout de fonctionnalités typographiques avec IDWriteTypography.

1.  Déclarez et créez un objet d’interface [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) en appelant la méthode [**IDWriteFactory :: CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) .
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  Ajoutez une fonctionnalité de police en déclarant un objet de [**\_ \_ fonctionnalité de police DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) dont le jeu stylistique 7 est spécifié et en appelant la méthode [**IDWriteTypography :: AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) .
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  Définissez la disposition du texte pour utiliser la typographie sur l’ensemble de la chaîne en déclarant une variable de [**\_ \_ portée de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) et en appelant la méthode [**IDWriteTextLayout :: SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) et en passant dans la plage de texte.
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  Définissez la nouvelle largeur et la hauteur de l’objet de disposition du texte dans la méthode MultiformattedText :: OnResize.
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a>Partie 4 : dessiner du texte à l’aide de la méthode Direct2D DrawTextLayout.

Pour dessiner le texte avec les paramètres de disposition du texte spécifiés par l’objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , modifiez le code de la méthode MultiformattedText ::D rawtext de sorte qu’il utilise [**IDWriteTextLayout ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Delcare une variable [**d2d1 \_ point \_ 2F**](../direct2d/d2d1-point-2f.md) et définissez-la sur le point supérieur gauche de la fenêtre.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Dessinez le texte à l’écran en appelant la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) de la cible de rendu [Direct2D](../direct2d/direct2d-portal.md) et en passant le pointeur [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

La classe MultiformattedText est implémentée dans MultiformattedText. h et MultiformattedText. cpp.

 

 