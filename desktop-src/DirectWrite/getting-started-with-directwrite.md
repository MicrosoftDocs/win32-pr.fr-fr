---
title: Didacticiel Prise en main avec DirectWrite
description: Ce document vous montre comment utiliser DirectWrite et Direct2D pour créer du texte simple contenant un seul format, puis du texte qui contient plusieurs formats.
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
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315863"
---
# <a name="tutorial-getting-started-with-directwrite"></a><span data-ttu-id="5846e-113">Didacticiel : Prise en main avec DirectWrite</span><span class="sxs-lookup"><span data-stu-id="5846e-113">Tutorial: Getting Started with DirectWrite</span></span>

<span data-ttu-id="5846e-114">Ce document vous montre comment utiliser [DirectWrite](direct-write-portal.md) et [Direct2D](rendering-by-using-direct2d.md) pour créer du texte simple contenant un seul format, puis du texte qui contient plusieurs formats.</span><span class="sxs-lookup"><span data-stu-id="5846e-114">This document shows you how to use [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to create simple text that contains a single format, and then text that contains multiple formats.</span></span>

<span data-ttu-id="5846e-115">Ce didacticiel contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5846e-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="5846e-116">Code source</span><span class="sxs-lookup"><span data-stu-id="5846e-116">Source Code</span></span>](#source-code)
-   [<span data-ttu-id="5846e-117">Dessiner du texte simple</span><span class="sxs-lookup"><span data-stu-id="5846e-117">Drawing Simple Text</span></span>](#drawing-simple-text)
    -   [<span data-ttu-id="5846e-118">Partie 1 : déclarer des ressources DirectWrite et Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5846e-118">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>](#part-1-declare-directwrite-and-direct2d-resources)
    -   [<span data-ttu-id="5846e-119">Partie 2 : créer des ressources indépendantes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5846e-119">Part 2: Create Device Independent Resources.</span></span>](#part-2-create-device-independent-resources)
    -   [<span data-ttu-id="5846e-120">Partie 3 : créer des ressources Device-Dependent.</span><span class="sxs-lookup"><span data-stu-id="5846e-120">Part 3: Create Device-Dependent Resources.</span></span>](#part-3-create-device-dependent-resources)
    -   [<span data-ttu-id="5846e-121">Partie 4 : dessiner du texte à l’aide de la méthode DrawText de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5846e-121">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [<span data-ttu-id="5846e-122">Partie 5 : rendu du contenu de la fenêtre à l’aide de Direct2D</span><span class="sxs-lookup"><span data-stu-id="5846e-122">Part 5: Render the Window Contents Using Direct2D</span></span>](#part-5-render-the-window-contents-using-direct2d)
-   [<span data-ttu-id="5846e-123">Dessin de texte avec plusieurs formats.</span><span class="sxs-lookup"><span data-stu-id="5846e-123">Drawing Text with Multiple Formats.</span></span>](#drawing-text-with-multiple-formats)
    -   [<span data-ttu-id="5846e-124">Partie 1 : créer une interface IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="5846e-124">Part 1: Create an IDWriteTextLayout Interface.</span></span>](#part-1-create-an-idwritetextlayout-interface)
    -   [<span data-ttu-id="5846e-125">Partie 2 : application de la mise en forme avec IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="5846e-125">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>](#part-2-applying-formatting-with-idwritetextlayout)
    -   [<span data-ttu-id="5846e-126">Partie 3 : ajout de fonctionnalités typographiques avec IDWriteTypography.</span><span class="sxs-lookup"><span data-stu-id="5846e-126">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>](#part-3-adding-typographic-features-with-idwritetypography)
    -   [<span data-ttu-id="5846e-127">Partie 4 : dessiner du texte à l’aide de la méthode Direct2D DrawTextLayout.</span><span class="sxs-lookup"><span data-stu-id="5846e-127">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a><span data-ttu-id="5846e-128">Code source</span><span class="sxs-lookup"><span data-stu-id="5846e-128">Source Code</span></span>

<span data-ttu-id="5846e-129">Le code source présenté dans cette vue d’ensemble est extrait de l' [exemple de Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="5846e-129">The source code shown in this overview is taken from the [DirectWrite Hello World sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="5846e-130">Chaque partie est implémentée dans une classe distincte (SimpleText et MultiformattedText) et s’affiche dans une fenêtre enfant distincte.</span><span class="sxs-lookup"><span data-stu-id="5846e-130">Each part is implemented in a separate class (SimpleText and MultiformattedText) and is displayed in a separate child window.</span></span> <span data-ttu-id="5846e-131">Chaque classe représente une fenêtre Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="5846e-131">Each class represents a Microsoft Win32 window.</span></span> <span data-ttu-id="5846e-132">En plus de la méthode *WndProc* , chaque classe contient les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5846e-132">In addition to the *WndProc* method, each class contains the following methods:</span></span>



| <span data-ttu-id="5846e-133">Fonction</span><span class="sxs-lookup"><span data-stu-id="5846e-133">Function</span></span>                              | <span data-ttu-id="5846e-134">Description</span><span class="sxs-lookup"><span data-stu-id="5846e-134">Description</span></span>                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5846e-135">**CreateDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="5846e-135">**CreateDeviceIndependentResources**</span></span>  | <span data-ttu-id="5846e-136">Crée des ressources indépendantes des appareils, afin qu’elles puissent être réutilisées n’importe où.</span><span class="sxs-lookup"><span data-stu-id="5846e-136">Creates resources that are device independent, so they can be reused anywhere.</span></span>                      |
| <span data-ttu-id="5846e-137">**DiscardDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="5846e-137">**DiscardDeviceIndependentResources**</span></span> | <span data-ttu-id="5846e-138">Libère les ressources indépendantes du périphérique une fois qu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="5846e-138">Releases the device-independent resources after they are no longer needed.</span></span>                          |
| <span data-ttu-id="5846e-139">**CreateDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="5846e-139">**CreateDeviceResources**</span></span>             | <span data-ttu-id="5846e-140">Crée des ressources, telles que des pinceaux et des cibles de rendu, qui sont liées à un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="5846e-140">Creates resources, such as brushes and render targets, that are tied to a particular device.</span></span>        |
| <span data-ttu-id="5846e-141">**DiscardDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="5846e-141">**DiscardDeviceResources**</span></span>            | <span data-ttu-id="5846e-142">Libère les ressources dépendantes de l’appareil une fois qu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="5846e-142">Releases the device-dependent resources after they are no longer needed.</span></span>                            |
| <span data-ttu-id="5846e-143">**DrawD2DContent**</span><span class="sxs-lookup"><span data-stu-id="5846e-143">**DrawD2DContent**</span></span>                    | <span data-ttu-id="5846e-144">Utilise [Direct2D](../direct2d/direct2d-portal.md) pour effectuer le rendu à l’écran.</span><span class="sxs-lookup"><span data-stu-id="5846e-144">Uses [Direct2D](../direct2d/direct2d-portal.md) to render to the screen.</span></span>                              |
| <span data-ttu-id="5846e-145">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="5846e-145">**DrawText**</span></span>                          | <span data-ttu-id="5846e-146">Dessine la chaîne de texte à l’aide de [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="5846e-146">Draws the text string by using [Direct2D](../direct2d/direct2d-portal.md).</span></span>                            |
| <span data-ttu-id="5846e-147">**OnResize**</span><span class="sxs-lookup"><span data-stu-id="5846e-147">**OnResize**</span></span>                          | <span data-ttu-id="5846e-148">Redimensionne la cible de rendu [Direct2D](../direct2d/direct2d-portal.md) lorsque la taille de la fenêtre est modifiée.</span><span class="sxs-lookup"><span data-stu-id="5846e-148">Resizes the [Direct2D](../direct2d/direct2d-portal.md) render target when the window size is changed.</span></span> |



 

<span data-ttu-id="5846e-149">Vous pouvez utiliser l’exemple fourni ou suivre les instructions qui suivent pour ajouter [DirectWrite](direct-write-portal.md) et [Direct2D](rendering-by-using-direct2d.md) à votre propre application Win32.</span><span class="sxs-lookup"><span data-stu-id="5846e-149">You can use the sample provided, or use the instructions that follow to add [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to your own Win32 application.</span></span> <span data-ttu-id="5846e-150">Pour plus d’informations sur l’exemple et les fichiers projet associés, consultez l' [exemple DirectWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="5846e-150">For more information about the sample and the associated project files, see the [DirectWriteHelloWorld sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="drawing-simple-text"></a><span data-ttu-id="5846e-151">Dessiner du texte simple</span><span class="sxs-lookup"><span data-stu-id="5846e-151">Drawing Simple Text</span></span>

<span data-ttu-id="5846e-152">Cette section montre comment utiliser [DirectWrite](direct-write-portal.md) et [Direct2D](../direct2d/direct2d-portal.md) pour afficher du texte simple avec un format unique, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="5846e-152">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render simple text that has a single format, as shown in the following screen shot.</span></span>

![capture d’écran de « Hello World using DirectWrite ! »](images/simplecropped.png)

<span data-ttu-id="5846e-155">Le fait de dessiner du texte simple à l’écran nécessite quatre composants :</span><span class="sxs-lookup"><span data-stu-id="5846e-155">Drawing simple text to the screen requires four components:</span></span>

-   <span data-ttu-id="5846e-156">Chaîne de caractères à afficher.</span><span class="sxs-lookup"><span data-stu-id="5846e-156">A character string to render.</span></span>
-   <span data-ttu-id="5846e-157">Une instance de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="5846e-157">An instance of [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span>
-   <span data-ttu-id="5846e-158">Dimensions de la zone devant contenir le texte.</span><span class="sxs-lookup"><span data-stu-id="5846e-158">The dimensions of the area to contain the text.</span></span>
-   <span data-ttu-id="5846e-159">Objet qui peut restituer le texte.</span><span class="sxs-lookup"><span data-stu-id="5846e-159">An object that can render the text.</span></span> <span data-ttu-id="5846e-160">Dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="5846e-160">In this tutorial.</span></span> <span data-ttu-id="5846e-161">vous utilisez une cible de rendu [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5846e-161">you use a [Direct2D](../direct2d/direct2d-portal.md) render target.</span></span>

<span data-ttu-id="5846e-162">L’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) décrit le nom, la taille, le poids, le style et l’étirement de la famille de polices utilisés pour mettre en forme le texte, et il décrit les informations relatives aux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="5846e-162">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface describes the font-family name, size, weight, style, and stretch used to format text, and it describes locale information.</span></span> <span data-ttu-id="5846e-163">**IDWriteTextFormat** définit également des méthodes pour définir et obtenir les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="5846e-163">**IDWriteTextFormat** also defines methods for setting and getting the following properties:</span></span>

-   <span data-ttu-id="5846e-164">Interligne.</span><span class="sxs-lookup"><span data-stu-id="5846e-164">The line spacing.</span></span>
-   <span data-ttu-id="5846e-165">Alignement du texte par rapport aux bords gauche et droit de la zone de disposition.</span><span class="sxs-lookup"><span data-stu-id="5846e-165">The text alignment relative to the left and right edges of the layout box.</span></span>
-   <span data-ttu-id="5846e-166">Alignement du paragraphe par rapport au haut et au bas de la zone de disposition.</span><span class="sxs-lookup"><span data-stu-id="5846e-166">The paragraph alignment relative to the top and bottom of the layout box.</span></span>
-   <span data-ttu-id="5846e-167">Sens de lecture.</span><span class="sxs-lookup"><span data-stu-id="5846e-167">The reading direction.</span></span>
-   <span data-ttu-id="5846e-168">Granularité de la suppression de texte pour le texte qui dépasse la zone de disposition.</span><span class="sxs-lookup"><span data-stu-id="5846e-168">The text trimming granularity for text that overflows the layout box.</span></span>
-   <span data-ttu-id="5846e-169">Taquet de tabulation incrémentiel.</span><span class="sxs-lookup"><span data-stu-id="5846e-169">The incremental tab stop.</span></span>
-   <span data-ttu-id="5846e-170">Sens du déroulement du paragraphe.</span><span class="sxs-lookup"><span data-stu-id="5846e-170">The paragraph flow direction.</span></span>

<span data-ttu-id="5846e-171">L’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) est requise pour dessiner du texte qui utilise les deux processus décrits dans ce document.</span><span class="sxs-lookup"><span data-stu-id="5846e-171">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is required for drawing text that uses both of the processes described in this document .</span></span>

<span data-ttu-id="5846e-172">Avant de pouvoir créer un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou tout autre objet [DirectWrite](direct-write-portal.md) , vous avez besoin d’une instance [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="5846e-172">Before you can create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, or any other [DirectWrite](direct-write-portal.md) object, you need an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) instance.</span></span> <span data-ttu-id="5846e-173">Vous utilisez un **IDWriteFactory** pour créer des instances **IDWriteTextFormat** et d’autres objets DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="5846e-173">You use an **IDWriteFactory** to create **IDWriteTextFormat** instances and other DirectWrite objects.</span></span> <span data-ttu-id="5846e-174">Pour obtenir une instance de fabrique, utilisez la fonction [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="5846e-174">To obtain a factory instance, use the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function.</span></span>

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a><span data-ttu-id="5846e-175">Partie 1 : déclarer des ressources DirectWrite et Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5846e-175">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>

<span data-ttu-id="5846e-176">Dans cette partie, vous déclarez les objets que vous utiliserez ultérieurement pour créer et afficher du texte sous la forme de membres de données privés de votre classe.</span><span class="sxs-lookup"><span data-stu-id="5846e-176">In this part, you declare the objects that you will use later for creating and displaying text as private data members of your class.</span></span> <span data-ttu-id="5846e-177">Toutes les interfaces, fonctions et types de données pour [DirectWrite](direct-write-portal.md) sont déclarés dans le fichier d’en-tête *DWrite. h* , et ceux de [Direct2D](../direct2d/direct2d-portal.md) sont déclarés dans *d2d1. h*. Si vous ne l’avez pas encore fait, incluez ces en-têtes dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="5846e-177">All of the interfaces, functions, and datatypes for [DirectWrite](direct-write-portal.md) are declared in the *dwrite.h* header file, and those for [Direct2D](../direct2d/direct2d-portal.md) are declared in the *d2d1.h*; if you haven't already done this, include these headers in your project.</span></span>

1.  <span data-ttu-id="5846e-178">Dans votre fichier d’en-tête de classe (SimpleText. h), déclarez des pointeurs vers des interfaces [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) et [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) en tant que membres privés.</span><span class="sxs-lookup"><span data-stu-id="5846e-178">In your class header file (SimpleText.h), declare pointers to [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interfaces as private members.</span></span>
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  <span data-ttu-id="5846e-179">Déclarez les membres pour contenir la chaîne de texte à restituer et la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5846e-179">Declare members to hold the text string to render and the length of the string.</span></span>
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  <span data-ttu-id="5846e-180">Déclarez des pointeurs vers des interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)et [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pour le rendu du texte avec [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="5846e-180">Declare pointers to [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), and [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces for rendering the text with [Direct2D](../direct2d/direct2d-portal.md).</span></span>
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a><span data-ttu-id="5846e-181">Partie 2 : créer des ressources indépendantes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5846e-181">Part 2: Create Device Independent Resources.</span></span>

<span data-ttu-id="5846e-182">[Direct2D](rendering-by-using-direct2d.md) fournit deux types de ressources : les ressources dépendantes de l’appareil et les ressources indépendantes du périphérique.</span><span class="sxs-lookup"><span data-stu-id="5846e-182">[Direct2D](rendering-by-using-direct2d.md) provides two types of resources: device-dependent resources and device-independent resources.</span></span> <span data-ttu-id="5846e-183">Les ressources dépendantes de l’appareil sont associées à un périphérique de rendu et ne fonctionnent plus si l’appareil est supprimé.</span><span class="sxs-lookup"><span data-stu-id="5846e-183">Device-dependent resources are associated with a rendering device and no longer function if that device is removed.</span></span> <span data-ttu-id="5846e-184">Les ressources indépendantes du périphérique, en revanche, peuvent être utilisées en dernier pour l’étendue de votre application.</span><span class="sxs-lookup"><span data-stu-id="5846e-184">Device-independent resources, on the other hand, can last for the scope of your application.</span></span>

<span data-ttu-id="5846e-185">Les ressources [DirectWrite](direct-write-portal.md) sont indépendantes des appareils.</span><span class="sxs-lookup"><span data-stu-id="5846e-185">[DirectWrite](direct-write-portal.md) resources are device-independent.</span></span>

<span data-ttu-id="5846e-186">Dans cette section, vous allez créer les ressources indépendantes du périphérique qui sont utilisées par votre application.</span><span class="sxs-lookup"><span data-stu-id="5846e-186">In this section, you create the device-independent resources that are used by your application.</span></span> <span data-ttu-id="5846e-187">Ces ressources doivent être libérées à l’aide d’un appel à la méthode **Release** de l’interface.</span><span class="sxs-lookup"><span data-stu-id="5846e-187">These resources must be freed with a call to the **Release** method of the interface.</span></span>

<span data-ttu-id="5846e-188">Certaines des ressources utilisées ne doivent être créées qu’une seule fois et ne sont pas liées à un appareil.</span><span class="sxs-lookup"><span data-stu-id="5846e-188">Some of the resources that are used have to be created only one time and are not tied to a device.</span></span> <span data-ttu-id="5846e-189">L’initialisation de ces ressources est placée dans la méthode *SimpleText :: CreateDeviceIndependentResources* , qui est appelée lors de l’initialisation de la classe.</span><span class="sxs-lookup"><span data-stu-id="5846e-189">The initialization for these resources is put in the *SimpleText::CreateDeviceIndependentResources* method, which is called when initializing the class.</span></span>

1.  <span data-ttu-id="5846e-190">À l’intérieur de la méthode *SimpleText :: CreateDeviceIndependentResources* dans le fichier d’implémentation de classe (SimpleText. cpp), appelez la fonction [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) pour créer une interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , qui est l’interface de fabrique racine pour tous les objets [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5846e-190">Inside the *SimpleText::CreateDeviceIndependentResources* method in the class implementation file (SimpleText.cpp), call the [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) function to create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface, which is the root factory interface for all [Direct2D](../direct2d/direct2d-portal.md) objects.</span></span> <span data-ttu-id="5846e-191">Vous utilisez la même fabrique pour instancier d’autres ressources Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5846e-191">You use the same factory to instantiate other Direct2D resources.</span></span>
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  <span data-ttu-id="5846e-192">Appelez la fonction [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) pour créer une interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , qui est l’interface de fabrique racine pour tous les objets [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5846e-192">Call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function to create an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface, which is the root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span> <span data-ttu-id="5846e-193">Vous utilisez la même fabrique pour instancier d’autres ressources DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="5846e-193">You use the same factory to instantiate other DirectWrite resources.</span></span>
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

    

3.  <span data-ttu-id="5846e-194">Initialisez la chaîne de texte et stockez sa longueur.</span><span class="sxs-lookup"><span data-stu-id="5846e-194">Initialize the text string and store its length.</span></span>

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  <span data-ttu-id="5846e-195">Créez un objet d’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) à l’aide de la méthode [**IDWriteFactory :: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) .</span><span class="sxs-lookup"><span data-stu-id="5846e-195">Create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface object by using the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method.</span></span> <span data-ttu-id="5846e-196">Le **IDWriteTextFormat** spécifie la police, le poids, l’étirement, le style et les paramètres régionaux qui seront utilisés pour le rendu de la chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="5846e-196">The **IDWriteTextFormat** specifies the font, weight, stretch, style, and locale that will be used to render the text string.</span></span>
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

    

5.  <span data-ttu-id="5846e-197">Centrez le texte horizontalement et verticalement en appelant les méthodes [**IDWriteTextFormat :: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) et [**IDWriteTextFormat :: SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) .</span><span class="sxs-lookup"><span data-stu-id="5846e-197">Center the text horizontally and vertically by calling the [**IDWriteTextFormat::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) and [**IDWriteTextFormat::SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) methods.</span></span>
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

    

<span data-ttu-id="5846e-198">Dans cette partie, vous avez initialisé les ressources indépendantes du périphérique qui sont utilisées par votre application.</span><span class="sxs-lookup"><span data-stu-id="5846e-198">In this part, you initialized the device-independent resources that are used by your application.</span></span> <span data-ttu-id="5846e-199">Dans la partie suivante, vous initialisez les ressources dépendantes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5846e-199">In the next part, you initialize the device-dependent resources.</span></span>

### <a name="part-3-create-device-dependent-resources"></a><span data-ttu-id="5846e-200">Partie 3 : créer des ressources Device-Dependent.</span><span class="sxs-lookup"><span data-stu-id="5846e-200">Part 3: Create Device-Dependent Resources.</span></span>

<span data-ttu-id="5846e-201">Dans cette partie, vous créez un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) et un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pour le rendu de votre texte.</span><span class="sxs-lookup"><span data-stu-id="5846e-201">In this part, you create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) for rendering your text.</span></span>

<span data-ttu-id="5846e-202">Une cible de rendu est un objet Direct2D qui crée des ressources de dessin et restitue des commandes de dessin sur un appareil de rendu.</span><span class="sxs-lookup"><span data-stu-id="5846e-202">A render target is a Direct2D object that creates drawing resources and renders drawing commands to a rendering device.</span></span> <span data-ttu-id="5846e-203">Un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) est une cible de rendu qui est restituée à un **HWND**.</span><span class="sxs-lookup"><span data-stu-id="5846e-203">An [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) is a render target that renders to an **HWND**.</span></span>

<span data-ttu-id="5846e-204">L’une des ressources de dessin qu’une cible de rendu peut créer est un pinceau pour peindre des contours, des remplissages et du texte.</span><span class="sxs-lookup"><span data-stu-id="5846e-204">One of the drawing resources that a render target can create is a brush for painting outlines, fills, and text.</span></span> <span data-ttu-id="5846e-205">Un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) peint avec une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="5846e-205">An [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints with a solid color.</span></span>

<span data-ttu-id="5846e-206">Les interfaces [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) et [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) sont liées à un appareil de rendu lorsqu’elles sont créées et doivent être libérées et recréées si l’appareil n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="5846e-206">Both the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces are bound to a rendering device when they are created and must be released and recreated if the device becomes invalid.</span></span>

1.  <span data-ttu-id="5846e-207">À l’intérieur de la méthode SimpleText :: CreateDeviceResources, vérifiez si le pointeur de la cible de rendu a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5846e-207">Inside the SimpleText::CreateDeviceResources method, check whether the render target pointer is **NULL**.</span></span> <span data-ttu-id="5846e-208">Si c’est le cas, récupérez la taille de la zone de rendu et créez un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) de cette taille.</span><span class="sxs-lookup"><span data-stu-id="5846e-208">If it is, retrieve the size of the render area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of that size.</span></span> <span data-ttu-id="5846e-209">Utilisez **ID2D1HwndRenderTarget** pour créer un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="5846e-209">Use the **ID2D1HwndRenderTarget** to create an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>
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

    

2.  <span data-ttu-id="5846e-210">Dans la méthode SimpleText ::D iscardDeviceResources, libérez à la fois le pinceau et la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="5846e-210">In the SimpleText::DiscardDeviceResources method, release both the brush and render target.</span></span>
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

<span data-ttu-id="5846e-211">Maintenant que vous avez créé une cible de rendu et un pinceau, vous pouvez les utiliser pour restituer votre texte.</span><span class="sxs-lookup"><span data-stu-id="5846e-211">Now that you have created a render target and a brush, you can use them to render your text.</span></span>

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a><span data-ttu-id="5846e-212">Partie 4 : dessiner du texte à l’aide de la méthode DrawText de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5846e-212">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>

1.  <span data-ttu-id="5846e-213">Dans la méthode SimpleText ::D rawText de votre classe, définissez la zone pour la disposition du texte en extrayant les dimensions de la zone de rendu et créez un rectangle [Direct2D](../direct2d/direct2d-portal.md) qui a les mêmes dimensions.</span><span class="sxs-lookup"><span data-stu-id="5846e-213">In the SimpleText::DrawText method of your class, define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="5846e-214">Utilisez la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) et l’objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pour afficher du texte à l’écran.</span><span class="sxs-lookup"><span data-stu-id="5846e-214">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="5846e-215">La méthode **ID2D1RenderTarget ::D rawtext** accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="5846e-215">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="5846e-216">Chaîne à restituer.</span><span class="sxs-lookup"><span data-stu-id="5846e-216">A string to render.</span></span>
    -   <span data-ttu-id="5846e-217">Pointeur vers une interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="5846e-217">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="5846e-218">Rectangle de disposition [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5846e-218">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="5846e-219">Pointeur vers une interface qui expose [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span><span class="sxs-lookup"><span data-stu-id="5846e-219">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a><span data-ttu-id="5846e-220">Partie 5 : rendu du contenu de la fenêtre à l’aide de Direct2D</span><span class="sxs-lookup"><span data-stu-id="5846e-220">Part 5: Render the Window Contents Using Direct2D</span></span>

<span data-ttu-id="5846e-221">Pour afficher le contenu de la fenêtre à l’aide de [Direct2D](../direct2d/direct2d-portal.md) lors de la réception d’un message de peinture, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5846e-221">To render the contents of the window by using [Direct2D](../direct2d/direct2d-portal.md) when a paint message is received, do the following:</span></span>

1.  <span data-ttu-id="5846e-222">Créez les ressources dépendantes de l’appareil en appelant la méthode SimpleText :: CreateDeviceResources implémentée dans la partie 3.</span><span class="sxs-lookup"><span data-stu-id="5846e-222">Create the device dependent resources by calling the SimpleText::CreateDeviceResources method implemented in Part 3.</span></span>
2.  <span data-ttu-id="5846e-223">Appelez la méthode [**ID2D1HwndRenderTarget :: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="5846e-223">Call the [**ID2D1HwndRenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method of the render target.</span></span>
3.  <span data-ttu-id="5846e-224">Effacez la cible de rendu en appelant la méthode [**ID2D1HwndRenderTarget :: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) .</span><span class="sxs-lookup"><span data-stu-id="5846e-224">Clear the render target by calling the [**ID2D1HwndRenderTarget::Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) method.</span></span>
4.  <span data-ttu-id="5846e-225">Appelez la méthode SimpleText ::D rawText, implémentée dans la partie 4.</span><span class="sxs-lookup"><span data-stu-id="5846e-225">Call the SimpleText::DrawText method, implemented in Part 4.</span></span>
5.  <span data-ttu-id="5846e-226">Appelez la méthode [**ID2D1HwndRenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="5846e-226">Call the [**ID2D1HwndRenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method of the render target.</span></span>
6.  <span data-ttu-id="5846e-227">Si nécessaire, ignorez les ressources dépendantes de l’appareil afin qu’elles puissent être recréées lorsque la fenêtre est redessinée.</span><span class="sxs-lookup"><span data-stu-id="5846e-227">If it is necessary, discard the device-dependent resources so that they can be recreated when the window is redrawn.</span></span>


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



<span data-ttu-id="5846e-228">La classe SimpleText est implémentée dans SimpleText. h et SimpleText. cpp.</span><span class="sxs-lookup"><span data-stu-id="5846e-228">The SimpleText class is implemented in SimpleText.h and SimpleText.cpp.</span></span>

## <a name="drawing-text-with-multiple-formats"></a><span data-ttu-id="5846e-229">Dessin de texte avec plusieurs formats.</span><span class="sxs-lookup"><span data-stu-id="5846e-229">Drawing Text with Multiple Formats.</span></span>

<span data-ttu-id="5846e-230">Cette section montre comment utiliser [DirectWrite](direct-write-portal.md) et [Direct2D](../direct2d/direct2d-portal.md) pour restituer du texte avec plusieurs formats, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="5846e-230">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render text with multiple formats, as shown in the following screen shot.</span></span>

![capture d’écran de « Hello World using DirectWrite ! », avec certaines parties dans différents styles, tailles et formats](images/multiformattedcropped.png)

<span data-ttu-id="5846e-232">Le code de cette section est implémenté en tant que classe MultiformattedText dans l' [exemple DWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="5846e-232">The code for this section is implemented as the MultiformattedText class in the [DWriteHelloWorld Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="5846e-233">Elle est basée sur les étapes de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5846e-233">It is based on the steps from the previous section.</span></span>

<span data-ttu-id="5846e-234">Pour créer du texte à plusieurs mises en forme, vous utilisez l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en plus de l’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) introduite dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5846e-234">To create multi-formatted text, you use the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface in addition to the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface introduced in the previous section.</span></span> <span data-ttu-id="5846e-235">L’interface **IDWriteTextLayout** décrit la mise en forme et la mise en page d’un bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="5846e-235">The **IDWriteTextLayout** interface describes the formatting and layout of a block of text.</span></span> <span data-ttu-id="5846e-236">En plus de la mise en forme par défaut spécifiée par un objet **IDWriteTextFormat** , la mise en forme de plages de texte spécifiques peut être modifiée à l’aide de **IDWriteTextLayout**.</span><span class="sxs-lookup"><span data-stu-id="5846e-236">In addition to default formatting specified by an **IDWriteTextFormat** object, the formatting for specific ranges of text can be changed by using **IDWriteTextLayout**.</span></span> <span data-ttu-id="5846e-237">Cela comprend le nom de famille de polices, la taille, le poids, le style, l’étirement, le barré et le soulignement.</span><span class="sxs-lookup"><span data-stu-id="5846e-237">This includes font family name, size, weight, style, stretch, strikethrough, and underlining.</span></span>

<span data-ttu-id="5846e-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) fournit également des méthodes de test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="5846e-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) also provides hit-testing methods.</span></span> <span data-ttu-id="5846e-239">Les métriques de test de positionnement retournées par ces méthodes sont relatives à la zone de disposition spécifiée lors de la création de l’objet d’interface **IDWriteTextLayout** à l’aide de la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) de l’interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="5846e-239">The hit-testing metrics returned by these methods are relative to the layout box specified when the **IDWriteTextLayout** interface object is created by using the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="5846e-240">L’interface [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) est utilisée pour ajouter des fonctionnalités typographiques [OpenType](../intl/opentype-font-format.md) facultatives à une disposition de texte, telles que des lettres ornées et des ensembles de texte stylistiques alternatifs.</span><span class="sxs-lookup"><span data-stu-id="5846e-240">The [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface is used to add optional [OpenType](../intl/opentype-font-format.md) typographic features to a text layout, such as swashes and alternative stylistic text sets.</span></span> <span data-ttu-id="5846e-241">Les fonctionnalités typographiques peuvent être ajoutées à une plage de texte spécifique dans une disposition de texte en appelant la méthode [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) de l’interface **IDWriteTypography** .</span><span class="sxs-lookup"><span data-stu-id="5846e-241">Typographic features can be added to a specific range of text within a text layout by calling the [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method of the **IDWriteTypography** interface.</span></span> <span data-ttu-id="5846e-242">Cette méthode reçoit une structure de [**\_ \_ fonctionnalité de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) en tant que paramètre qui contient une constante d’énumération de **\_ \_ \_ balise de fonctionnalité de police DWRITE** et un paramètre d’exécution **UInt32** .</span><span class="sxs-lookup"><span data-stu-id="5846e-242">This method receives a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) structure as a parameter that contains a **DWRITE\_FONT\_FEATURE\_TAG** enumeration constant and a **UINT32** execution parameter.</span></span> <span data-ttu-id="5846e-243">Vous trouverez une liste des fonctionnalités OpenType inscrites dans le [Registre de balises de disposition OpenType](https://www.microsoft.com/typography/otspec/features_ae.htm) sur Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5846e-243">A list of registered OpenType features can be found at the [OpenType Layout Tag Registry](https://www.microsoft.com/typography/otspec/features_ae.htm) on microsoft.com.</span></span> <span data-ttu-id="5846e-244">Pour obtenir les constantes d’énumération DirectWrite équivalentes, consultez **\_ \_ \_ balise de fonctionnalité de police DWRITE**.</span><span class="sxs-lookup"><span data-stu-id="5846e-244">For the equivalent DirectWrite enumeration constants, see **DWRITE\_FONT\_FEATURE\_TAG**.</span></span>

### <a name="part-1-create-an-idwritetextlayout-interface"></a><span data-ttu-id="5846e-245">Partie 1 : créer une interface IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="5846e-245">Part 1: Create an IDWriteTextLayout Interface.</span></span>

1.  <span data-ttu-id="5846e-246">Déclarez un pointeur vers une interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en tant que membre de la classe MultiformattedText.</span><span class="sxs-lookup"><span data-stu-id="5846e-246">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the MultiformattedText class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="5846e-247">À la fin de la méthode MultiformattedText :: CreateDeviceIndependentResources, créez un objet d’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en appelant la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5846e-247">At the end of the MultiformattedText::CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span> <span data-ttu-id="5846e-248">L’interface **IDWriteTextLayout** fournit des fonctionnalités de mise en forme supplémentaires, telles que la possibilité d’appliquer des formats différents aux portions de texte sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="5846e-248">The **IDWriteTextLayout** interface provides additional formatting features, such as the ability to apply different formats to selected portions of text.</span></span>
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

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a><span data-ttu-id="5846e-249">Partie 2 : application de la mise en forme avec IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="5846e-249">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>

<span data-ttu-id="5846e-250">La mise en forme, telle que la taille de la police, le poids et le soulignement, peut être appliquée aux sous-chaînes du texte à afficher à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5846e-250">Formatting, such as the font size, weight, and underlining, can be applied to substrings of the text to be displayed by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

1.  <span data-ttu-id="5846e-251">Définissez la taille de police de la sous-chaîne « di » de « DirectWrite » sur 100 en déclarant [**une \_ \_ plage de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) et en appelant la méthode [**IDWriteTextLayout :: SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) .</span><span class="sxs-lookup"><span data-stu-id="5846e-251">Set the font size for the substring "Di" of "DirectWrite" to 100 by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) and calling the [**IDWriteTextLayout::SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) method.</span></span>
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  <span data-ttu-id="5846e-252">Soulignez la sous-chaîne « DirectWrite » en appelant la méthode [**IDWriteTextLayout :: SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .</span><span class="sxs-lookup"><span data-stu-id="5846e-252">Underline the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  <span data-ttu-id="5846e-253">Affectez la valeur gras à l’épaisseur de la police pour la sous-chaîne « DirectWrite » en appelant la méthode [**IDWriteTextLayout :: SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) .</span><span class="sxs-lookup"><span data-stu-id="5846e-253">Set the font weight to bold for the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) method.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a><span data-ttu-id="5846e-254">Partie 3 : ajout de fonctionnalités typographiques avec IDWriteTypography.</span><span class="sxs-lookup"><span data-stu-id="5846e-254">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>

1.  <span data-ttu-id="5846e-255">Déclarez et créez un objet d’interface [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) en appelant la méthode [**IDWriteFactory :: CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) .</span><span class="sxs-lookup"><span data-stu-id="5846e-255">Declare and create an [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface object by calling the [**IDWriteFactory::CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) method.</span></span>
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  <span data-ttu-id="5846e-256">Ajoutez une fonctionnalité de police en déclarant un objet de [**\_ \_ fonctionnalité de police DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) dont le jeu stylistique 7 est spécifié et en appelant la méthode [**IDWriteTypography :: AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) .</span><span class="sxs-lookup"><span data-stu-id="5846e-256">Add a font feature by declaring a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) object that has the stylistic set 7 specified and calling the [**IDWriteTypography::AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method.</span></span>
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  <span data-ttu-id="5846e-257">Définissez la disposition du texte pour utiliser la typographie sur l’ensemble de la chaîne en déclarant une variable de [**\_ \_ portée de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) et en appelant la méthode [**IDWriteTextLayout :: SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) et en passant dans la plage de texte.</span><span class="sxs-lookup"><span data-stu-id="5846e-257">Set the text layout to use the typography over the whole string by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable and calling the [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) method and passing in the text range.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  <span data-ttu-id="5846e-258">Définissez la nouvelle largeur et la hauteur de l’objet de disposition du texte dans la méthode MultiformattedText :: OnResize.</span><span class="sxs-lookup"><span data-stu-id="5846e-258">Set the new width and height for the text layout object in the MultiformattedText::OnResize method.</span></span>
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a><span data-ttu-id="5846e-259">Partie 4 : dessiner du texte à l’aide de la méthode Direct2D DrawTextLayout.</span><span class="sxs-lookup"><span data-stu-id="5846e-259">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>

<span data-ttu-id="5846e-260">Pour dessiner le texte avec les paramètres de disposition du texte spécifiés par l’objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , modifiez le code de la méthode MultiformattedText ::D rawtext de sorte qu’il utilise [**IDWriteTextLayout ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span><span class="sxs-lookup"><span data-stu-id="5846e-260">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="5846e-261">Delcare une variable [**d2d1 \_ point \_ 2F**](../direct2d/d2d1-point-2f.md) et définissez-la sur le point supérieur gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5846e-261">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="5846e-262">Dessinez le texte à l’écran en appelant la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) de la cible de rendu [Direct2D](../direct2d/direct2d-portal.md) et en passant le pointeur [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5846e-262">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

<span data-ttu-id="5846e-263">La classe MultiformattedText est implémentée dans MultiformattedText. h et MultiformattedText. cpp.</span><span class="sxs-lookup"><span data-stu-id="5846e-263">The MultiformattedText class is implemented in MultiformattedText.h and MultiformattedText.cpp.</span></span>

 

 