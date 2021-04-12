---
description: Cette rubrique explique comment écrire du texte dans un modèle d’objet XPS.
ms.assetid: 5552b7b0-1c95-43fa-ad06-c167c69c5a56
title: Écrire du texte dans un modèle d’objet XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cca953d5281620cf7b7d9b7b07c133bee0d4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203705"
---
# <a name="write-text-to-an-xps-om"></a><span data-ttu-id="64fd7-103">Écrire du texte dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="64fd7-103">Write Text to an XPS OM</span></span>

<span data-ttu-id="64fd7-104">Cette rubrique explique comment écrire du texte dans un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="64fd7-104">This topic describes how to write text to an XPS OM.</span></span>

<span data-ttu-id="64fd7-105">Le texte est placé dans un modèle OM XPS en créant et en formatant une interface [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) , puis en ajoutant l’interface **IXpsOMGlyphs** à la liste des objets visuels de la page ou de la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="64fd7-105">Text is placed in an XPS OM by creating and formatting an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface and then adding the **IXpsOMGlyphs** interface to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="64fd7-106">Chaque interface **IXpsOMGlyphs** représente une exécution de glyphe, qui est une exécution continue de caractères qui partagent un format commun.</span><span class="sxs-lookup"><span data-stu-id="64fd7-106">Each **IXpsOMGlyphs** interface represents a glyph run, which is a continuous run of characters that share a common format.</span></span> <span data-ttu-id="64fd7-107">Lorsqu’un élément de format caractère (tel que le type ou la taille de police) change ou qu’un saut de ligne est nécessaire, une nouvelle interface **IXpsOMGlyphs** doit être créée et ajoutée à la liste des objets visuels.</span><span class="sxs-lookup"><span data-stu-id="64fd7-107">When a character format element (such as font type or size) changes or when a line breaks, a new **IXpsOMGlyphs** interface must be created and added to the list of visual objects.</span></span>

