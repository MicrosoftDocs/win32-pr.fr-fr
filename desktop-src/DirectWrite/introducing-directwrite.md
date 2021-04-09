---
title: Présentation de DirectWrite
description: Les personnes communiquent avec le texte tout le temps de leur vie quotidienne.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, à propos de
- DirectWrite, fonctionnalités typographiques
- typographie
- DirectWrite, texte international
- DirectWrite, polices OpenType
- Polices OpenType
- DirectWrite, ClearType
- ClearType
- DirectWrite, vue d’ensemble de l’API
- DirectWrite, IDWriteFontFace
- IDWriteFontFace
- DirectWrite, rendu de texte
- DirectWrite, modes de rendu
- DirectWrite, interopérabilité GDI
- DirectWrite, interopérabilité
- interopérabilité, DirectWrite
- interopérabilité, Graphics Device Interface (GDI)
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842678"
---
# <a name="introducing-directwrite"></a><span data-ttu-id="cbfb6-122">Présentation de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="cbfb6-122">Introducing DirectWrite</span></span>

<span data-ttu-id="cbfb6-123">Les personnes communiquent avec le texte tout le temps de leur vie quotidienne.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-123">People communicate with text all the time in their daily lives.</span></span> <span data-ttu-id="cbfb6-124">C’est le principal moyen pour les utilisateurs de consommer un volume d’informations en plus important.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-124">It is the primary way for people to consume an increasing volume of information.</span></span> <span data-ttu-id="cbfb6-125">Dans le passé, il était utilisé par le contenu imprimé, principalement des documents, des journaux, des livres, etc.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-125">In the past, it used to be through printed content, primarily documents, newspapers, books, and so on.</span></span> <span data-ttu-id="cbfb6-126">De plus en plus, il s’agit d’un contenu en ligne sur son PC Windows.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-126">Increasingly, it is online content on their Windows PC.</span></span> <span data-ttu-id="cbfb6-127">Un utilisateur Windows classique passe beaucoup de temps à lire à partir de son écran d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-127">A typical Windows user spends a lot of time reading from their computer screen.</span></span> <span data-ttu-id="cbfb6-128">Ils peuvent surfer sur le Web, analyser le courrier électronique, rédiger un rapport, remplir une feuille de calcul ou écrire des logiciels, mais ce qu’ils font vraiment, c’est la lecture.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-128">They might be surfing the Web, scanning e-mail, composing a report, filling in a spreadsheet, or writing software, but what they're really doing is reading.</span></span> <span data-ttu-id="cbfb6-129">Même si le texte et les polices sont performants presque toutes les parties de l’expérience utilisateur dans Windows, pour la plupart des utilisateurs, la lecture sur l’écran n’est pas aussi agréable que la lecture imprimée.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-129">Even though text and fonts permeate nearly every part of the user experience in Windows, for most users, reading on the screen is not as enjoyable as reading printed output.</span></span>

<span data-ttu-id="cbfb6-130">Pour les développeurs d’applications Windows, l’écriture de code de gestion de texte est un défi en raison des exigences accrues pour une meilleure lisibilité, une mise en forme et un contrôle de disposition sophistiqués, ainsi que la prise en charge de plusieurs langues que l’application doit afficher.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-130">For Windows application developers, writing text-handling code is a challenge because of the increased requirements for better readability, sophisticated formatting and layout control, and support for the multiple languages the application must display.</span></span> <span data-ttu-id="cbfb6-131">Même le système de gestion de texte le plus basique doit autoriser la saisie de texte, la mise en page, l’affichage, la modification et la copie et le collage.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-131">Even the most basic text-handling system must allow for text input, layout, display, editing, and copying and pasting.</span></span> <span data-ttu-id="cbfb6-132">Les utilisateurs de Windows attendent généralement plus que ces fonctionnalités de base, nécessitant des éditeurs simples pour la prise en charge de plusieurs polices, de divers styles de paragraphes, d’images incorporées, d’une vérification orthographique et d’autres fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-132">Windows users commonly expect even more than these basic features, requiring even simple editors to support multiple fonts, various paragraph styles, embedded images, spell checking, and other features.</span></span> <span data-ttu-id="cbfb6-133">La conception d’interface utilisateur moderne n’est pas non plus limitée à un format simple, du texte brut, mais doit présenter une meilleure expérience en matière de polices de texte et de polices riches.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-133">Modern UI design is also no longer confined to single format, plain text, but needs to present a better experience with rich fonts and text layouts.</span></span>

<span data-ttu-id="cbfb6-134">Il s’agit d’une introduction à la façon dont [DirectWrite](direct-write-portal.md) permet aux applications Windows d’améliorer l’expérience de texte pour l’interface utilisateur et les documents.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-134">This is an introduction to how [DirectWrite](direct-write-portal.md) enables Windows applications to enhance the text experience for UI and documents.</span></span>

## <a name="improving-the-text-experience"></a><span data-ttu-id="cbfb6-135">Amélioration de l’expérience de texte</span><span class="sxs-lookup"><span data-stu-id="cbfb6-135">Improving the Text Experience</span></span>

<span data-ttu-id="cbfb6-136">Les applications Windows modernes ont des exigences sophistiquées pour le texte dans leur interface utilisateur et leurs documents.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-136">Modern Windows applications have sophisticated requirements for text in their UI and documents.</span></span> <span data-ttu-id="cbfb6-137">Celles-ci incluent une meilleure lisibilité, la prise en charge d’une grande variété de langages et de scripts et des performances de rendu supérieures.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-137">These include better readability, support for a large variety of languages and scripts, and superior rendering performance.</span></span> <span data-ttu-id="cbfb6-138">En outre, la plupart des applications existantes nécessitent un moyen de transférer les investissements existants dans la base de code WindowsWin32.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-138">In addition, most existing applications require a way to carry forward existing investments in the WindowsWin32 code base.</span></span>

<span data-ttu-id="cbfb6-139">[DirectWrite](direct-write-portal.md) fournit les trois fonctionnalités suivantes qui permettent aux développeurs d’applications Windows d’améliorer l’expérience de texte dans leurs applications : l’indépendance par rapport au système de rendu, la typographie de haute qualité et plusieurs couches de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-139">[DirectWrite](direct-write-portal.md) provides the following three features that enable Windows application developers to improve the text experience within their applications: independence from the rendering system, high-quality typography, and multiple layers of functionality.</span></span>

## <a name="rendering-system-independence"></a><span data-ttu-id="cbfb6-140">Indépendance Rendering-System</span><span class="sxs-lookup"><span data-stu-id="cbfb6-140">Rendering-System Independence</span></span>

