---
title: Mise en forme et disposition du texte
description: DirectWrite fournit deux interfaces pour mettre en forme le texte IDWriteTextFormat et IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, mise en forme du texte
- DirectWrite, disposition
- DirectWrite, interface IDWriteTextFormat
- DirectWrite, interface IDWriteTextLayout
- Interface IDWriteTextFormat
- Interface IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fcf884c15015af2645c32e217d3b4a6b433554
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199346"
---
# <a name="text-formatting-and-layout"></a><span data-ttu-id="6d9d9-109">Mise en forme et disposition du texte</span><span class="sxs-lookup"><span data-stu-id="6d9d9-109">Text Formatting and Layout</span></span>

<span data-ttu-id="6d9d9-110">[DirectWrite](direct-write-portal.md) fournit deux interfaces pour la mise en forme du texte : [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="6d9d9-110">[DirectWrite](direct-write-portal.md) provides two interfaces for formatting text: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="6d9d9-111">**IDWriteTextFormat** décrit uniquement le format du texte et est utilisé dans les cas où une chaîne entière doit avoir la même taille de police, le même style, le même poids, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-111">**IDWriteTextFormat** describes only the format for text and is used in cases when an entire string is to be the same font size, style, weight and so on.</span></span> <span data-ttu-id="6d9d9-112">En revanche, **IDWriteTextLayout** encapsule une chaîne de texte et la mise en forme des plages spécifiées de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-112">On the other hand, **IDWriteTextLayout** encapsulates both a text string and the formatting for specified ranges of the string.</span></span> <span data-ttu-id="6d9d9-113">Ce document décrit chaque interface et leurs utilisations.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-113">This document describes each interface and their uses.</span></span> <span data-ttu-id="6d9d9-114">Pour plus d’informations sur la création et les méthodes de ces interfaces, consultez les pages de référence [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6d9d9-114">For more information about the creation and methods of these interfaces, see the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference pages.</span></span>

<span data-ttu-id="6d9d9-115">Ce document contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6d9d9-115">This document contains the following parts:</span></span>

-   [<span data-ttu-id="6d9d9-116">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="6d9d9-116">IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
    -   [<span data-ttu-id="6d9d9-117">Modification d’un IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="6d9d9-117">Modifying an IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
-   [<span data-ttu-id="6d9d9-118">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="6d9d9-118">IDWriteTextLayout</span></span>](#idwritetextlayout)
    -   [<span data-ttu-id="6d9d9-119">Mise en forme d’une plage de texte</span><span class="sxs-lookup"><span data-stu-id="6d9d9-119">Formatting a range of text</span></span>](#formatting-a-range-of-text)
    -   [<span data-ttu-id="6d9d9-120">Options de rendu</span><span class="sxs-lookup"><span data-stu-id="6d9d9-120">Rendering Options</span></span>](#rendering-options)

## <a name="idwritetextformat"></a><span data-ttu-id="6d9d9-121">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="6d9d9-121">IDWriteTextFormat</span></span>

<span data-ttu-id="6d9d9-122">Un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) est utilisé pour :</span><span class="sxs-lookup"><span data-stu-id="6d9d9-122">An [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object is used to:</span></span>

-   <span data-ttu-id="6d9d9-123">Décrit le format d’une chaîne entière lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-123">Describe the format for an entire string when rendering.</span></span> <span data-ttu-id="6d9d9-124">Pour restituer une chaîne avec plusieurs formats, utilisez un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6d9d9-124">To render a string with multiple formats, use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>
-   <span data-ttu-id="6d9d9-125">Spécifiez le format de texte par défaut lors de la création d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6d9d9-125">Specify the default text format when creating an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="6d9d9-126">Pour créer un objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , utilisez la méthode [**IDWriteFactory :: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) et spécifiez la famille de polices, la collection de polices, l’épaisseur de police, la taille de police (DIP), le nom des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-126">To create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, you use the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method and specify the font family, font collection, font weight, font size (in DIPs), locale name.</span></span>

### <a name="modifying-an-idwritetextformat"></a><span data-ttu-id="6d9d9-127">Modification d’un IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="6d9d9-127">Modifying an IDWriteTextFormat</span></span>

<span data-ttu-id="6d9d9-128">Une fois qu’une interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) est créée, certaines valeurs ne peuvent pas être modifiées : la famille de polices, la collection, le poids et la taille, ainsi que le nom des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-128">Once an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is created, some values cannot be changed: the font family, collection, weight, and size, as well the locale name.</span></span> <span data-ttu-id="6d9d9-129">Pour modifier ces valeurs, vous devez créer un nouvel objet **IDWriteTextFormat** .</span><span class="sxs-lookup"><span data-stu-id="6d9d9-129">To change these values, a new **IDWriteTextFormat** object must be created.</span></span>

<span data-ttu-id="6d9d9-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) vous permet de modifier les propriétés ci-dessus sans recréer d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) enables you to change the properties above without recreating anthing.</span></span> <span data-ttu-id="6d9d9-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) vous permet d’apporter des modifications de format qui s’appliquent à l’intégralité du texte, par exemple l’alignement du texte.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) enables you to make format changes that apply to the entire text, such as text alignment.</span></span> <span data-ttu-id="6d9d9-132">Si vous souhaitez appliquer une mise en forme à des plages de caractères spécifiques, vous devez le faire à l’aide d’un **IDWriteTextLayout**.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-132">If you want to apply formatting to specific character ranges, you should do so by using a **IDWriteTextLayout**.</span></span>

<span data-ttu-id="6d9d9-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fournit des méthodes permettant de définir l’alignement du texte, le sens du déroulement, le taquet de tabulation incrémentiel, l’interligne, l’alignement des paragraphes, le rognage et le retour automatique à la ligne.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provides methods to set the text alignment, flow direction, incremental tab stop, line spacing, paragraph alignment, trimming, and word wrapping.</span></span> <span data-ttu-id="6d9d9-134">Ces propriétés peuvent être modifiées à tout moment après la création de l’objet **IDWriteTextFormat** .</span><span class="sxs-lookup"><span data-stu-id="6d9d9-134">These properties can be changed at any time after the creation of the **IDWriteTextFormat** object.</span></span>

## <a name="idwritetextlayout"></a><span data-ttu-id="6d9d9-135">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="6d9d9-135">IDWriteTextLayout</span></span>

<span data-ttu-id="6d9d9-136">L’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , contrairement à [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), représente à la fois un bloc de texte et la mise en forme associée.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-136">The [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface, unlike [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), represents both a block of text and the associated formatting.</span></span> <span data-ttu-id="6d9d9-137">**IDWriteTextFormat** représente les informations de mise en forme initiales.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-137">**IDWriteTextFormat** represents initial formatting information.</span></span> <span data-ttu-id="6d9d9-138">L’exemple suivant montre comment créer un objet **IDWriteTextLayout** à l’aide de [**IDWriteFactory :: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span><span class="sxs-lookup"><span data-stu-id="6d9d9-138">The following example shows how to create an **IDWriteTextLayout** object using [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span></span>


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



<span data-ttu-id="6d9d9-139">Le texte d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ne peut pas être modifié une fois que l’objet est créé.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-139">The text in an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object cannot be changed once the object is created.</span></span> <span data-ttu-id="6d9d9-140">Pour modifier le texte, vous devez supprimer l’objet existant et créer un nouvel objet **IDWriteTextLayout** .</span><span class="sxs-lookup"><span data-stu-id="6d9d9-140">To change the text you must delete the existing object and create a new **IDWriteTextLayout** object.</span></span>

<span data-ttu-id="6d9d9-141">Vous pouvez utiliser un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pour mettre en forme des plages de texte spécifiées.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-141">You can use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to format specified ranges of text.</span></span> <span data-ttu-id="6d9d9-142">**IDWriteTextLayout** fournit également des méthodes pour modifier le style et le poids de la police, et ajoute des fonctionnalités de police OpenType et un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-142">**IDWriteTextLayout** also provides methods for changing font style and weight, and adding OpenType font features and hit testing.</span></span> <span data-ttu-id="6d9d9-143">Pour plus d’informations et pour obtenir la liste complète des méthodes, consultez la page de référence [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6d9d9-143">For more information and a complete list of methods see the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference page.</span></span>

### <a name="formatting-a-range-of-text"></a><span data-ttu-id="6d9d9-144">Mise en forme d’une plage de texte</span><span class="sxs-lookup"><span data-stu-id="6d9d9-144">Formatting a range of text</span></span>

<span data-ttu-id="6d9d9-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) fournit plusieurs méthodes pour mettre en forme des plages de texte.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) provides several methods to format ranges of text.</span></span> <span data-ttu-id="6d9d9-146">Chacune de ces méthodes prend une structure de [**\_ \_ plage de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) comme paramètre pour spécifier la position du texte de départ dans la chaîne et la longueur de la plage à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-146">Each of these methods takes a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) structure as a parameter to specify the starting text position within the string and the length of the range to format.</span></span> <span data-ttu-id="6d9d9-147">L’exemple suivant montre comment affecter la valeur gras à l’épaisseur de la police d’une plage de texte.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-147">The following example shows how to set the font weight of a range of text to bold.</span></span>


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a><span data-ttu-id="6d9d9-148">Options de rendu</span><span class="sxs-lookup"><span data-stu-id="6d9d9-148">Rendering Options</span></span>

<span data-ttu-id="6d9d9-149">Le texte avec une mise en forme décrite par un seul objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) peut être rendu avec [Direct2D](../direct2d/direct2d-portal.md), toutefois, il existe quelques options supplémentaires pour le rendu d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6d9d9-149">Text with formatting described by only a [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="6d9d9-150">La chaîne décrite par un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) peut être rendue à l’aide des méthodes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6d9d9-150">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

1.  <span data-ttu-id="6d9d9-151">[Rendu à l’aide de Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="6d9d9-151">[Render using Direct2D](rendering-by-using-direct2d.md).</span></span>
2.  <span data-ttu-id="6d9d9-152">[Rendu à l’aide d’un convertisseur de texte personnalisé](how-to-implement-a-custom-text-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="6d9d9-152">[Render using a custom text renderer](how-to-implement-a-custom-text-renderer.md).</span></span>
3.  <span data-ttu-id="6d9d9-153">[Rendre sur une surface GDI](render-to-a-gdi-surface.md).</span><span class="sxs-lookup"><span data-stu-id="6d9d9-153">[Render to a GDI surface](render-to-a-gdi-surface.md).</span></span>

 

 