<span data-ttu-id="64fd7-108">Certaines propriétés d’une exécution de glyphes peuvent être définies à l’aide des méthodes de l’interface [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) .</span><span class="sxs-lookup"><span data-stu-id="64fd7-108">Some of the properties of a glyph run can be set by using the methods of the [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface.</span></span> <span data-ttu-id="64fd7-109">Toutefois, certaines propriétés interagissent avec d’autres et doivent être définies à l’aide d’une interface [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) .</span><span class="sxs-lookup"><span data-stu-id="64fd7-109">Some properties, however, interact with others and must be set by using an [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) interface.</span></span>

<span data-ttu-id="64fd7-110">Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="64fd7-110">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="64fd7-111">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="64fd7-111">Code Example</span></span>

### <a name="create-a-glyph-run-from-a-string"></a><span data-ttu-id="64fd7-112">Créer une exécution de glyphe à partir d’une chaîne</span><span class="sxs-lookup"><span data-stu-id="64fd7-112">Create a glyph run from a string</span></span>

<span data-ttu-id="64fd7-113">Une exécution de glyphe est couramment créée en plusieurs étapes, notamment le chargement des ressources de police utilisées par l’exécution du glyphe, la définition d’un pinceau de remplissage, la spécification de la taille de la police et de l’emplacement de départ, ainsi que la définition de la chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="64fd7-113">A glyph run is commonly created in several steps that include loading the font resources that are used by the glyph run, setting a fill brush, specifying the font size and starting location, and setting the Unicode string.</span></span>

<span data-ttu-id="64fd7-114">La section suivante de l’exemple de code contient une routine qui accepte certaines variables, y compris la taille de la police, la couleur et l’emplacement, ainsi que les caractères à écrire.</span><span class="sxs-lookup"><span data-stu-id="64fd7-114">The following section of the code example contains a routine that accepts some variables, including the font size, color and location, and the characters to be written.</span></span> <span data-ttu-id="64fd7-115">Le code crée ensuite une exécution de glyphe, puis l’ajoute à une page.</span><span class="sxs-lookup"><span data-stu-id="64fd7-115">The code then creates a glyph run and then adds it to a page.</span></span> <span data-ttu-id="64fd7-116">L’exemple de code suppose que l’initialisation décrite dans [Initialize an XPS OM](xps-object-model-initialization.md) s’est produite et que le document comporte au moins une page.</span><span class="sxs-lookup"><span data-stu-id="64fd7-116">The code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has occurred and that the document has at least one page.</span></span> <span data-ttu-id="64fd7-117">Pour plus d’informations sur la création d’un modèle d’objet XPS vide, consultez [créer un modèle d’objet XPS vide](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="64fd7-117">For more information about creating a blank XPS OM, refer to [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


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



### <a name="load-and-create-resources"></a><span data-ttu-id="64fd7-118">Charger et créer des ressources</span><span class="sxs-lookup"><span data-stu-id="64fd7-118">Load and create resources</span></span>

<span data-ttu-id="64fd7-119">La création d’une interface [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) nécessite une ressource de police.</span><span class="sxs-lookup"><span data-stu-id="64fd7-119">Creation of an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface requires a font resource.</span></span> <span data-ttu-id="64fd7-120">Dans de nombreux cas, un bloc de texte utilise la même police et la même couleur.</span><span class="sxs-lookup"><span data-stu-id="64fd7-120">In many cases, a block of text uses the same font and color.</span></span> <span data-ttu-id="64fd7-121">Par conséquent, cette section de l’exemple de code créera les interfaces de ressource de police qui seront utilisées dans les appels qui placent le texte sur la page.</span><span class="sxs-lookup"><span data-stu-id="64fd7-121">Hence, this section of the code example will create the font resource interfaces that will be used in the calls that place the text on the page.</span></span>


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



### <a name="draw-text-in-a-page"></a><span data-ttu-id="64fd7-122">Dessiner du texte dans une page</span><span class="sxs-lookup"><span data-stu-id="64fd7-122">Draw text in a page</span></span>

<span data-ttu-id="64fd7-123">La dernière section de l’exemple de code crée les exécutions de glyphes pour chaque exécution du texte mis en forme de la même façon.</span><span class="sxs-lookup"><span data-stu-id="64fd7-123">The final section of the code example creates the glyph runs for each run of similarly formatted text.</span></span> <span data-ttu-id="64fd7-124">Pour exécuter le code dans cette section finale, l’interface **xpsFactory** , ainsi que la ressource de police et un pinceau de couleur de texte sont nécessaires et doivent avoir été instanciés et initialisés.</span><span class="sxs-lookup"><span data-stu-id="64fd7-124">To execute the code in this final section, the **xpsFactory** interface as well as the font resource and a text color brush are necessary and must have been instantiated and initialized.</span></span> <span data-ttu-id="64fd7-125">Dans cet exemple, la fonction décrite dans la première section est utilisée pour créer les exécutions de glyphe et les ajouter à la page.</span><span class="sxs-lookup"><span data-stu-id="64fd7-125">In this example, the function described in the first section is used to create the glyph runs and to add them to the page.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="64fd7-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64fd7-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="64fd7-127">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="64fd7-127">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="64fd7-128">Naviguer dans le modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="64fd7-128">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="64fd7-129">Dessiner des graphiques dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="64fd7-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="64fd7-130">Placer des images dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="64fd7-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="64fd7-131">Écrire un modèle OM XPS dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="64fd7-131">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="64fd7-132">Imprimer un modèle OM XPS</span><span class="sxs-lookup"><span data-stu-id="64fd7-132">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="64fd7-133">**Utilisé dans cette section**</span><span class="sxs-lookup"><span data-stu-id="64fd7-133">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="64fd7-134">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="64fd7-134">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="64fd7-135">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="64fd7-135">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="64fd7-136">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="64fd7-136">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[<span data-ttu-id="64fd7-137">**IXpsOMGlyphsEditor**</span><span class="sxs-lookup"><span data-stu-id="64fd7-137">**IXpsOMGlyphsEditor**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[<span data-ttu-id="64fd7-138">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="64fd7-138">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="64fd7-139">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="64fd7-139">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="64fd7-140">**IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="64fd7-140">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="64fd7-141">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="64fd7-141">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="64fd7-142">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="64fd7-142">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="64fd7-143">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="64fd7-143">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="64fd7-144">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="64fd7-144">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="64fd7-145">Informations de référence sur l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="64fd7-145">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="64fd7-146">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="64fd7-146">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