<span data-ttu-id="cbfb6-141">[DirectWrite](direct-write-portal.md) est indépendant de toute technologie graphique particulière.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-141">[DirectWrite](direct-write-portal.md) is independent of any particular graphics technology.</span></span> <span data-ttu-id="cbfb6-142">Les applications sont libres d’utiliser la technologie de rendu qui convient le mieux à leurs besoins.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-142">Applications are free to use the rendering technology best suited to their needs.</span></span> <span data-ttu-id="cbfb6-143">Cela permet aux applications de continuer à afficher certaines parties de leur application via GDI et d’autres parties via Direct3D ou [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb6-143">This gives applications the flexibility to continue rendering some parts of their application through GDI and other parts through Direct3D or [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="cbfb6-144">En fait, une application peut choisir d’afficher DirectWrite via une pile de rendu propriétaire.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-144">In fact, an application could choose to render DirectWrite through a proprietary rendering stack.</span></span>

## <a name="high-quality-typography"></a><span data-ttu-id="cbfb6-145">Typographie High-Quality</span><span class="sxs-lookup"><span data-stu-id="cbfb6-145">High-Quality Typography</span></span>

<span data-ttu-id="cbfb6-146">[DirectWrite](direct-write-portal.md) tire parti des avancées de la technologie de police [OpenType](../intl/opentype-font-format.md) pour permettre une typographie de haute qualité dans une application Windows.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-146">[DirectWrite](direct-write-portal.md) takes advantage of the advances in [OpenType](../intl/opentype-font-format.md) Font technology to enable high quality typography within a Windows application.</span></span> <span data-ttu-id="cbfb6-147">Le système de police DirectWrite fournit des services pour gérer l’énumération des polices, la police de substitution et la mise en cache des polices, qui sont toutes nécessaires aux applications pour la gestion des polices.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-147">The DirectWrite font system provides services for dealing with font enumeration, font fallback, and font caching, which are all needed by applications for handling fonts.</span></span>

<span data-ttu-id="cbfb6-148">La prise en charge [OpenType](../intl/opentype-font-format.md) fournie par [DirectWrite](direct-write-portal.md) permet aux développeurs d’ajouter à leurs applications des fonctionnalités typographiques avancées et la prise en charge du texte international.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-148">The [OpenType](../intl/opentype-font-format.md) support provided by [DirectWrite](direct-write-portal.md) enables developers to add to their applications advanced typographic features and support for international text.</span></span>

## <a name="support-for-advanced-typographic-features"></a><span data-ttu-id="cbfb6-149">Prise en charge des fonctionnalités typographiques avancées</span><span class="sxs-lookup"><span data-stu-id="cbfb6-149">Support for Advanced Typographic Features</span></span>

<span data-ttu-id="cbfb6-150">[DirectWrite](direct-write-portal.md) permet aux développeurs d’applications de déverrouiller les fonctionnalités des polices OpenType qu’ils n’ont pas pu utiliser dans WINFORMS ou GDI.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-150">[DirectWrite](direct-write-portal.md) enables application developers to unlock the features of OpenType fonts that they couldn't use in WinForms or GDI.</span></span> <span data-ttu-id="cbfb6-151">L’objet DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) expose un grand nombre des fonctionnalités avancées des polices OpenType, telles que les variantes stylistiques et les paraphes.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-151">The DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) object exposes many of the advanced features of OpenType fonts, such as stylistic alternates and swashes.</span></span> <span data-ttu-id="cbfb6-152">Le kit de développement logiciel (SDK) Microsoft Windows fournit un ensemble d’exemples de polices [OpenType](../intl/opentype-font-format.md) conçues avec des fonctionnalités riches, telles que les polices Pericles et Pescadero.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-152">The Microsoft Windows Software Development Kit (SDK) provides a set of sample [OpenType](../intl/opentype-font-format.md) fonts that are designed with rich features, such as the Pericles and Pescadero fonts.</span></span> <span data-ttu-id="cbfb6-153">Pour plus d’informations sur les fonctionnalités OpenType, consultez [caractéristiques des polices OpenType](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cbfb6-153">For more details on OpenType features, see [OpenType Font Features](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span></span>

## <a name="support-for-international-text"></a><span data-ttu-id="cbfb6-154">Prise en charge du texte international</span><span class="sxs-lookup"><span data-stu-id="cbfb6-154">Support for International Text</span></span>

<span data-ttu-id="cbfb6-155">[DirectWrite](direct-write-portal.md) utilise des polices [OpenType](../intl/opentype-font-format.md) pour permettre une prise en charge étendue du texte international.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-155">[DirectWrite](direct-write-portal.md) uses [OpenType](../intl/opentype-font-format.md) fonts to enable broad support for international text.</span></span> <span data-ttu-id="cbfb6-156">Les fonctionnalités Unicode telles que les substituts, BIDI, saut de ligne et UVS sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-156">Unicode features such as surrogates, BIDI, line breaking, and UVS are supported.</span></span> <span data-ttu-id="cbfb6-157">L’élément de script guidé dans le langage, la substitution de nombres et la mise en forme de glyphes garantissent que le texte de n’importe quel script possède une disposition et un rendu corrects.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-157">Language-guided script itemization, number substitution, and glyph shaping ensure that text in any script has the correct layout and rendering.</span></span>

<span data-ttu-id="cbfb6-158">Les scripts suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="cbfb6-158">The following scripts are currently supported:</span></span>

> [!Note]  
> <span data-ttu-id="cbfb6-159">Pour les scripts marqués avec un \* , il n’y a pas de polices système par défaut.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-159">For scripts marked with an \*, there are no default system fonts.</span></span> <span data-ttu-id="cbfb6-160">Les applications doivent installer les polices qui prennent en charge ces scripts.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-160">Applications must install fonts that support these scripts.</span></span>

 

-   <span data-ttu-id="cbfb6-161">Arabe</span><span class="sxs-lookup"><span data-stu-id="cbfb6-161">Arabic</span></span>
-   <span data-ttu-id="cbfb6-162">Arménien</span><span class="sxs-lookup"><span data-stu-id="cbfb6-162">Armenian</span></span>
-   <span data-ttu-id="cbfb6-163">Bengala</span><span class="sxs-lookup"><span data-stu-id="cbfb6-163">Bengala</span></span>
-   <span data-ttu-id="cbfb6-164">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="cbfb6-164">Bopomofo</span></span>
-   <span data-ttu-id="cbfb6-165">Braille\*</span><span class="sxs-lookup"><span data-stu-id="cbfb6-165">Braille\*</span></span>
-   <span data-ttu-id="cbfb6-166">SYLLABE autochtones canadienne</span><span class="sxs-lookup"><span data-stu-id="cbfb6-166">Canadian aboriginal syllabics</span></span>
-   <span data-ttu-id="cbfb6-167">Cherokee</span><span class="sxs-lookup"><span data-stu-id="cbfb6-167">Cherokee</span></span>
-   <span data-ttu-id="cbfb6-168">Chinois (simplifié & traditionnel)</span><span class="sxs-lookup"><span data-stu-id="cbfb6-168">Chinese (Simplified & Traditional)</span></span>
-   <span data-ttu-id="cbfb6-169">Cyrillique</span><span class="sxs-lookup"><span data-stu-id="cbfb6-169">Cyrillic</span></span>
-   <span data-ttu-id="cbfb6-170">Copte\*</span><span class="sxs-lookup"><span data-stu-id="cbfb6-170">Coptic\*</span></span>
-   <span data-ttu-id="cbfb6-171">Dévanâgarî</span><span class="sxs-lookup"><span data-stu-id="cbfb6-171">Devanagari</span></span>
-   <span data-ttu-id="cbfb6-172">Éthiopien</span><span class="sxs-lookup"><span data-stu-id="cbfb6-172">Ethiopic</span></span>
-   <span data-ttu-id="cbfb6-173">Géorgien</span><span class="sxs-lookup"><span data-stu-id="cbfb6-173">Georgian</span></span>
-   <span data-ttu-id="cbfb6-174">Lettre\*</span><span class="sxs-lookup"><span data-stu-id="cbfb6-174">Glagolitic\*</span></span>
-   <span data-ttu-id="cbfb6-175">Grec</span><span class="sxs-lookup"><span data-stu-id="cbfb6-175">Greek</span></span>
-   <span data-ttu-id="cbfb6-176">Goudjrati</span><span class="sxs-lookup"><span data-stu-id="cbfb6-176">Gujarati</span></span>
-   <span data-ttu-id="cbfb6-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="cbfb6-177">Gurmukhi</span></span>
-   <span data-ttu-id="cbfb6-178">Hébreu</span><span class="sxs-lookup"><span data-stu-id="cbfb6-178">Hebrew</span></span>
-   <span data-ttu-id="cbfb6-179">Japonais</span><span class="sxs-lookup"><span data-stu-id="cbfb6-179">Japanese</span></span>
-   <span data-ttu-id="cbfb6-180">Kannada</span><span class="sxs-lookup"><span data-stu-id="cbfb6-180">Kannada</span></span>
-   <span data-ttu-id="cbfb6-181">Khmer</span><span class="sxs-lookup"><span data-stu-id="cbfb6-181">Khmer</span></span>
-   <span data-ttu-id="cbfb6-182">Coréen</span><span class="sxs-lookup"><span data-stu-id="cbfb6-182">Korean</span></span>
-   <span data-ttu-id="cbfb6-183">Lao</span><span class="sxs-lookup"><span data-stu-id="cbfb6-183">Lao</span></span>
-   <span data-ttu-id="cbfb6-184">Latin</span><span class="sxs-lookup"><span data-stu-id="cbfb6-184">Latin</span></span>
-   <span data-ttu-id="cbfb6-185">Malayalam</span><span class="sxs-lookup"><span data-stu-id="cbfb6-185">Malayalam</span></span>
-   <span data-ttu-id="cbfb6-186">Mongol</span><span class="sxs-lookup"><span data-stu-id="cbfb6-186">Mongolian</span></span>
-   <span data-ttu-id="cbfb6-187">Myanmar</span><span class="sxs-lookup"><span data-stu-id="cbfb6-187">Myanmar</span></span>
-   <span data-ttu-id="cbfb6-188">Nouveau taï lü</span><span class="sxs-lookup"><span data-stu-id="cbfb6-188">New Tai Lue</span></span>
-   <span data-ttu-id="cbfb6-189">OGAM\*</span><span class="sxs-lookup"><span data-stu-id="cbfb6-189">Ogham\*</span></span>
-   <span data-ttu-id="cbfb6-190">Odia</span><span class="sxs-lookup"><span data-stu-id="cbfb6-190">Odia</span></span>
-   <span data-ttu-id="cbfb6-191">'PHAGS-PA</span><span class="sxs-lookup"><span data-stu-id="cbfb6-191">'Phags-pa</span></span>
-   <span data-ttu-id="cbfb6-192">Lettre\*</span><span class="sxs-lookup"><span data-stu-id="cbfb6-192">Runic\*</span></span>
-   <span data-ttu-id="cbfb6-193">Cingalais</span><span class="sxs-lookup"><span data-stu-id="cbfb6-193">Sinhala</span></span>
-   <span data-ttu-id="cbfb6-194">Syriaque</span><span class="sxs-lookup"><span data-stu-id="cbfb6-194">Syriac</span></span>
-   <span data-ttu-id="cbfb6-195">LETTRE TAÏ le</span><span class="sxs-lookup"><span data-stu-id="cbfb6-195">Tai Le</span></span>
-   <span data-ttu-id="cbfb6-196">Tamoul</span><span class="sxs-lookup"><span data-stu-id="cbfb6-196">Tamil</span></span>
-   <span data-ttu-id="cbfb6-197">Télougou</span><span class="sxs-lookup"><span data-stu-id="cbfb6-197">Telugu</span></span>
-   <span data-ttu-id="cbfb6-198">Tana</span><span class="sxs-lookup"><span data-stu-id="cbfb6-198">Thaana</span></span>
-   <span data-ttu-id="cbfb6-199">Thaï</span><span class="sxs-lookup"><span data-stu-id="cbfb6-199">Thai</span></span>
-   <span data-ttu-id="cbfb6-200">Tibétain</span><span class="sxs-lookup"><span data-stu-id="cbfb6-200">Tibetan</span></span>
-   <span data-ttu-id="cbfb6-201">Yi</span><span class="sxs-lookup"><span data-stu-id="cbfb6-201">Yi</span></span>

## <a name="multiple-layers-of-functionality"></a><span data-ttu-id="cbfb6-202">Plusieurs couches de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="cbfb6-202">Multiple Layers of Functionality</span></span>

<span data-ttu-id="cbfb6-203">[DirectWrite](direct-write-portal.md) fournit des couches de fonctionnalités pondérées, chaque couche interagissant en toute transparence avec la suivante.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-203">[DirectWrite](direct-write-portal.md) provides factored layers of functionality, with each layer interacting seamlessly with the next.</span></span> <span data-ttu-id="cbfb6-204">La conception d’API offre aux développeurs d’applications la liberté et la flexibilité nécessaires pour adopter des couches individuelles en fonction de leurs besoins et de leur planification.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-204">The API design gives application developers the freedom and flexibility to adopt individual layers depending on their needs and schedule.</span></span> <span data-ttu-id="cbfb6-205">Le diagramme suivant illustre la relation entre ces couches.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-205">The following diagram shows the relationship between these layers.</span></span>

![diagramme des couches DirectWrite et de la façon dont elles communiquent avec une application ou une infrastructure d’interface utilisateur et l’API Graphics](images/intro-01.png)

<span data-ttu-id="cbfb6-207">L’API Text Layout fournit les fonctionnalités de niveau le plus élevé disponibles dans [DirectWrite](direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb6-207">The text layout API provides the highest level functionality available from [DirectWrite](direct-write-portal.md).</span></span> <span data-ttu-id="cbfb6-208">Il fournit des services permettant à l’application de mesurer, d’afficher et d’interagir avec des chaînes de texte riches en format.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-208">It provides services for the application to measure, display, and interact with richly formatted text strings.</span></span> <span data-ttu-id="cbfb6-209">Cette API Text peut être utilisée dans les applications qui utilisent actuellement Win32 DrawText pour générer une interface utilisateur moderne avec du texte riche en format.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-209">This text API can be used in applications that currently use Win32's DrawText to build a modern UI with richly formatted text.</span></span>

<span data-ttu-id="cbfb6-210">Les applications gourmandes en texte qui implémentent leur propre moteur de disposition peuvent utiliser la couche suivante : le processeur de script.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-210">Text-intensive applications that implement their own layout engine may use the next layer down: the script processor.</span></span> <span data-ttu-id="cbfb6-211">Le processeur de script décompose un segment de texte en blocs de script et gère le mappage entre les représentations Unicode et la représentation de glyphe appropriée dans la police afin que le texte du script puisse s’afficher correctement dans la langue appropriée.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-211">The script processor breaks down a chunk of text into script blocks and handles the mapping between Unicode representations to the appropriate glyph representation in the font so the text of the script can be correctly displayed in the correct language.</span></span> <span data-ttu-id="cbfb6-212">Le système de disposition utilisé par la couche de l’API Text Layout est basé sur le système de polices et de traitement des scripts.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-212">The layout system used by the text layout API layer is built upon the font and script processing system.</span></span>

<span data-ttu-id="cbfb6-213">La couche de rendu de glyphes est la couche de fonctionnalités la plus basse et fournit des fonctionnalités de rendu de glyphes pour les applications qui implémentent leur propre moteur de disposition de texte.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-213">The glyph-rendering layer is the lowest layer of functionality and provides glyph-rendering functionality for applications that implement their own text layout engine.</span></span> <span data-ttu-id="cbfb6-214">La couche de rendu des glyphes est également utile pour les applications qui implémentent un convertisseur personnalisé pour modifier le comportement de dessin de glyphe par le biais de la fonction de rappel dans l’API de mise en forme du texte [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb6-214">The glyph rendering layer is also useful for applications that implement a custom renderer to modify the glyph-drawing behavior through the callback function in the [DirectWrite](direct-write-portal.md) text-formatting API.</span></span>

<span data-ttu-id="cbfb6-215">Le système de polices [DirectWrite](direct-write-portal.md) est disponible pour toutes les couches fonctionnelles de DirectWrite et permet à une application d’accéder aux informations sur les polices et les glyphes.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-215">The [DirectWrite](direct-write-portal.md) font system is available to all the DirectWrite functional layers and enables an application to access font and glyph information.</span></span> <span data-ttu-id="cbfb6-216">Il est conçu pour gérer les technologies de polices et les formats de données courants.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-216">It is designed to handle common font technologies and data formats.</span></span> <span data-ttu-id="cbfb6-217">Le modèle de police DirectWrite suit la pratique typographique courante qui consiste à prendre en charge un nombre quelconque de poids, de styles et d’étirements dans la même famille de polices.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-217">The DirectWrite font model follows the common typographic practice of supporting any number of weights, styles, and stretches in the same font family.</span></span> <span data-ttu-id="cbfb6-218">Ce modèle, le même modèle suivi par WPF et CSS, spécifie que les polices qui diffèrent uniquement en poids (gras, clair, etc.), style (vertical, italique ou oblique) ou Stretch (étroit, condensé, large, etc.) sont considérées comme des membres d’une même famille de polices.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-218">This model, the same model followed by WPF and CSS, specifies that fonts differing only in weight (bold, light, and so on), style (upright, italic, or oblique) or stretch (narrow, condensed, wide, and so on) are considered to be members of a single font family.</span></span>

### <a name="improved-text-rendering-with-cleartype"></a><span data-ttu-id="cbfb6-219">Amélioration du rendu du texte avec ClearType</span><span class="sxs-lookup"><span data-stu-id="cbfb6-219">Improved Text Rendering with ClearType</span></span>

<span data-ttu-id="cbfb6-220">L’amélioration de la lisibilité sur l’écran est une condition essentielle pour toutes les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-220">Improving readability on the screen is a key requirement for all Windows applications.</span></span> <span data-ttu-id="cbfb6-221">La preuve de la recherche en psychologie cognitive indique que nous devons être en mesure de reconnaître toutes les lettres avec précision et que même l’espacement entre les lettres est essentiel pour un traitement rapide.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-221">The evidence from research in cognitive psychology indicates that we need to be able to recognize every letter accurately and that even spacing between letters is critical for fast processing.</span></span> <span data-ttu-id="cbfb6-222">Les lettres et les mots qui ne sont pas symétriques sont perçus comme insupportable et dégradent l’expérience de lecture.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-222">Letters and words that are not symmetrical are perceived as ugly and degrade the reading experience.</span></span> <span data-ttu-id="cbfb6-223">Kevin Larson, Microsoft Advanced Read Technologies Group, a écrit un article sur le sujet qui a été publié dans Spectrum IEEE.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-223">Kevin Larson, Microsoft Advanced Reading Technologies group, wrote an article on the subject that was published in Spectrum IEEE.</span></span> <span data-ttu-id="cbfb6-224">L’article est appelé « technologie de texte » ( https://www.spectrum.ieee.org/print/5049) .</span><span class="sxs-lookup"><span data-stu-id="cbfb6-224">The article is called "The Technology of Text" (https://www.spectrum.ieee.org/print/5049).</span></span>

<span data-ttu-id="cbfb6-225">Le texte de [DirectWrite](direct-write-portal.md) est rendu à l’aide de Microsoft ClearType, ce qui améliore la clarté et la lisibilité du texte.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-225">Text in [DirectWrite](direct-write-portal.md) is rendered using Microsoft ClearType, which enhances the clarity and readability of text.</span></span> <span data-ttu-id="cbfb6-226">ClearType tire parti du fait que les écrans LCD modernes affichent des bandes RVB pour chaque pixel pouvant être contrôlé individuellement.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-226">ClearType takes advantage of the fact that modern LCD displays have RGB stripes for each pixel that can be controlled individually.</span></span> <span data-ttu-id="cbfb6-227">DirectWrite utilise les dernières améliorations apportées à ClearType, d’abord inclus avec Windows Vista avec Windows Presentation Foundation, qui lui permet d’évaluer non seulement les lettres individuelles, mais également l’espacement entre les lettres.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-227">DirectWrite uses the latest enhancements to ClearType, first included with Windows Vista with Windows Presentation Foundation, that enables it to evaluate not just the individual letters but also the spacing between letters.</span></span> <span data-ttu-id="cbfb6-228">Avant ces améliorations ClearType, le texte avec une taille de « lecture » de 10 ou 12 points était difficile à afficher : nous pourrions placer 1 pixel entre les lettres, ce qui était souvent trop faible, ou 2 pixels, ce qui était souvent trop grand.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-228">Before these ClearType enhancements, text with a "reading" size of 10 or 12 points was difficult to display: we could place either 1 pixel in between letters, which was often too little, or 2 pixels, which was often too much.</span></span> <span data-ttu-id="cbfb6-229">L’utilisation de la résolution supplémentaire dans les sous-pixels nous fournit un espacement fractionnaire qui améliore l’uniformité et la symétrie de la page entière.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-229">Using the extra resolution in the subpixels provides us with fractional spacing, which improves the evenness and symmetry of the entire page.</span></span>

<span data-ttu-id="cbfb6-230">Les deux illustrations suivantes montrent comment les glyphes peuvent commencer sur n’importe quelle limite de sous-pixel lorsque le positionnement du sous-pixel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-230">The following two illustration show how glyphs may begin on any sub-pixel boundary when sub-pixel positioning is used.</span></span>

<span data-ttu-id="cbfb6-231">L’illustration suivante est rendue à l’aide de la version GDI du convertisseur ClearType, qui n’utilisait pas le positionnement du sous-pixel.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-231">The following illustration is rendered using the GDI version of the ClearType renderer, which did not employ sub-pixel positioning.</span></span>

![illustration de la « technologie » rendue sans le positionnement des sous-pixels](images/intro-03.png)

<span data-ttu-id="cbfb6-233">L’illustration suivante est rendue à l’aide de la version [DirectWrite](direct-write-portal.md) du convertisseur ClearType, qui utilise le positionnement de sous-pixel.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-233">The following illustration is rendered using the [DirectWrite](direct-write-portal.md) version of the ClearType renderer, which uses sub-pixel positioning.</span></span>

![illustration de la « technologie » rendue avec le positionnement des sous-pixels](images/intro-04.png)

<span data-ttu-id="cbfb6-235">Notez que l’espacement entre les lettres h et n est plus pair dans la deuxième image et que la lettre o est plus espacée de la lettre n, plus même avec la lettre l.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-235">Note that the spacing between the letters h and n is more even in the second image and the letter o is spaced further from the letter n, more even with the letter l.</span></span> <span data-ttu-id="cbfb6-236">Notez également que les tiges sur les lettres l sont plus naturelles.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-236">Also note how the stems on the letters l are more natural looking.</span></span>

<span data-ttu-id="cbfb6-237">Le positionnement ClearType de sous-pixel offre l’espace de caractères le plus précis à l’écran, en particulier pour les petites tailles où la différence entre un sous-pixel et un pixel entier représente une proportion significative de la largeur de glyphe.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-237">The subpixel ClearType positioning offers the most accurate spacing of characters on screen, especially at small sizes where the difference between a sub-pixel and a whole pixel represents a significant proportion of glyph width.</span></span> <span data-ttu-id="cbfb6-238">Il permet de mesurer le texte dans un espace de résolution idéal et de le rendre à sa position naturelle à l’aide de la bande de couleur de l’écran LCD, avec une granularité de sous-pixel.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-238">It enables text to be measured in ideal resolution space and rendered at its natural position at the LCD color stripe, with subpixel granularity.</span></span> <span data-ttu-id="cbfb6-239">Le texte mesuré et rendu à l’aide de cette technologie est, par définition, indépendant de la résolution, ce qui signifie que la même disposition du texte est obtenue sur la plage de différentes résolutions d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-239">Text measured and rendered using this technology is, by definition, resolution-independent, meaning that the exact same layout of text is achieved across the range of various display resolutions.</span></span>

<span data-ttu-id="cbfb6-240">Contrairement à l’un ou l’autre type de rendu ClearType GDI, le ClearType sous-pixel offre la largeur de caractères la plus précise.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-240">Unlike either type of GDI ClearType rendering, sub-pixel ClearType offers the most accurate width of characters.</span></span>

<span data-ttu-id="cbfb6-241">L’API de chaîne de texte adopte par défaut le rendu de texte de sous-pixel, ce qui signifie qu’elle mesure le texte à sa résolution idéale indépendamment de la résolution d’affichage actuelle, et produit le résultat de positionnement du glyphe en fonction des largeurs d’avance de glyphe réellement mis à l’échelle et des décalages de positionnement.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-241">The Text String API adopts sub-pixel text rendering by default, which means it measures text at its ideal resolution independent of the current display resolution, and produces the glyph positioning result based on the truly scaled glyph advance widths and positioning offsets.</span></span>

<span data-ttu-id="cbfb6-242">Pour le texte de grande taille, [DirectWrite](direct-write-portal.md) permet également l’anticrénelage le long de l’axe y pour rendre les bords plus lisses et rendre les lettres plus lisses comme le concepteur de polices.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-242">For large-sized text, [DirectWrite](direct-write-portal.md) also enables anti-aliasing along the y-axis to make the edges smoother and render letters as the font designer intended.</span></span> <span data-ttu-id="cbfb6-243">L’illustration suivante montre l’anticrénelage de direction y.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-243">The following illustration shows y-direction anti-aliasing.</span></span>

![illustration de « ClearType » rendue sous forme de texte GDI et de texte DirectWrite avec l’anticrénelage de direction y](images/intro-05.png)

<span data-ttu-id="cbfb6-245">Bien que le texte [DirectWrite](direct-write-portal.md) soit positionné et rendu à l’aide de l’option ClearType sous-pixel par défaut, d’autres options de rendu sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-245">Although [DirectWrite](direct-write-portal.md) text is positioned and rendered using sub-pixel ClearType by default, other rendering options are available.</span></span> <span data-ttu-id="cbfb6-246">De nombreuses applications existantes utilisent GDI pour restituer la plupart de leur interface utilisateur, et certaines applications utilisent des contrôles d’édition du système qui continuent d’utiliser GDI pour le rendu du texte.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-246">Many existing applications use GDI to render most of their UI, and some applications use system editing controls that continue to use GDI for text rendering.</span></span> <span data-ttu-id="cbfb6-247">Lorsque vous ajoutez du texte DirectWrite à ces applications, il peut être nécessaire de sacrifier les améliorations apportées à l’expérience de lecture fournies par la fonction ClearType de sous-pixel afin que le texte ait une apparence cohérente dans l’application.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-247">When adding DirectWrite text to these applications, it may be necessary to sacrifice the reading experience improvements provided by sub-pixel ClearType so that text has a consistent appearance across the application.</span></span>

<span data-ttu-id="cbfb6-248">Pour répondre à ces exigences, [DirectWrite](direct-write-portal.md) prend également en charge les options de rendu suivantes :</span><span class="sxs-lookup"><span data-stu-id="cbfb6-248">To meet these requirements, [DirectWrite](direct-write-portal.md) also supports the following rendering options:</span></span>

-   <span data-ttu-id="cbfb6-249">Sous-pixel ClearType (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="cbfb6-249">Sub-pixel ClearType (default).</span></span>
-   <span data-ttu-id="cbfb6-250">ClearType sous-pixel avec anticrénelage à la fois dans les dimensions horizontales et verticales.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-250">Sub-pixel ClearType with anti-aliasing in both horizontal and vertical dimensions.</span></span>
-   <span data-ttu-id="cbfb6-251">Texte avec alias.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-251">Aliased text.</span></span>
-   <span data-ttu-id="cbfb6-252">GDI-largeur naturelle (utilisée par Microsoft Word Mode Lecture, par exemple).</span><span class="sxs-lookup"><span data-stu-id="cbfb6-252">GDI natural-width (used by Microsoft Word Reading View, for example).</span></span>
-   <span data-ttu-id="cbfb6-253">Compatible GDI-largeur (y compris l’image bitmap incorporée d’Extrême-Orient).</span><span class="sxs-lookup"><span data-stu-id="cbfb6-253">GDI compatible-width (including East Asian embedded bitmap).</span></span>

<span data-ttu-id="cbfb6-254">Chacun de ces modes de rendu peut être affiné par le biais de l’API DirectWrite et du nouveau tuner ClearType de la boîte de réception Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-254">Each of these rendering modes can be fine-tuned through the DirectWrite API and through the new Windows 7 inbox ClearType tuner.</span></span>

> [!Note]  
> <span data-ttu-id="cbfb6-255">À compter de Windows 8, vous devez utiliser l’anticrénelage de texte en nuances de gris dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-255">Starting with Windows 8, you should use greyscale text antialiasing in most cases.</span></span> <span data-ttu-id="cbfb6-256">Pour en savoir plus, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-256">See the next section for more information.</span></span>

 

### <a name="support-for-natural-layout"></a><span data-ttu-id="cbfb6-257">Prise en charge de la disposition naturelle</span><span class="sxs-lookup"><span data-stu-id="cbfb6-257">Support for Natural Layout</span></span>

<span data-ttu-id="cbfb6-258">La disposition naturelle est indépendante de la résolution, de sorte que l’espacement des caractères ne change pas au fur et à mesure que vous effectuez un zoom avant ou arrière, ou en fonction de la résolution de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-258">Natural layout is resolution-independent, so the spacing of characters doesn't change as you zoom in or out, or depending on the DPI of the display.</span></span> <span data-ttu-id="cbfb6-259">L’un des avantages secondaires est que l’espacement est vrai pour la conception de la police.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-259">A secondary advantage is that spacing is true to the design of the font.</span></span> <span data-ttu-id="cbfb6-260">La disposition naturelle est rendue possible par la prise en charge de DirectWrite pour le rendu naturel, ce qui signifie que les glyphes individuels peuvent être positionnés sur une fraction d’un pixel.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-260">Natural layout is made possible by DirectWrite's support for natural rendering, which means individual glyphs can be positioned to a fraction of a pixel.</span></span>

<span data-ttu-id="cbfb6-261">Bien que la disposition naturelle soit la valeur par défaut, certaines applications doivent restituer du texte avec le même espace et l’même apparence que GDI.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-261">While natural layout is the default, some applications need to render text with the same spacing and appearance as GDI.</span></span> <span data-ttu-id="cbfb6-262">Pour ces applications, DirectWrite fournit des modes de mesure naturel GDI et GDI classiques et des modes de rendu correspondants.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-262">For such applications, DirectWrite provides GDI classic and GDI natural measuring modes and corresponding rendering modes.</span></span>

<span data-ttu-id="cbfb6-263">L’un des modes de rendu ci-dessus peut être combiné à l’un ou l’autre des deux modes d’anticrénelage : ClearType ou nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-263">Any of the above rendering modes can be combined with either of the two antialiasing modes: ClearType or grayscale.</span></span> <span data-ttu-id="cbfb6-264">L’anticrénelage ClearType simule une résolution plus élevée en manipulant individuellement les valeurs de couleur rouge, verte et bleue de chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-264">ClearType antialiasing simulations a higher resolution by individually manipulating the red, green, and blue color values of each pixel.</span></span> <span data-ttu-id="cbfb6-265">L’anticrénelage de nuances de gris calcule une seule valeur de couverture (ou alpha) pour chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-265">Grayscale antialiasing computes only one coverage (or alpha) value for each pixel.</span></span> <span data-ttu-id="cbfb6-266">ClearType est la valeur par défaut, mais l’anticrénelage en nuances de gris est recommandé pour les applications du Windows Store, car il est plus rapide et compatible avec l’anticrénelage standard, tout en étant très lisible.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-266">ClearType is the default, but grayscale antialiasing is recommended for Windows Store apps because it is faster and is compatible with standard antialiasing, while still being highly readable.</span></span>

## <a name="api-overview"></a><span data-ttu-id="cbfb6-267">Présentation de l’API</span><span class="sxs-lookup"><span data-stu-id="cbfb6-267">API Overview</span></span>

<span data-ttu-id="cbfb6-268">L’interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) est le point de départ pour l’utilisation de la fonctionnalité DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-268">The [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface is the starting point for using DirectWrite functionality.</span></span> <span data-ttu-id="cbfb6-269">La fabrique est l’objet racine qui crée un ensemble d’objets qui peuvent être utilisés ensemble.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-269">The factory is the root object that creates a set of objects that can be used together.</span></span>

<span data-ttu-id="cbfb6-270">L’opération de mise en forme et de mise en page est un prérequis pour les opérations, car le texte doit être correctement mis en forme et disposé sur un ensemble de contraintes spécifié avant de pouvoir être dessiné ou testé.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-270">The formatting and layout operation is a prerequisite to the operations, as text needs to be properly formatted and laid out to a specified set of constraints before it can be drawn or hit-tested.</span></span> <span data-ttu-id="cbfb6-271">Pour ce faire, deux objets clés que vous pouvez créer avec un [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) sont [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="cbfb6-271">Two key objects that you can create with an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) for this purpose are [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="cbfb6-272">Un objet **IDWriteTextFormat** représente les informations de mise en forme d’un paragraphe de texte.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-272">An **IDWriteTextFormat** object represents the formatting information for a paragraph of text.</span></span> <span data-ttu-id="cbfb6-273">La fonction [**IDWriteFactory :: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) prend la chaîne d’entrée, les contraintes associées telles que la dimension de l’espace à remplir et l’objet **IDWriteTextFormat** , puis place le résultat entièrement analysé et mis en forme dans **IDWriteTextLayout** à utiliser dans les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-273">The [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) function takes the input string, the associated constraints such as the dimension of the space to be filled, and the **IDWriteTextFormat** object, and puts the fully analyzed and formatted result into **IDWriteTextLayout** to use in subsequent operations.</span></span>

<span data-ttu-id="cbfb6-274">L’application peut ensuite restituer le texte à l’aide de la fonction [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) fournie par [Direct2D](../direct2d/direct2d-portal.md) ou en implémentant une fonction de rappel qui peut utiliser GDI, Direct2D ou d’autres systèmes graphiques pour restituer les glyphes.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-274">The application can then render the text using the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) function provided by [Direct2D](../direct2d/direct2d-portal.md) or by implementing a callback function that can use GDI, Direct2D, or other graphics systems to render the glyphs.</span></span> <span data-ttu-id="cbfb6-275">Dans le cas d’un texte de format unique, la fonction [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) sur Direct2D offre un moyen plus simple de dessiner du texte sans avoir à créer d’abord un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="cbfb6-275">For a single format text, the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function on Direct2D provides a simpler way to draw text without having to first create a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a><span data-ttu-id="cbfb6-276">Mise en forme et dessin de « Hello World » à l’aide de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="cbfb6-276">Formatting and Drawing "Hello World" Using DirectWrite</span></span>

<span data-ttu-id="cbfb6-277">L’exemple de code suivant montre comment une application peut mettre en forme un seul paragraphe à l’aide de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et la dessiner à l’aide de la fonction [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) de [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb6-277">The following code example shows how an application can format a single paragraph using [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and draw it using the [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function.</span></span>


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a><span data-ttu-id="cbfb6-278">Accès au système de polices</span><span class="sxs-lookup"><span data-stu-id="cbfb6-278">Accessing the Font System</span></span>

<span data-ttu-id="cbfb6-279">En plus de spécifier un nom de famille de polices pour la chaîne de texte à l’aide de l’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) dans l’exemple ci-dessus, [DirectWrite](direct-write-portal.md) offre aux applications davantage de contrôle sur la sélection des polices grâce à l’énumération des polices et à la possibilité de créer une collection de polices personnalisée basée sur des polices de document incorporées.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-279">In addition to specifying a font family name for the text string by using the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface in the example above, [DirectWrite](direct-write-portal.md) provides applications more control over font selection through font enumeration and the ability to create custom font collection based on embedded document fonts.</span></span>

<span data-ttu-id="cbfb6-280">L’objet [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) est une collection de familles de polices.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-280">The [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) object is a collection of font families.</span></span> <span data-ttu-id="cbfb6-281">DirectWrite permet d’accéder à l’ensemble de polices installées sur le système par le biais d’une collection de polices spéciale appelée collection de polices système.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-281">DirectWrite provides access to the set of fonts installed on the system through a special font collection called the system font collection.</span></span> <span data-ttu-id="cbfb6-282">Cela est obtenu en appelant la méthode [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) de l’objet [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="cbfb6-282">This is obtained by calling the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) object.</span></span> <span data-ttu-id="cbfb6-283">Une application peut également créer une collection de polices personnalisée à partir d’un ensemble de polices énumérées par un rappel défini par l’application, c’est-à-dire des polices privées installées par une application, ou des polices incorporées dans un document.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-283">An application can also create a custom font collection from a set of fonts enumerated by an application-defined callback, that is, private fonts installed by an application, or fonts embedded in a document.</span></span>

<span data-ttu-id="cbfb6-284">L’application peut ensuite appeler [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) pour accéder à un objet FontFamily spécifique dans la collection, puis appeler [**IDWriteFontFamily :: GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) pour atteindre un objet [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) spécifique.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-284">The application can then call [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) to get to a specific FontFamily object within the collection, and then call [**IDWriteFontFamily::GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) to get to a specific [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object.</span></span> <span data-ttu-id="cbfb6-285">L’objet **IDWriteFont** représente une police dans une collection de polices et expose des propriétés et quelques métriques de police de base.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-285">The **IDWriteFont** object represents a font in a font collection and exposes properties and a few basic font metrics.</span></span>

<span data-ttu-id="cbfb6-286">[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) est un autre objet qui représente une police et expose un jeu complet de métriques sur une police.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-286">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) is another object that represents a font and exposes a full set of metrics on a font.</span></span> <span data-ttu-id="cbfb6-287">Le **IDWriteFontFace** peut être créé directement à partir d’un nom de police ; une application n’a pas besoin d’obtenir une collection de polices pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-287">The **IDWriteFontFace** can be created directly from a font name; an application does not have to get a font collection to access it.</span></span> <span data-ttu-id="cbfb6-288">Elle est utile pour une application de disposition de texte telle que Microsoft Word qui doit interroger les détails d’une police spécifique.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-288">It is useful for a text layout application such as Microsoft Word that needs to query the details for a specific font.</span></span>

<span data-ttu-id="cbfb6-289">Le diagramme suivant illustre la relation entre ces objets.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-289">The following diagram illustrates the relationship between these objects.</span></span>

![diagramme de la relation entre une collection de polices, une famille de polices et un type de police](images/fontcollection.png)

### <a name="idwritefontface"></a><span data-ttu-id="cbfb6-291">IDWriteFontFace</span><span class="sxs-lookup"><span data-stu-id="cbfb6-291">IDWriteFontFace</span></span>

<span data-ttu-id="cbfb6-292">L’objet [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) représente une police et fournit des informations plus détaillées sur la police que l’objet [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) .</span><span class="sxs-lookup"><span data-stu-id="cbfb6-292">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object represents a font and provides more detailed information about the font than the [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object does.</span></span> <span data-ttu-id="cbfb6-293">Les métriques de police et de glyphe du **IDWriteFontFace** sont utiles pour les applications qui implémentent la disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-293">The font and glyph metrics from the **IDWriteFontFace** are useful for applications that implement text layout.</span></span>

<span data-ttu-id="cbfb6-294">La plupart des applications courantes n’utilisent pas directement ces API et utilisent [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) ou spécifient directement le nom de famille de polices.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-294">Most mainstream applications will not use these APIs directly, and instead will use [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) or specify the font family name directly.</span></span>

<span data-ttu-id="cbfb6-295">Le tableau suivant récapitule les scénarios d’utilisation des deux objets.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-295">The following table summarizes the usage scenarios for the two objects.</span></span>



| <span data-ttu-id="cbfb6-296">Category</span><span class="sxs-lookup"><span data-stu-id="cbfb6-296">Category</span></span>                                                                                                         | [<span data-ttu-id="cbfb6-297">**IDWriteFont**</span><span class="sxs-lookup"><span data-stu-id="cbfb6-297">**IDWriteFont**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [<span data-ttu-id="cbfb6-298">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="cbfb6-298">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="cbfb6-299">API pour prendre en charge l’interaction de l’utilisateur, telle qu’une interface utilisateur de sélection de polices : description et autres API d’informations</span><span class="sxs-lookup"><span data-stu-id="cbfb6-299">APIs to support user interaction such as a font-chooser user interface: description and other informational APIs</span></span> | <span data-ttu-id="cbfb6-300">Oui</span><span class="sxs-lookup"><span data-stu-id="cbfb6-300">Yes</span></span>                                        | <span data-ttu-id="cbfb6-301">Non</span><span class="sxs-lookup"><span data-stu-id="cbfb6-301">No</span></span>                                                 |
| <span data-ttu-id="cbfb6-302">API pour la prise en charge du mappage des polices : famille, style, poids, étirement, couverture des caractères</span><span class="sxs-lookup"><span data-stu-id="cbfb6-302">APIs to support font mapping: family, style, weight, stretch, character coverage</span></span>                                 | <span data-ttu-id="cbfb6-303">Oui</span><span class="sxs-lookup"><span data-stu-id="cbfb6-303">Yes</span></span>                                        | <span data-ttu-id="cbfb6-304">Non</span><span class="sxs-lookup"><span data-stu-id="cbfb6-304">No</span></span>                                                 |
| <span data-ttu-id="cbfb6-305">API DrawText</span><span class="sxs-lookup"><span data-stu-id="cbfb6-305">DrawText API</span></span>                                                                                                     | <span data-ttu-id="cbfb6-306">Oui</span><span class="sxs-lookup"><span data-stu-id="cbfb6-306">Yes</span></span>                                        | <span data-ttu-id="cbfb6-307">Non</span><span class="sxs-lookup"><span data-stu-id="cbfb6-307">No</span></span>                                                 |
| <span data-ttu-id="cbfb6-308">API utilisées pour le rendu</span><span class="sxs-lookup"><span data-stu-id="cbfb6-308">APIs used for rendering</span></span>                                                                                          | <span data-ttu-id="cbfb6-309">Non</span><span class="sxs-lookup"><span data-stu-id="cbfb6-309">No</span></span>                                         | <span data-ttu-id="cbfb6-310">Oui</span><span class="sxs-lookup"><span data-stu-id="cbfb6-310">Yes</span></span>                                                |
| <span data-ttu-id="cbfb6-311">API utilisées pour la disposition du texte : métriques de glyphe, etc.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-311">APIs used for text layout: glyph metrics, and so on</span></span>                                                              | <span data-ttu-id="cbfb6-312">Non</span><span class="sxs-lookup"><span data-stu-id="cbfb6-312">No</span></span>                                         | <span data-ttu-id="cbfb6-313">Oui</span><span class="sxs-lookup"><span data-stu-id="cbfb6-313">Yes</span></span>                                                |
| <span data-ttu-id="cbfb6-314">API pour le contrôle de l’interface utilisateur et la disposition du texte : métriques à l’ensemble des polices</span><span class="sxs-lookup"><span data-stu-id="cbfb6-314">APIs for UI control and text layout: font-wide metrics</span></span>                                                           | <span data-ttu-id="cbfb6-315">Oui</span><span class="sxs-lookup"><span data-stu-id="cbfb6-315">Yes</span></span>                                        | <span data-ttu-id="cbfb6-316">Oui</span><span class="sxs-lookup"><span data-stu-id="cbfb6-316">Yes</span></span>                                                |



 

<span data-ttu-id="cbfb6-317">Voici un exemple d’application qui énumère les polices de la collection de polices système.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-317">The following is an example application that enumerates the fonts in the system font collection.</span></span>


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a><span data-ttu-id="cbfb6-318">Rendu du texte</span><span class="sxs-lookup"><span data-stu-id="cbfb6-318">Text rendering</span></span>

<span data-ttu-id="cbfb6-319">Les API de rendu de texte permettent le rendu des glyphes dans une police [DirectWrite](direct-write-portal.md) sur une surface [Direct2D](../direct2d/direct2d-portal.md) ou une image bitmap indépendante du périphérique GDI, ou à convertir en plans ou bitmaps.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-319">The text rendering APIs enable glyphs in a [DirectWrite](direct-write-portal.md) font to be rendered to a [Direct2D](../direct2d/direct2d-portal.md) surface or to a GDI device independent bitmap, or to be converted to outlines or bitmaps.</span></span> <span data-ttu-id="cbfb6-320">Le rendu ClearType dans DirectWrite prend en charge le positionnement des sous-pixels avec une netteté et un contraste améliorés par rapport aux implémentations précédentes sur Windows.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-320">The ClearType rendering in DirectWrite supports sub-pixel positioning with improved sharpness and contrast compared to previous implementations on Windows.</span></span> <span data-ttu-id="cbfb6-321">DirectWrite prend également en charge le texte noir et blanc avec alias pour prendre en charge les scénarios impliquant des polices d’Extrême-Orient avec des bitmaps incorporées, ou lorsque l’utilisateur a désactivé le lissage des polices de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-321">DirectWrite also supports aliased black-and-white text to support scenarios involving East Asian fonts with embedded bitmaps, or where the user has disabled font smoothing of any type.</span></span>

<span data-ttu-id="cbfb6-322">Toutes les options sont réglables par tous les boutons ClearType disponibles accessibles par le biais des API [DirectWrite](direct-write-portal.md) , ainsi que par l’intermédiaire de la nouvelle applet du panneau de configuration du tuner ClearType Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-322">All the options are adjustable by all the available ClearType knobs accessible through the [DirectWrite](direct-write-portal.md) APIs, and also exposed via the new Windows 7 ClearType tuner control panel applet.</span></span>

<span data-ttu-id="cbfb6-323">Deux API sont disponibles pour le rendu des glyphes : l’un fournissant un rendu accéléré par le matériel via [Direct2D](../direct2d/direct2d-portal.md) et l’autre fournissant un rendu logiciel à une image bitmap GDI.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-323">There are two APIs available for rendering glyphs, one providing hardware-accelerated rendering through [Direct2D](../direct2d/direct2d-portal.md) and the other providing software rendering to a GDI bitmap.</span></span> <span data-ttu-id="cbfb6-324">Une application utilisant [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) et l’implémentation du rappel [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) peuvent appeler l’une de ces fonctions en réponse à un rappel [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="cbfb6-324">An application using [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) and implementing the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) callback can call either of these functions in response to a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback.</span></span> <span data-ttu-id="cbfb6-325">En outre, les applications qui implémentent leur propre disposition ou gèrent les données de niveau glyphe peuvent utiliser ces API.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-325">Also, applications that implement their own layout or deal with glyph-level data can use these APIs.</span></span>

1.  [<span data-ttu-id="cbfb6-326">**ID2DRenderTarget ::D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="cbfb6-326">**ID2DRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    <span data-ttu-id="cbfb6-327">Les applications peuvent utiliser l’API [Direct2D](../direct2d/direct2d-portal.md) [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) pour fournir une accélération matérielle pour le rendu de texte à l’aide du GPU.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-327">Applications can use the [Direct2D](../direct2d/direct2d-portal.md) API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) to provide hardware acceleration for text rendering using the GPU.</span></span> <span data-ttu-id="cbfb6-328">L’accélération matérielle affecte toutes les phases du pipeline de rendu de texte, de la fusion des glyphes aux exécutions de glyphes et du filtrage de la bitmap d’exécution de glyphes, à l’application de l’algorithme de fusion ClearType à la sortie affichée finale.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-328">Hardware acceleration affects all phases of the text rendering pipeline—from merging glyphs into glyph runs and filtering the glyph-run bitmap, to applying the ClearType blending algorithm to the final displayed output.</span></span> <span data-ttu-id="cbfb6-329">Il s’agit de l’API recommandée pour obtenir les meilleures performances de rendu.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-329">This is the recommended API for getting the best rendering performance.</span></span>

2.  [<span data-ttu-id="cbfb6-330">**IDWriteBitmapRenderTarget ::D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="cbfb6-330">**IDWriteBitmapRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    <span data-ttu-id="cbfb6-331">Les applications peuvent utiliser la méthode [**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) pour effectuer un rendu logiciel d’une série de glyphes dans une image bitmap 32-BPP.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-331">Applications can use the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to perform a software-rendering of a run of glyphs to a 32-bpp bitmap.</span></span> <span data-ttu-id="cbfb6-332">L’objet [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsule une image bitmap et un contexte de périphérique de mémoire qui peut être utilisé pour le rendu des glyphes.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-332">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object encapsulates a bitmap and a memory device context that can be used for rendering glyphs.</span></span> <span data-ttu-id="cbfb6-333">Cette API est utile si vous souhaitez rester avec GDI, car vous disposez d’une base de code existante qui s’affiche dans GDI.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-333">This API is useful if you want to stay with GDI because you have an existing code base that renders in GDI.</span></span>

<span data-ttu-id="cbfb6-334">Si vous disposez d’une application qui possède un code de disposition de texte qui utilise GDI et que vous souhaitez conserver son code de disposition existant mais utiliser [DirectWrite](direct-write-portal.md) uniquement pour l’étape finale du rendu des glyphes, [**IDWriteGdiInterop :: CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) fournit le pont entre les deux API.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-334">If you have an application that has existing text layout code that uses GDI, and you want to preserve its existing layout code but use [DirectWrite](direct-write-portal.md) just for the final step of rendering glyphs, [**IDWriteGdiInterop::CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) provides the bridge between the two APIs.</span></span> <span data-ttu-id="cbfb6-335">Avant d’appeler cette fonction, l’application utilise la fonction **IDWriteGdiInterop :: CreateFontFaceFromHdc** pour obtenir une référence de type font-face d’un contexte de périphérique (Device Context).</span><span class="sxs-lookup"><span data-stu-id="cbfb6-335">Before calling this function, the application will use the **IDWriteGdiInterop::CreateFontFaceFromHdc** function to get a font-face reference from a device context.</span></span>

> [!Note]  
> <span data-ttu-id="cbfb6-336">Pour la plupart des scénarios, les applications n’ont peut-être pas besoin d’utiliser ces API de rendu de glyphe.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-336">For most scenarios, applications may not need to use these glyph-rendering APIs.</span></span> <span data-ttu-id="cbfb6-337">Une fois qu’une application a créé un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , elle peut utiliser la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) pour restituer le texte.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-337">After an application has created an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, it can use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method to render the text.</span></span>

 

## <a name="custom-rendering-modes"></a><span data-ttu-id="cbfb6-338">Modes de rendu personnalisés</span><span class="sxs-lookup"><span data-stu-id="cbfb6-338">Custom Rendering Modes</span></span>

<span data-ttu-id="cbfb6-339">Un certain nombre de paramètres affectent le rendu du texte, tels que gamma, le niveau ClearType, la géométrie des pixels et le contraste amélioré.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-339">A number of parameters affect text rendering, such as gamma, ClearType level, pixel geometry, and enhanced contrast.</span></span> <span data-ttu-id="cbfb6-340">Les paramètres de rendu sont encapsulés par un objet, qui implémente l’interface [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) publique.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-340">Rendering parameters are encapsulated by an object, which implements the public [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) interface.</span></span> <span data-ttu-id="cbfb6-341">L’objet de paramètres de rendu est initialisé automatiquement en fonction des propriétés matérielles et/ou des préférences de l’utilisateur spécifiées par le biais de l’applet du panneau de configuration ClearType dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-341">The rendering parameters object is automatically initialized based on hardware properties and/or user preferences specified through the ClearType control panel applet in Windows 7.</span></span> <span data-ttu-id="cbfb6-342">En règle générale, si un client utilise l’API de disposition [DirectWrite](direct-write-portal.md) , DirectWrite sélectionne automatiquement un mode de rendu qui correspond au mode de mesure spécifié.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-342">Generally, if a client uses the [DirectWrite](direct-write-portal.md) layout API, DirectWrite will automatically select a rendering mode that corresponds to the specified measuring mode.</span></span>

<span data-ttu-id="cbfb6-343">Les applications qui souhaitent davantage de contrôle peuvent utiliser [**IDWriteFactory :: CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) pour implémenter les différentes options de rendu.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-343">Applications that want more control can use [**IDWriteFactory::CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) to implement the different rendering options.</span></span> <span data-ttu-id="cbfb6-344">Cette fonction peut également être utilisée pour définir la valeur gamma, la géométrie des pixels et le contraste amélioré.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-344">This function can also be used to set the gamma, pixel geometry, and enhanced contrast.</span></span>

<span data-ttu-id="cbfb6-345">Voici les différentes options de rendu disponibles :</span><span class="sxs-lookup"><span data-stu-id="cbfb6-345">The following are the various rendering options available:</span></span>

-   <span data-ttu-id="cbfb6-346">Anticrénelage de sous-pixel</span><span class="sxs-lookup"><span data-stu-id="cbfb6-346">Sub-pixel anti-aliasing</span></span>

    <span data-ttu-id="cbfb6-347">L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE \_ \_ naturel pour spécifier le rendu avec anticrénelage dans la dimension horizontale uniquement.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-347">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL to specify rendering with anti-aliasing in the horizontal dimension only.</span></span>

-   <span data-ttu-id="cbfb6-348">Anticrénelage de sous-pixel dans les dimensions horizontales et verticales.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-348">Sub-pixel anti-aliasing in both horizontal and vertical dimensions.</span></span>

    <span data-ttu-id="cbfb6-349">L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE \_ \_ Natural \_ symétrique pour spécifier le rendu avec anticrénelage à la fois dans les dimensions horizontales et verticales.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-349">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL\_SYMMETRIC to specify rendering with anti-aliasing in both horizontal and vertical dimensions.</span></span> <span data-ttu-id="cbfb6-350">Cela rend les courbes et les lignes diagonales plus lisses au détriment d’une certaine douceur, et est généralement utilisée à des tailles supérieures à 16 ppem.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-350">This makes curves and diagonal lines look smoother at the expense of some softness, and is typically used at sizes above 16 ppem.</span></span>

-   <span data-ttu-id="cbfb6-351">Texte avec alias</span><span class="sxs-lookup"><span data-stu-id="cbfb6-351">Aliased Text</span></span>

    <span data-ttu-id="cbfb6-352">L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE avec un \_ \_ alias pour spécifier un alias de texte.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-352">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_ALIASED to specify aliased text.</span></span>

-   <span data-ttu-id="cbfb6-353">Texte en nuances de gris</span><span class="sxs-lookup"><span data-stu-id="cbfb6-353">Grayscale Text</span></span>

    <span data-ttu-id="cbfb6-354">L’application définit le paramètre *pixelGeometry* sur DWRITE \_ pixel \_ Geometry \_ Flat pour spécifier un texte en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-354">The application sets the *pixelGeometry* parameter to DWRITE\_PIXEL\_GEOMETRY\_FLAT to specify grayscale text.</span></span>

-   <span data-ttu-id="cbfb6-355">Compatible GDI-largeur (y compris l’image bitmap incorporée d’Extrême-Orient)</span><span class="sxs-lookup"><span data-stu-id="cbfb6-355">GDI compatible-width (including East Asian embedded bitmap)</span></span>

    <span data-ttu-id="cbfb6-356">L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE \_ \_ GDI Classic pour spécifier l’anticrénelage de \_ largeur compatible GDI.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-356">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC to specify GDI compatible-width anti-aliasing.</span></span>

-   <span data-ttu-id="cbfb6-357">GDI-largeur naturelle</span><span class="sxs-lookup"><span data-stu-id="cbfb6-357">GDI natural-width</span></span>

    <span data-ttu-id="cbfb6-358">L’application définit le paramètre *renderingMode* sur le \_ mode de rendu DWRITE \_ \_ GDI \_ Natural pour spécifier l’anticrénelage compatible GDI en largeur naturelle.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-358">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_NATURAL to specify GDI natural-width compatible anti-aliasing.</span></span>

-   <span data-ttu-id="cbfb6-359">Texte du plan</span><span class="sxs-lookup"><span data-stu-id="cbfb6-359">Outline text</span></span>

    <span data-ttu-id="cbfb6-360">Pour un rendu de grande taille, un développeur d’applications peut préférer le rendu à l’aide de la structure de police plutôt que de la pixellisation dans une bitmap.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-360">For rendering at large sizes, an application developer might prefer to render by using the font outline rather than by rasterizing into a bitmap.</span></span> <span data-ttu-id="cbfb6-361">L’application définit le paramètre *renderingMode* sur **\_ \_ \_ plan du mode de rendu DWRITE** pour spécifier que le rendu doit contourner le rastériseur et utiliser directement les contours.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-361">The application sets the *renderingMode* parameter to **DWRITE\_RENDERING\_MODE\_OUTLINE** to specify that rendering should bypass the rasterizer and use the outlines directly.</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="cbfb6-362">Interopérabilité GDI</span><span class="sxs-lookup"><span data-stu-id="cbfb6-362">GDI Interoperability</span></span>

<span data-ttu-id="cbfb6-363">L’interface [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) fournit une interopérabilité avec GDI.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-363">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface provides interoperability with GDI.</span></span> <span data-ttu-id="cbfb6-364">Cela permet aux applications de poursuivre leurs investissements existants dans les bases de code GDI et d’utiliser de manière sélective [DirectWrite](direct-write-portal.md) pour le rendu ou la mise en page.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-364">This enables applications to continue their existing investment in GDI code bases and selectively use [DirectWrite](direct-write-portal.md) for either rendering or layout.</span></span>

<span data-ttu-id="cbfb6-365">Voici les API qui permettent à une application de migrer vers ou à partir du système de polices GDI :</span><span class="sxs-lookup"><span data-stu-id="cbfb6-365">The following are the APIs that enable an application to migrate to or from the GDI font system:</span></span>

-   [<span data-ttu-id="cbfb6-366">**CreateFontFromLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="cbfb6-366">**CreateFontFromLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    <span data-ttu-id="cbfb6-367">Crée un objet [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) qui correspond aux propriétés spécifiées par la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="cbfb6-367">Creates an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object that matches the properties specified by the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

-   [<span data-ttu-id="cbfb6-368">**ConvertFontToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="cbfb6-368">**ConvertFontToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    <span data-ttu-id="cbfb6-369">Initialise une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basée sur les propriétés compatibles GDI du [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)spécifié.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-369">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).</span></span>

-   [<span data-ttu-id="cbfb6-370">**ConvertFontFaceToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="cbfb6-370">**ConvertFontFaceToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    <span data-ttu-id="cbfb6-371">Initialise une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basée sur les propriétés compatibles GDI du [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)spécifié.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-371">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).</span></span>

-   [<span data-ttu-id="cbfb6-372">**CreateFontFaceFromHdc**</span><span class="sxs-lookup"><span data-stu-id="cbfb6-372">**CreateFontFaceFromHdc**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    <span data-ttu-id="cbfb6-373">Crée un objet [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) qui correspond au **Hfont** actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-373">Creates an [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object that corresponds to the currently selected **HFONT**.</span></span>

## <a name="conclusion"></a><span data-ttu-id="cbfb6-374">Conclusion</span><span class="sxs-lookup"><span data-stu-id="cbfb6-374">Conclusion</span></span>

<span data-ttu-id="cbfb6-375">L’amélioration de l’expérience de lecture est très intéressante pour les utilisateurs, qu’ils soient sur l’écran ou sur papier.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-375">Improving the reading experience is of great value to users whether it is on the screen or on paper.</span></span> <span data-ttu-id="cbfb6-376">[DirectWrite](direct-write-portal.md) offre la facilité d’utilisation et le modèle de programmation en couches pour les développeurs d’applications afin d’améliorer l’expérience de texte pour leurs applications Windows.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-376">[DirectWrite](direct-write-portal.md) provides the ease of use and the layered programming model for application developers to improve the text experience for their Windows applications.</span></span> <span data-ttu-id="cbfb6-377">Les applications peuvent utiliser DirectWrite pour restituer un texte riche en format pour leur interface utilisateur et leurs documents avec l’API Layout.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-377">Applications can use DirectWrite to render richly formatted text for their UI and documents with the layout API.</span></span> <span data-ttu-id="cbfb6-378">Pour les scénarios plus complexes, une application peut fonctionner directement avec des glyphes, accéder aux polices, etc. et exploiter la puissance de DirectWrite pour fournir une typographie de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-378">For more complex scenarios, an application can work directly with glyphs, access fonts, and so on, and harness the power of DirectWrite to deliver high-quality typography.</span></span>

<span data-ttu-id="cbfb6-379">Les fonctionnalités d’interopérabilité de [DirectWrite](direct-write-portal.md) permettent aux développeurs d’applications de transférer leurs codes base Win32 existants et d’adopter DirectWrite de manière sélective au sein de leurs applications.</span><span class="sxs-lookup"><span data-stu-id="cbfb6-379">The interoperability capabilities of [DirectWrite](direct-write-portal.md) enable application developers to carry forward their existing Win32 codebases and adopt DirectWrite selectively within their applications.</span></span>

 

 