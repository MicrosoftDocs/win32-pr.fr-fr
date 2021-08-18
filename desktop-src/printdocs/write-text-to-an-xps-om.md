---
description: Cette rubrique explique comment écrire du texte dans un modèle d’objet XPS.
ms.assetid: 5552b7b0-1c95-43fa-ad06-c167c69c5a56
title: Écrire du texte dans un modèle d’objet XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff2c77106649960982888d7ee8d6e4b679bd62e44be1e0dc9786206261b62bbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718529"
---
# <a name="write-text-to-an-xps-om"></a>Écrire du texte dans un modèle d’objet XPS

Cette rubrique explique comment écrire du texte dans un modèle d’objet XPS.

Le texte est placé dans un modèle OM XPS en créant et en formatant une interface [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) , puis en ajoutant l’interface **IXpsOMGlyphs** à la liste des objets visuels de la page ou de la zone de dessin. Chaque interface **IXpsOMGlyphs** représente une exécution de glyphe, qui est une exécution continue de caractères qui partagent un format commun. Lorsqu’un élément de format caractère (tel que le type ou la taille de police) change ou qu’un saut de ligne est nécessaire, une nouvelle interface **IXpsOMGlyphs** doit être créée et ajoutée à la liste des objets visuels.

Certaines propriétés d’une exécution de glyphes peuvent être définies à l’aide des méthodes de l’interface [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) . Toutefois, certaines propriétés interagissent avec d’autres et doivent être définies à l’aide d’une interface [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) .

Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).

## <a name="code-example"></a>Exemple de code

### <a name="create-a-glyph-run-from-a-string"></a>Créer une exécution de glyphe à partir d’une chaîne

Une exécution de glyphe est couramment créée en plusieurs étapes, notamment le chargement des ressources de police utilisées par l’exécution du glyphe, la définition d’un pinceau de remplissage, la spécification de la taille de la police et de l’emplacement de départ, ainsi que la définition de la chaîne Unicode.

La section suivante de l’exemple de code contient une routine qui accepte certaines variables, y compris la taille de la police, la couleur et l’emplacement, ainsi que les caractères à écrire. Le code crée ensuite une exécution de glyphe, puis l’ajoute à une page. L’exemple de code suppose que l’initialisation décrite dans [Initialize an XPS OM](xps-object-model-initialization.md) s’est produite et que le document comporte au moins une page. Pour plus d’informations sur la création d’un modèle d’objet XPS vide, consultez [créer un modèle d’objet XPS vide](create-a-blank-xps-om.md).


```C++
// Write Text to an XPS OM
HRESULT
WriteText_AddTextToPage(
            // A pre-created object factory
    __in    IXpsOMObjectFactory   *xpsFactory,
            // The font resource to use for this run
    __in    IXpsOMFontResource    *xpsFont,
            // The font size
    __in    float                 fontEmSize,
            // The solid color brush to use for the font
    __in    IXpsOMSolidColorBrush *xpsBrush,
            // The starting location of this glyph run
    __in    XPS_POINT             *origin,
            // The text to use for this run
    __in    LPCWSTR               unicodeString,
            // The page on which to write this glyph run
    __inout IXpsOMPage            *xpsPage        
)
{
    // The data type definitions are included in this function
    // for the convenience of this code example. In an actual
    // implementation they would probably belong in a header file.
    HRESULT                       hr = S_OK;
    XPS_POINT                     glyphsOrigin = {origin->x, origin->y};
    IXpsOMGlyphsEditor            *glyphsEditor = NULL;
    IXpsOMGlyphs                  *xpsGlyphs = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;

    // Create a new Glyphs object and set its properties.
    hr = xpsFactory->CreateGlyphs(xpsFont, &xpsGlyphs);
    hr = xpsGlyphs->SetOrigin(&glyphsOrigin);
    hr = xpsGlyphs->SetFontRenderingEmSize(fontEmSize);
    hr = xpsGlyphs->SetFillBrushLocal(xpsBrush);

    // Some properties are inter-dependent so they
    //    must be changed by using a GlyphsEditor.
    hr = xpsGlyphs->GetGlyphsEditor(&glyphsEditor);
    hr = glyphsEditor->SetUnicodeString(unicodeString);
    hr = glyphsEditor->ApplyEdits();

    // Add the new Glyphs object to the page
    hr = xpsPage->GetVisuals(&pageVisuals);
    hr = pageVisuals->Append(xpsGlyphs);

    // Release interface pointers.
    if (NULL != xpsGlyphs) xpsGlyphs->Release();
    if (NULL != glyphsEditor) glyphsEditor->Release();
    if (NULL != pageVisuals) pageVisuals->Release();

    return hr;
}
```



### <a name="load-and-create-resources"></a>Charger et créer des ressources

La création d’une interface [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) nécessite une ressource de police. Dans de nombreux cas, un bloc de texte utilise la même police et la même couleur. Par conséquent, cette section de l’exemple de code créera les interfaces de ressource de police qui seront utilisées dans les appels qui placent le texte sur la page.


