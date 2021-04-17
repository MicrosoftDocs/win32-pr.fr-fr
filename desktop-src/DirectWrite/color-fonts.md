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
# <a name="color-fonts"></a><span data-ttu-id="f218b-103">Polices de couleur</span><span class="sxs-lookup"><span data-stu-id="f218b-103">Color Fonts</span></span>

<span data-ttu-id="f218b-104">Cette rubrique décrit les polices de couleur, leur prise en charge dans DirectWrite et Direct2D, et comment les utiliser dans votre application.</span><span class="sxs-lookup"><span data-stu-id="f218b-104">This topic describes color fonts, their support in DirectWrite and Direct2D, and how to use them in your app.</span></span>

<span data-ttu-id="f218b-105">Ce document contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f218b-105">This document contains the following parts:</span></span>

-   [<span data-ttu-id="f218b-106">Que sont les polices de couleur ?</span><span class="sxs-lookup"><span data-stu-id="f218b-106">What are color fonts?</span></span>](#what-are-color-fonts)
-   [<span data-ttu-id="f218b-107">Pourquoi utiliser des polices de couleur ?</span><span class="sxs-lookup"><span data-stu-id="f218b-107">Why use color fonts?</span></span>](#why-use-color-fonts)
-   [<span data-ttu-id="f218b-108">Quels types de polices de couleurs Windows prend-il en charge ?</span><span class="sxs-lookup"><span data-stu-id="f218b-108">What kinds of color fonts does Windows support?</span></span>](#what-kinds-of-color-fonts-does-windows-support)
-   [<span data-ttu-id="f218b-109">Utilisation des polices de couleur</span><span class="sxs-lookup"><span data-stu-id="f218b-109">Using color fonts</span></span>](#using-color-fonts)
    -   [<span data-ttu-id="f218b-110">Utilisation des polices de couleur dans une application XAML</span><span class="sxs-lookup"><span data-stu-id="f218b-110">Using color fonts in a XAML app</span></span>](#using-color-fonts-in-a-xaml-app)
    -   [<span data-ttu-id="f218b-111">Utilisation des polices de couleur dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f218b-111">Using color fonts in Microsoft Edge</span></span>](#using-color-fonts-in-microsoft-edge)
    -   [<span data-ttu-id="f218b-112">Utilisation des polices de couleur avec DirectWrite et Direct2D</span><span class="sxs-lookup"><span data-stu-id="f218b-112">Using color fonts with DirectWrite and Direct2D</span></span>](#using-color-fonts-with-directwrite-and-direct2d)
    -   [<span data-ttu-id="f218b-113">Utilisation des polices de couleur avec Win2D</span><span class="sxs-lookup"><span data-stu-id="f218b-113">Using color fonts with Win2D</span></span>](#using-color-fonts-with-win2d)
-   [<span data-ttu-id="f218b-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f218b-114">Related topics</span></span>](#related-topics)

## <a name="what-are-color-fonts"></a><span data-ttu-id="f218b-115">Que sont les polices de couleur ?</span><span class="sxs-lookup"><span data-stu-id="f218b-115">What are color fonts?</span></span>

<span data-ttu-id="f218b-116">Les polices de couleur, également appelées polices multicolores ou polices chromatiques, sont une technologie de police qui permet aux concepteurs de polices d’utiliser plusieurs couleurs dans chaque glyphe.</span><span class="sxs-lookup"><span data-stu-id="f218b-116">Color fonts, also referred to as  multicolored fonts  or  chromatic fonts,  are a font technology that allows font designers to use multiple colors within each glyph.</span></span> <span data-ttu-id="f218b-117">Les polices de couleur activent les scénarios de texte multicolore dans les applications et les sites Web avec moins de code et une prise en charge de système d’exploitation plus robuste que les techniques ad hoc implémentées au-dessus du système de rendu de texte.</span><span class="sxs-lookup"><span data-stu-id="f218b-117">Color fonts enable multicolored text scenarios in apps and websites with less code and more robust operating system support than ad-hoc techniques implemented above the text rendering system.</span></span>

<span data-ttu-id="f218b-118">Les polices que vous connaissez sans doute ne sont pas des polices de couleurs.</span><span class="sxs-lookup"><span data-stu-id="f218b-118">The fonts you are probably most familiar with are not color fonts.</span></span> <span data-ttu-id="f218b-119">Ces polices définissent uniquement la forme des glyphes qu’elles contiennent, soit avec des contours vectoriels, soit avec des images bitmap monochromatiques.</span><span class="sxs-lookup"><span data-stu-id="f218b-119">These fonts define only the shape of the glyphs they contain, either with vector outlines or monochromatic bitmaps.</span></span> <span data-ttu-id="f218b-120">Au moment du tracé, un convertisseur de texte remplit la forme de glyphe à l’aide d’une couleur unique (la couleur de police) spécifiée par l’application ou le document en cours de rendu.</span><span class="sxs-lookup"><span data-stu-id="f218b-120">At draw time, a text renderer fills the glyph shape using a single color (the  font color ) specified by the app or document being rendered.</span></span> <span data-ttu-id="f218b-121">Les polices de couleur, quant à elles, contiennent des informations de couleur en plus des informations de forme.</span><span class="sxs-lookup"><span data-stu-id="f218b-121">Color fonts, on the other hand, contain color information in addition to shape information.</span></span> <span data-ttu-id="f218b-122">Certaines approches permettent aux concepteurs de polices d’offrir plusieurs palettes de couleurs, ce qui donne la flexibilité de la police de couleur artistique.</span><span class="sxs-lookup"><span data-stu-id="f218b-122">Some approaches allow font designers to offer multiple color palettes, giving the color font artistic flexibility.</span></span>

<span data-ttu-id="f218b-123">L’exemple suivant montre un glyphe issu de la police de couleur Segoe UI Emoji.</span><span class="sxs-lookup"><span data-stu-id="f218b-123">The following example shows a glyph from the Segoe UI Emoji color font.</span></span> <span data-ttu-id="f218b-124">Le glyphe est rendu en monochrome à gauche et dans la couleur à droite.</span><span class="sxs-lookup"><span data-stu-id="f218b-124">The glyph is rendered in monochrome on the left, and in color on the right.</span></span>

![Affiche des glyphes côte à côte, le glyphe gauche rendu en monochrome, le droit dans la police de couleur d’Emoji Segoe U I.](images/color-font-cat.png)

<span data-ttu-id="f218b-126">Les polices de couleur incluent généralement des informations de secours pour les plateformes qui ne prennent pas en charge les polices de couleur ou pour les scénarios dans lesquels la fonctionnalité de couleur a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="f218b-126">Color fonts typically include fallback information for platforms that do not support color fonts or for scenarios in which color functionality has been disabled.</span></span> <span data-ttu-id="f218b-127">Sur ces plateformes, les polices de couleur sont rendues en tant que polices monochromatiques standard.</span><span class="sxs-lookup"><span data-stu-id="f218b-127">On those platforms, color fonts are rendered as regular monochromatic fonts.</span></span>

## <a name="why-use-color-fonts"></a><span data-ttu-id="f218b-128">Pourquoi utiliser des polices de couleur ?</span><span class="sxs-lookup"><span data-stu-id="f218b-128">Why use color fonts?</span></span>

<span data-ttu-id="f218b-129">Historiquement, les concepteurs et les développeurs ont utilisé diverses techniques pour obtenir du texte multicolore.</span><span class="sxs-lookup"><span data-stu-id="f218b-129">Historically, designers and developers have used a variety of techniques to achieve multicolored text.</span></span> <span data-ttu-id="f218b-130">Par exemple, les sites Web utilisent souvent des images raster au lieu de texte pour afficher des en-têtes enrichis.</span><span class="sxs-lookup"><span data-stu-id="f218b-130">For example, websites often use raster images instead of text in order to display rich headers.</span></span> <span data-ttu-id="f218b-131">Cette approche permet une flexibilité artistique, mais les graphiques raster ne sont pas adaptés à toutes les tailles d’affichage et ne fournissent pas les mêmes fonctionnalités d’accessibilité que le texte réel.</span><span class="sxs-lookup"><span data-stu-id="f218b-131">This approach enables artistic flexibility, but raster graphics do not scale well to all display sizes, nor do they provide the same accessibility features as real text.</span></span> <span data-ttu-id="f218b-132">Une autre technique courante consiste à superposer plusieurs polices monochromatiques dans différentes couleurs de police, mais cela nécessite généralement un code de disposition supplémentaire à gérer.</span><span class="sxs-lookup"><span data-stu-id="f218b-132">Another common technique is to overlay multiple monochromatic fonts in different font colors, but this typically requires extra layout code to manage.</span></span>

<span data-ttu-id="f218b-133">Les polices de couleur offrent un moyen d’obtenir ces effets visuels avec toute la simplicité et les fonctionnalités des polices standard.</span><span class="sxs-lookup"><span data-stu-id="f218b-133">Color fonts offer a way to achieve these visual effects with all the simplicity and functionality of regular fonts.</span></span> <span data-ttu-id="f218b-134">Le texte affiché dans une police de couleur est identique à un autre texte : il peut être copié et collé, il peut être analysé par les outils d’accessibilité, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f218b-134">Text rendered in a color font is the same as other text: it can be copied and pasted, it can be parsed by accessibility tools, and so forth.</span></span>

## <a name="what-kinds-of-color-fonts-does-windows-support"></a><span data-ttu-id="f218b-135">Quels types de polices de couleurs Windows prend-il en charge ?</span><span class="sxs-lookup"><span data-stu-id="f218b-135">What kinds of color fonts does Windows support?</span></span>

<span data-ttu-id="f218b-136">La [spécification OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) définit plusieurs manières d’incorporer des informations de couleur dans une police.</span><span class="sxs-lookup"><span data-stu-id="f218b-136">The [OpenType specification](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) defines several ways to embed color information in a font.</span></span> <span data-ttu-id="f218b-137">À compter de la mise à jour anniversaire de Windows 10, DirectWrite et Direct2D (et les infrastructures Windows qui s’y basent) prennent en charge toutes ces approches.</span><span class="sxs-lookup"><span data-stu-id="f218b-137">Starting in Windows 10 Anniversary Update, DirectWrite and Direct2D (and the Windows frameworks built on them) support all of these approaches.</span></span> <span data-ttu-id="f218b-138">Elles sont résumées dans le tableau ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f218b-138">They are summarized in the table below:</span></span>



| <span data-ttu-id="f218b-139">Technique</span><span class="sxs-lookup"><span data-stu-id="f218b-139">Technique</span></span>                                                                                                                        | <span data-ttu-id="f218b-140">Description</span><span class="sxs-lookup"><span data-stu-id="f218b-140">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f218b-141">[Colr](/typography/opentype/spec/colr) / Tables [CPAL](/typography/opentype/spec/cpal)</span><span class="sxs-lookup"><span data-stu-id="f218b-141">[COLR](/typography/opentype/spec/colr)/[CPAL](/typography/opentype/spec/cpal) tables</span></span> | <span data-ttu-id="f218b-142">Utilise des couches de vecteurs de couleur, dont les formes sont définies de la même façon que les contours de glyphe de couleur unique.</span><span class="sxs-lookup"><span data-stu-id="f218b-142">Uses layers of colored vectors, whose shapes are defined in the same way as single-color glyph outlines.</span></span> <span data-ttu-id="f218b-143">**Remarque :** Prise en charge à partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="f218b-143">**Note:** Supported starting in Windows 8.1.</span></span> <br/>                                                                                                                                                 |
| <span data-ttu-id="f218b-144">Table [SVG](/typography/opentype/spec/svg)</span><span class="sxs-lookup"><span data-stu-id="f218b-144">[SVG](/typography/opentype/spec/svg) table</span></span>                                                                 | <span data-ttu-id="f218b-145">Utilise des images vectorielles créées dans le format graphique vectoriel Scalable.</span><span class="sxs-lookup"><span data-stu-id="f218b-145">Uses vector images authored in the Scalable Vector Graphics format.</span></span> <span data-ttu-id="f218b-146">**Remarque :** À compter de la mise à jour anniversaire de Windows 10, DirectWrite prend en charge un sous-ensemble de la spécification SVG complète. Le rendu de tout le contenu SVG n’est pas garanti dans une police OpenType SVG.</span><span class="sxs-lookup"><span data-stu-id="f218b-146">**Note:** As of Windows 10 Anniversary Update, DirectWrite supports a subset of the full SVG spec. Not all SVG content is guaranteed to render in an OpenType SVG font.</span></span> <span data-ttu-id="f218b-147">Pour plus d’informations, consultez [prise en charge SVG](../direct2d/svg-support.md) .</span><span class="sxs-lookup"><span data-stu-id="f218b-147">See [SVG Support](../direct2d/svg-support.md) for more details.</span></span> <br/> |
| <span data-ttu-id="f218b-148">[CBDT](/typography/opentype/spec/cbdt) / Tables [CBLC](/typography/opentype/spec/cblc)</span><span class="sxs-lookup"><span data-stu-id="f218b-148">[CBDT](/typography/opentype/spec/cbdt)/[CBLC](/typography/opentype/spec/cblc) tables</span></span> | <span data-ttu-id="f218b-149">Utilise des images bitmap de couleur incorporées.</span><span class="sxs-lookup"><span data-stu-id="f218b-149">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f218b-150">table [sbix](/typography/opentype/spec/sbix)</span><span class="sxs-lookup"><span data-stu-id="f218b-150">[sbix](/typography/opentype/spec/sbix) table</span></span>                                                               | <span data-ttu-id="f218b-151">Utilise des images bitmap de couleur incorporées.</span><span class="sxs-lookup"><span data-stu-id="f218b-151">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a><span data-ttu-id="f218b-152">Utilisation des polices de couleur</span><span class="sxs-lookup"><span data-stu-id="f218b-152">Using color fonts</span></span>

<span data-ttu-id="f218b-153">Du point de vue des utilisateurs, les polices de couleur sont simplement des polices.</span><span class="sxs-lookup"><span data-stu-id="f218b-153">From the user s perspective, color fonts are  just fonts .</span></span> <span data-ttu-id="f218b-154">Par exemple, ils peuvent généralement être installés et désinstallés du système de la même façon que les polices monochromatiques, et ils sont rendus sous forme de texte normal et sélectionnable.</span><span class="sxs-lookup"><span data-stu-id="f218b-154">For example, they can usually be installed and uninstalled from the system in the same way as monochromatic fonts, and they are rendered as regular, selectable text.</span></span>

<span data-ttu-id="f218b-155">Du point de vue du développeur, les polices de couleur sont généralement utilisées de la même façon que les polices monochromatiques.</span><span class="sxs-lookup"><span data-stu-id="f218b-155">From the developer s perspective too, color fonts are usually used the same way as monochromatic fonts.</span></span> <span data-ttu-id="f218b-156">Dans les infrastructures XAML et Microsoft Edge, vous pouvez définir le style de votre texte avec les polices de couleur de la même façon que les polices standard, et par défaut, votre texte est rendu en couleur.</span><span class="sxs-lookup"><span data-stu-id="f218b-156">In the XAML and Microsoft Edge frameworks, you can style your text with color fonts the same way as regular fonts, and by default your text will be rendered in color.</span></span> <span data-ttu-id="f218b-157">Toutefois, si votre application appelle directement les API Direct2D (ou API Win2D) pour restituer le texte, elle doit explicitement demander le rendu des polices de couleurs.</span><span class="sxs-lookup"><span data-stu-id="f218b-157">However, if your app directly calls Direct2D APIs (or Win2D APIs) to render text, it must explicitly request color font rendering.</span></span>

### <a name="using-color-fonts-in-a-xaml-app"></a><span data-ttu-id="f218b-158">Utilisation des polices de couleur dans une application XAML</span><span class="sxs-lookup"><span data-stu-id="f218b-158">Using color fonts in a XAML app</span></span>

<span data-ttu-id="f218b-159">Les éléments de texte de la plateforme XAML (tels que [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)et [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) prennent en charge les polices de couleur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f218b-159">The XAML platform s text elements (such as [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396), and [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) support color fonts by default.</span></span> <span data-ttu-id="f218b-160">Il vous suffit de définir le style de votre texte avec une police de couleur, et les glyphes de couleur sont rendus en couleur.</span><span class="sxs-lookup"><span data-stu-id="f218b-160">Simply style your text with a color font, and any color glyphs will be rendered in color.</span></span> <span data-ttu-id="f218b-161">L’exemple de code suivant montre une façon de styliser un TextBlock avec une police de couleur empaquetée avec votre application.</span><span class="sxs-lookup"><span data-stu-id="f218b-161">The following code example shows one way to style a TextBlock with a color font packaged with your app.</span></span> <span data-ttu-id="f218b-162">La même technique s’applique aux polices normales.</span><span class="sxs-lookup"><span data-stu-id="f218b-162">The same technique applies to regular fonts.</span></span>


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



<span data-ttu-id="f218b-163">Si vous ne souhaitez pas que votre élément de texte XAML restitue le texte multicolore, affectez la valeur false à sa propriété [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) .</span><span class="sxs-lookup"><span data-stu-id="f218b-163">If you never want your XAML text element to render multicolored text, set its [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) property to false.</span></span>

### <a name="using-color-fonts-in-microsoft-edge"></a><span data-ttu-id="f218b-164">Utilisation des polices de couleur dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f218b-164">Using color fonts in Microsoft Edge</span></span>

<span data-ttu-id="f218b-165">Les polices de couleur sont rendues par défaut dans les sites Web et les applications Web s’exécutant sur Microsoft Edge, y compris le contrôle XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) .</span><span class="sxs-lookup"><span data-stu-id="f218b-165">Color fonts are rendered by default in websites and web apps running on Microsoft Edge, including the XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) control.</span></span> <span data-ttu-id="f218b-166">Utilisez simplement HTML et CSS pour appliquer un style à votre texte avec une police de couleur, et les glyphes de couleur sont rendus en couleur.</span><span class="sxs-lookup"><span data-stu-id="f218b-166">Simply use HTML and CSS to style your text with a color font, and any color glyphs will be rendered in color.</span></span>

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a><span data-ttu-id="f218b-167">Utilisation des polices de couleur avec DirectWrite et Direct2D</span><span class="sxs-lookup"><span data-stu-id="f218b-167">Using color fonts with DirectWrite and Direct2D</span></span>

<span data-ttu-id="f218b-168">Votre application peut utiliser des méthodes de dessin de texte de niveau supérieur de Direct2D ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) et [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) ou elle peut utiliser des techniques de niveau inférieur pour dessiner des exécutions de glyphes directement.</span><span class="sxs-lookup"><span data-stu-id="f218b-168">Your app can use Direct2D s higher-level text drawing methods ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) and [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) or it can use lower-level techniques to draw glyph runs directly.</span></span> <span data-ttu-id="f218b-169">Dans les deux cas, votre application requiert des modifications de code afin de gérer correctement les glyphes de couleurs.</span><span class="sxs-lookup"><span data-stu-id="f218b-169">In either case, your app requires code changes in order to handle color glyphs correctly.</span></span> <span data-ttu-id="f218b-170">Si votre application utilise les API de la valeur de Direct2D s **DrawText** et **DrawTextLayout** , Notez que celles-ci ne restituent pas les glyphes de couleur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f218b-170">If your app uses Direct2D s **DrawText** and **DrawTextLayout** APIs, note that these do not render color glyphs by default.</span></span> <span data-ttu-id="f218b-171">Cela permet d’éviter des changements de comportement inattendus dans les applications de rendu de texte qui ont été conçues avant la prise en charge des polices de couleur.</span><span class="sxs-lookup"><span data-stu-id="f218b-171">This is to avoid unexpected behavior changes in text rendering apps that were designed prior to color font support.</span></span>

<span data-ttu-id="f218b-172">Pour accepter le rendu des glyphes de couleurs, transmettez l’indicateur de dessin [**d2d1 \_ \_ \_ options \_ activer \_ \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) les options de police de couleur à la méthode de dessin.</span><span class="sxs-lookup"><span data-stu-id="f218b-172">To opt in to color glyph rendering, pass the [**D2D1\_DRAW\_TEXT\_OPTIONS\_ENABLE\_COLOR\_FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) options flag to the drawing method.</span></span> <span data-ttu-id="f218b-173">L’exemple de code suivant montre comment appeler Direct2D s DrawText, méthode pour restituer une chaîne dans une police de couleur :</span><span class="sxs-lookup"><span data-stu-id="f218b-173">The following code example shows how to call Direct2D s DrawText method to render a string in a color font:</span></span>


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



<span data-ttu-id="f218b-174">Si votre application utilise des API de niveau inférieur pour gérer les exécutions de glyphe directement, elle continuera à fonctionner en présence de polices de couleur, mais elle ne pourra pas dessiner de glyphes de couleur sans logique supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="f218b-174">If your app uses lower-level APIs to handle glyph runs directly, then it will continue to function in the presence of color fonts, but it will not be able to draw color glyphs without additional logic.</span></span>

<span data-ttu-id="f218b-175">Pour gérer correctement les glyphes de couleur, votre application doit :</span><span class="sxs-lookup"><span data-stu-id="f218b-175">To correctly handle color glyphs, your app should:</span></span>

1.  <span data-ttu-id="f218b-176">Transmettez les informations d’exécution du glyphe à [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), ainsi qu’un paramètre de [**formats d' \_ \_ image \_ de glyphe DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) qui indique le ou les types de glyphes de couleur que l’application est prêt à gérer.</span><span class="sxs-lookup"><span data-stu-id="f218b-176">Pass the glyph run information to [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), along with a [**DWRITE\_GLYPH\_IMAGE\_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) parameter that indicates which type(s) of color glyph the app is prepared to handle.</span></span> <span data-ttu-id="f218b-177">Si des glyphes de couleur sont présents (selon la police et les **formats d' \_ \_ image de \_ glyphe DWRITE** demandés), DirectWrite fractionne l’exécution du glyphe principal en différentes exécutions de glyphes de couleurs, accessibles via l’objet [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) retourné à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="f218b-177">If any color glyphs are present (based on the font and the requested **DWRITE\_GLYPH\_IMAGE\_FORMATS**), then DirectWrite will split the primary glyph run into individual  color glyph runs  which can be accessed through the returned [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) object in Step 4.</span></span>
2.  <span data-ttu-id="f218b-178">Vérifiez le HRESULT retourné par [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) pour déterminer si des exécutions de glyphes de couleurs ont été détectées.</span><span class="sxs-lookup"><span data-stu-id="f218b-178">Check the HRESULT returned by [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) to determine whether any color glyph runs were detected.</span></span> <span data-ttu-id="f218b-179">Un **HRESULT** de **DWRITE \_ E \_ nocolor** n’indique aucune exécution de glyphe de couleur applicable.</span><span class="sxs-lookup"><span data-stu-id="f218b-179">An **HRESULT** of **DWRITE\_E\_NOCOLOR** indicates no applicable color glyph run.</span></span>
3.  <span data-ttu-id="f218b-180">Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) n’a signalé aucune exécution de glyphes de couleurs (en retournant **DWRITE \_ E \_ nocolor**), l’exécution de glyphe entière est traitée comme monochromatique et votre application doit la dessiner comme vous le souhaitez (par exemple, à l’aide de [**ID2D1DeviceContext ::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span><span class="sxs-lookup"><span data-stu-id="f218b-180">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) reported no color glyph runs (by returning **DWRITE\_E\_NOCOLOR**), then the whole glyph run is treated as monochromatic, and your app should draw it as desired (for example, using [**ID2D1DeviceContext::DrawGlyphRun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span></span>
4.  <span data-ttu-id="f218b-181">Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) signale la présence d’exécutions de glyphes de couleurs, votre application doit ignorer l’exécution du glyphe principal et utiliser à la place les exécutions de glyphes de couleur retournées par TranslateColorGlyphRun.</span><span class="sxs-lookup"><span data-stu-id="f218b-181">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) does report the presence of color glyph runs, then your app should ignore the primary glyph run and instead use the color glyph run(s) returned by TranslateColorGlyphRun.</span></span> <span data-ttu-id="f218b-182">Pour ce faire, itérez au sein de l’objet [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) retourné, en récupérant chaque exécution de glyphe de couleur et en le dessinant en fonction de son format d’image de glyphe (par exemple, vous pouvez utiliser [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) et [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) pour dessiner des glyphes de bitmap de couleur et des glyphes SVG, respectivement).</span><span class="sxs-lookup"><span data-stu-id="f218b-182">To do so, iterate through the returned [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) object, retrieving each color glyph run and drawing it as appropriate for its glyph image format (for example, you can use [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) and [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) to draw color bitmap glyphs and SVG glyphs, respectively).</span></span>

<span data-ttu-id="f218b-183">L’exemple de code suivant illustre la structure générale de cette procédure :</span><span class="sxs-lookup"><span data-stu-id="f218b-183">The following code example shows the general structure of this procedure:</span></span>


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



### <a name="using-color-fonts-with-win2d"></a><span data-ttu-id="f218b-184">Utilisation des polices de couleur avec Win2D</span><span class="sxs-lookup"><span data-stu-id="f218b-184">Using color fonts with Win2D</span></span>

<span data-ttu-id="f218b-185">À l’instar de Direct2D, les API de dessin de texte Win2D s ne restituent pas les glyphes de couleur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f218b-185">Similar to Direct2D, Win2D s text drawing APIs do not render color glyphs by default.</span></span> <span data-ttu-id="f218b-186">Pour accepter le rendu des glyphes de couleurs, définissez l’indicateur options [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) dans l’objet de format de texte que votre application passe à la méthode de dessin de texte.</span><span class="sxs-lookup"><span data-stu-id="f218b-186">To opt in to color glyph rendering, set the [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) options flag in the text format object your app passes to the text drawing method.</span></span> <span data-ttu-id="f218b-187">L’exemple de code suivant montre comment restituer une chaîne dans une police de couleur à l’aide de Win2D :</span><span class="sxs-lookup"><span data-stu-id="f218b-187">The following code example shows how to render a string in a color font using Win2D:</span></span>


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

## <a name="related-topics"></a><span data-ttu-id="f218b-188">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f218b-188">Related topics</span></span>

[<span data-ttu-id="f218b-189">Exemple de glyphe de couleur DirectWrite</span><span class="sxs-lookup"><span data-stu-id="f218b-189">DirectWrite colored glyph sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[<span data-ttu-id="f218b-190">**Interface IDWriteFontFace4**</span><span class="sxs-lookup"><span data-stu-id="f218b-190">**IDWriteFontFace4 interface**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[<span data-ttu-id="f218b-191">**IDWriteFactory4 :: TranslateColorGlyphRun, méthode**</span><span class="sxs-lookup"><span data-stu-id="f218b-191">**IDWriteFactory4::TranslateColorGlyphRun method**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[<span data-ttu-id="f218b-192">**ID2D1DeviceContext4 ::D méthode rawText**</span><span class="sxs-lookup"><span data-stu-id="f218b-192">**ID2D1DeviceContext4::DrawText method**</span></span>](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