```C++
    // fontFileName is the name of the font file and it 
    //  is defined outside of this example.

    HRESULT                       hr = S_OK;

    GUID                          fontNameGuid;
    WCHAR                         guidString[128] = {0};
    WCHAR                         uriString[256] = {0};

    IStream                       *fontStream  = NULL;
    IOpcPartUri                   *fontUri = NULL;
    IXpsOMFontResource            *fontResource = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;
    IXpsOMPage                    *page = NULL;
    IXpsOMVisual                  *canvasVisual = NULL;
    IXpsOMSolidColorBrush         *xpsTextColor = NULL;
    XPS_COLOR                     xpsColorBodyText;
 
    // Create font stream.
    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
        fontFileName, &fontStream );
    
    // Create new obfuscated part name for this resource using a GUID.
    hr = CoCreateGuid( &fontNameGuid );
    hr = StringFromGUID2( 
            fontNameGuid, 
            guidString, 
            ARRAYSIZE(guidString));

    // Create a URI string for this font resource that will place 
    //  the font part in the /Resources/Fonts folder of the package.
    wcscpy_s(uriString, ARRAYSIZE(uriString), L"/Resources/Fonts/");

    // Create the part name using the GUID string as the name and 
    //  ".odttf" as the extension GUID string start and ends with 
    //  curly braces so they are removed.
    wcsncat_s(uriString, ARRAYSIZE(uriString), 
        guidString + 1, wcslen(guidString) - 2); 
    wcscat_s(uriString, ARRAYSIZE(uriString), L".odttf");

    // Create the font URI interface.
    hr = xpsFactory->CreatePartUri(
        uriString,
        &fontUri);
    // Create the font resource.
    hr = xpsFactory->CreateFontResource(
        fontStream,
        XPS_FONT_EMBEDDING_OBFUSCATED,
        fontUri,
        FALSE,     // isObfSourceStream
        &fontResource);
    if (NULL != fontUri) fontUri->Release();

    // Create the brush to use for the font.
    xpsColorBodyText.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColorBodyText.value.sRGB.alpha = 0xFF;
    xpsColorBodyText.value.sRGB.red = 0x00;
    xpsColorBodyText.value.sRGB.green = 0x00;
    xpsColorBodyText.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColorBodyText,
        NULL, // This color type does not use a color profile resource.             
        &xpsTextColor);

    // xpsTextColor is released after it has been used.
```



### <a name="draw-text-in-a-page"></a>Dessiner du texte dans une page

La dernière section de l’exemple de code crée les exécutions de glyphes pour chaque exécution du texte mis en forme de la même façon. Pour exécuter le code dans cette section finale, l’interface **xpsFactory** , ainsi que la ressource de police et un pinceau de couleur de texte sont nécessaires et doivent avoir été instanciés et initialisés. Dans cet exemple, la fonction décrite dans la première section est utilisée pour créer les exécutions de glyphe et les ajouter à la page.


```C++
    // The following interfaces are created outside of this example.

    // The page on which to place the text.
    IXpsOMPage                *page = NULL;

    // The object factory used by this program.
    IXpsOMObjectFactory       *xpsFactory = NULL;

    // The font resource created in the previous snippet.
    IXpsOMFontResource        *fontResource = NULL;

    // The color brush created in the previous snippet.
    IXpsOMSolidColorBrush     *xpsTextColor = NULL;

    // The following variables are defined outside of this example.

    // An array of pointers to the Unicode strings to write.
    LPCWSTR                   *textRuns = NULL;

    // An array of start points that correspond to the 
    //    strings in textRuns.
    XPS_POINT                 *startPoints = NULL;

    // The number of text runs to add to the page.
    UINT32                    numRuns = 0;            

    HRESULT                   hr = S_OK;

    FLOAT                     fontSize = 7.56f;
    UINT32                    thisRun;

    // Add all the text runs to the page.
    thisRun = 0;
    while (thisRun < numRuns) {  
        hr = WriteText_AddTextToPage(
            xpsFactory, 
            fontResource,
            fontSize,
            xpsTextColor,
            &startPoints[thisRun],
            textRuns[thisRun],
            page);
        thisRun++;
    }
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Naviguer dans le modèle d’objet XPS](navigate-the-xps-om.md)
</dt> <dt>

[Dessiner des graphiques dans un modèle d’objet XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Placer des images dans un modèle d’objet XPS](place-images-in-an-xps-om.md)
</dt> <dt>

[Écrire un modèle OM XPS dans un document XPS](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[Imprimer un modèle OM XPS](print-an-xps-om.md)
</dt> <dt>

**Utilisé dans cette section**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMFontResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[Initialiser un modèle d’objet XPS](xps-object-model-initialization.md)
</dt> <dt>

[Informations de référence sur l’API de document XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
