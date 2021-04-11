---
title: Format de presse-papiers HTML
description: Cette section décrit le format de presse-papiers HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Interface utilisateur Windows, presse-papiers
- presse-papiers, découper des données
- presse-papiers, copier des données
- presse-papiers, coller des données
- presse-papiers, formats
- presse-papiers, format HTML
- presse-papiers, couper du texte HTML
- presse-papiers, coller du texte HTML
- Format du presse-papiers CF_HTML
- presse-papiers, format CF_HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029383"
---
# <a name="html-clipboard-format"></a><span data-ttu-id="a4992-113">Format de presse-papiers HTML</span><span class="sxs-lookup"><span data-stu-id="a4992-113">HTML Clipboard Format</span></span>

<span data-ttu-id="a4992-114">La configuration requise pour le transfert de texte HTML au moyen du presse-papiers diffère selon le scénario.</span><span class="sxs-lookup"><span data-stu-id="a4992-114">The requirements for transferring HTML text by means of the clipboard differ depending on scenario.</span></span> <span data-ttu-id="a4992-115">Cet article s’intéresse à la coupe et au collage de fragments d’un document HTML.</span><span class="sxs-lookup"><span data-stu-id="a4992-115">This article is concerned with cutting and pasting fragments of an HTML document.</span></span> <span data-ttu-id="a4992-116">Il peut y avoir des conditions requises pour le transfert de documents HTML entiers dans le presse-papiers. Toutefois, cet article est piloté par une nécessité de transférer des fragments de texte HTML sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a4992-116">There may be requirements for transferring entire HTML documents through the clipboard; however, this article is driven by a requirement to transfer fragments of selected HTML text.</span></span> <span data-ttu-id="a4992-117">Par conséquent, une méthode qui nécessitait la copie de l’intégralité du document HTML dans le presse-papiers s’affiche comme trop haute.</span><span class="sxs-lookup"><span data-stu-id="a4992-117">As such, a method that required the entire HTML document to be copied to the clipboard is seen as too heavyweight.</span></span>

<span data-ttu-id="a4992-118">Le \_ format de presse-papiers html CF permet de stocker un fragment de texte HTML brut et son contexte dans le presse-papiers au format ASCII.</span><span class="sxs-lookup"><span data-stu-id="a4992-118">The CF\_HTML clipboard format allows a fragment of raw HTML text and its context to be stored on the clipboard as ASCII.</span></span> <span data-ttu-id="a4992-119">Cela permet au contexte du fragment HTML, qui se compose de toutes les balises précédentes, d’être examiné par une application afin que les balises environnantes du fragment HTML puissent être notées avec leurs attributs.</span><span class="sxs-lookup"><span data-stu-id="a4992-119">This allows the context of the HTML fragment, which consists of all preceding surrounding tags, to be examined by an application so that the surrounding tags of the HTML fragment can be noted with their attributes.</span></span> <span data-ttu-id="a4992-120">Bien qu’il s’agisse d’applications pour décider de l’interprétation de tels fragments, certaines recommandations de base sont incluses ici en fonction des implémentations de IE4/MSHTML.</span><span class="sxs-lookup"><span data-stu-id="a4992-120">Although it is up to applications to decide how to interpret such fragments, some basic guidelines are included here based on IE4/MSHTML implementations.</span></span>

<span data-ttu-id="a4992-121">Le nom officiel du presse-papiers (la chaîne utilisée par RegisterClipboardFormat) est au format HTML.</span><span class="sxs-lookup"><span data-stu-id="a4992-121">The official name of the clipboard (the string used by RegisterClipboardFormat) is HTML Format.</span></span>

-   [<span data-ttu-id="a4992-122">Description</span><span class="sxs-lookup"><span data-stu-id="a4992-122">Description</span></span>](#description)
-   [<span data-ttu-id="a4992-123">Scénarios</span><span class="sxs-lookup"><span data-stu-id="a4992-123">Scenarios</span></span>](#scenarios)

## <a name="description"></a><span data-ttu-id="a4992-124">Description</span><span class="sxs-lookup"><span data-stu-id="a4992-124">Description</span></span>

<span data-ttu-id="a4992-125">CF \_ HTML est un format de texte intégral (c’est-à-dire, entre autres choses, dans l’esprit html et utilise UTF-8) et comprend un `description` , un facultatif `context` et, dans le contexte, le `fragment` .</span><span class="sxs-lookup"><span data-stu-id="a4992-125">CF\_HTML is entirely text format (to be, among other things, in the HTML spirit, and uses UTF-8) and includes a `description`, an optional `context`, and, within the context, the `fragment`.</span></span>

<span data-ttu-id="a4992-126">Voici un exemple de presse-papiers :</span><span class="sxs-lookup"><span data-stu-id="a4992-126">The following is an example of a clipboard:</span></span>


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



<span data-ttu-id="a4992-127">La description comprend le numéro de version et les décalages du presse-papiers, indiquant où le contexte et le début et la fin du fragment.</span><span class="sxs-lookup"><span data-stu-id="a4992-127">The description includes the clipboard version number and offsets, indicating where the context and the fragment start and end.</span></span> <span data-ttu-id="a4992-128">La description est une liste de mots clés de texte ASCII (min/Maj n’est pas significative) suivie d’une chaîne et séparée par un signe deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="a4992-128">The description is a list of ASCII text keywords (min/maj is not meaningful) followed by a string and separated by a colon (:).</span></span>

<span data-ttu-id="a4992-129">**Version**: numéro de version VV du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a4992-129">**Version**: vv version number of the clipboard.</span></span> <span data-ttu-id="a4992-130">La version de démarrage est 0,9.</span><span class="sxs-lookup"><span data-stu-id="a4992-130">Starting version is 0.9.</span></span>

<span data-ttu-id="a4992-131">**StartHTML**: byteCount du début du presse-papiers jusqu’au début du contexte, ou-1 si aucun contexte n’est présent.</span><span class="sxs-lookup"><span data-stu-id="a4992-131">**StartHTML**: bytecount from the beginning of the clipboard to the start of the context, or -1 if no context.</span></span>

<span data-ttu-id="a4992-132">**Polydhtml**: byteCount du début du presse-papiers jusqu’à la fin du contexte, ou-1 si aucun contexte n’est présent.</span><span class="sxs-lookup"><span data-stu-id="a4992-132">**EndHTML**: bytecount from the beginning of the clipboard to the end of the context, or -1 if no context.</span></span>

<span data-ttu-id="a4992-133">**StartFragment**: byteCount du début du presse-papiers jusqu’au début du fragment.</span><span class="sxs-lookup"><span data-stu-id="a4992-133">**StartFragment**: bytecount from the beginning of the clipboard to the start of the fragment.</span></span>

<span data-ttu-id="a4992-134">**EndFragment**: byteCount du début du presse-papiers jusqu’à la fin du fragment.</span><span class="sxs-lookup"><span data-stu-id="a4992-134">**EndFragment**: bytecount from the beginning of the clipboard to the end of the fragment.</span></span>

<span data-ttu-id="a4992-135">**StartSelection**: byteCount du début du presse-papiers jusqu’au début de la sélection.</span><span class="sxs-lookup"><span data-stu-id="a4992-135">**StartSelection**: bytecount from the beginning of the clipboard to the start of the selection.</span></span>

<span data-ttu-id="a4992-136">**EndSelection**: byteCount du début du presse-papiers jusqu’à la fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="a4992-136">**EndSelection**: bytecount from the beginning of the clipboard to the end of the selection.</span></span>

<span data-ttu-id="a4992-137">Les mots clés StartSelection et EndSelection sont facultatifs et doivent tous deux être omis si vous ne souhaitez pas que l’application génère ces informations.</span><span class="sxs-lookup"><span data-stu-id="a4992-137">The StartSelection and EndSelection keywords are optional and must both be omitted if you do not want the application to generate this information.</span></span>

<span data-ttu-id="a4992-138">D’autres informations de ce genre peuvent être ajoutées ici plus tard, puisque le code HTML commence au StartHTMLoffset.</span><span class="sxs-lookup"><span data-stu-id="a4992-138">Other information of this kind could be added here later, since the HTML starts at the StartHTMLoffset.</span></span> <span data-ttu-id="a4992-139">Par exemple, plusieurs paires de StartFragment/EndFragment peuvent être ajoutées ultérieurement pour prendre en charge une sélection non contiguë de fragments.</span><span class="sxs-lookup"><span data-stu-id="a4992-139">For example, multiple pairs of StartFragment / EndFragment could be added later to support noncontiguous selection of fragments.</span></span>

<span data-ttu-id="a4992-140">Pour la commodité des programmes qui génèrent le bytecounts, les bytecounts peuvent être laissés remplis par des zéros.</span><span class="sxs-lookup"><span data-stu-id="a4992-140">For the convenience of the programs generating the bytecounts, bytecounts could be left padded by zeros.</span></span> <span data-ttu-id="a4992-141">Par exemple, les programmes qui génèrent le bytecounts peuvent avoir un impact arbitraire sur dix (10) zéros pour chaque mot clé (StartHTML : 0000000000), puis, lorsque l’byteCount exact de StartHTML est connu (par exemple, 71), le programme peut remplacer le nombre approprié de zéros par le byteCount (StartHTML : 0000000071).</span><span class="sxs-lookup"><span data-stu-id="a4992-141">For example, programs generating the bytecounts could arbitrarily affect ten (10) zeros to each keyword (StartHTML: 0000000000) and then, when the exact StartHTML bytecount is known (say, 71), the program can replace the appropriate number of zeros by the bytecount (StartHTML: 0000000071).</span></span>

<span data-ttu-id="a4992-142">Le seul jeu de caractères pris en charge par le presse-papiers est Unicode dans son encodage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="a4992-142">The only character set supported by the clipboard is Unicode in its UTF-8 encoding.</span></span> <span data-ttu-id="a4992-143">Étant donné que les premiers caractères d’UTF-8 et d’ASCII correspondent, la description est toujours ASCII, mais les octets du contexte (à partir de StartHTML) peuvent utiliser n’importe quel autre caractère codé au format UTF-8.</span><span class="sxs-lookup"><span data-stu-id="a4992-143">Because the first characters of UTF-8 and ASCII match, the description is always ASCII, but the bytes of the context (starting at StartHTML) could be using any other characters coded in UTF-8.</span></span>

<span data-ttu-id="a4992-144">La fin des lignes dans l’en-tête du format du presse-papiers peut être CR ou CR/LF ou LF.</span><span class="sxs-lookup"><span data-stu-id="a4992-144">End of lines in the clipboard format header could be CR or CR/LF or LF.</span></span>

<span data-ttu-id="a4992-145">Le fragment contient du code HTML pur et valide qui représente la zone sélectionnée par l’utilisateur (pour la copie, par exemple).</span><span class="sxs-lookup"><span data-stu-id="a4992-145">The fragment contains pure, valid HTML representing the area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="a4992-146">Il contient le texte sélectionné, ainsi que les balises d’ouverture et les attributs d’un élément qui a une balise de fin dans le texte sélectionné, et des balises de fin à la fin du fragment pour toute balise de début incluse.</span><span class="sxs-lookup"><span data-stu-id="a4992-146">This contains the selected text plus the opening tags and attributes of any element that has an end tag within the selected text, and end tags at the end of the fragment for any start tag included.</span></span> <span data-ttu-id="a4992-147">Il s’agit de toutes les informations requises pour le collage de base d’un fragment HTML.</span><span class="sxs-lookup"><span data-stu-id="a4992-147">This is all information required for basic pasting of an HTML fragment.</span></span>

<span data-ttu-id="a4992-148">Le fragment doit être précédé et suivi des commentaires HTML</span><span class="sxs-lookup"><span data-stu-id="a4992-148">The fragment should be preceded and followed by the HTML comments</span></span> <!--StartFragment--> <span data-ttu-id="a4992-149">et</span><span class="sxs-lookup"><span data-stu-id="a4992-149">and</span></span> <!--EndFragment--> <span data-ttu-id="a4992-150">(aucun espace n’est autorisé entre le !--et le texte) pour indiquer facilement où le fragment démarre et se termine.</span><span class="sxs-lookup"><span data-stu-id="a4992-150">(no space allowed between the !-- and the text) to conveniently indicate where the fragment starts and ends.</span></span> <span data-ttu-id="a4992-151">Par conséquent, le début et la fin du fragment sont indiqués par la présence de ces commentaires et par le nombre d’octets StartFragment et EndFragment dans la description.</span><span class="sxs-lookup"><span data-stu-id="a4992-151">Thus the start and end of the fragment are indicated by the presence of these comments and by StartFragment and EndFragment byte counts in the description.</span></span> <span data-ttu-id="a4992-152">Les outils sont censés produire ces informations.</span><span class="sxs-lookup"><span data-stu-id="a4992-152">Tools are expected to produce this information.</span></span> <span data-ttu-id="a4992-153">Cette redondance a été introduite pour pouvoir trouver rapidement le début du fragment (à partir du nombre d’octets) et marquer la position du fragment directement dans l’arborescence HTML.</span><span class="sxs-lookup"><span data-stu-id="a4992-153">This redundancy has been introduced to be able to rapidly find the start of the fragment (from the byte count) and mark the position of the fragment directly in the HTML tree.</span></span>

<span data-ttu-id="a4992-154">La sélection indique à l’intérieur du fragment la zone HTML exacte que l’utilisateur a sélectionnée (pour la copie, par exemple).</span><span class="sxs-lookup"><span data-stu-id="a4992-154">The selection indicates inside the fragment the exact HTML area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="a4992-155">Cela ajoute plus d’informations au fragment en indiquant le texte exact sélectionné, sans les balises d’ouverture et de fin qui ont été ajoutées pour s’assurer que le fragment est correctement formé.</span><span class="sxs-lookup"><span data-stu-id="a4992-155">This adds more information to the fragment by indicating the exact selected text, without the opening tags and end tags that have been added to ensure the fragment is well-formed HTML.</span></span>

<span data-ttu-id="a4992-156">La sélection est facultative, car des informations suffisantes sont incluses dans le fragment pour le collage de base.</span><span class="sxs-lookup"><span data-stu-id="a4992-156">The selection is optional, as sufficient information is included in the fragment for basic pasting.</span></span> <span data-ttu-id="a4992-157">Si la sélection n’est pas stockée, StartSelection et EndSelection ne sont pas stockés dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="a4992-157">If the selection is not stored, both StartSelection and EndSelection are not stored in the header.</span></span>

<span data-ttu-id="a4992-158">Le contexte est un document HTML valide et complet.</span><span class="sxs-lookup"><span data-stu-id="a4992-158">The context is a valid, complete HTML document.</span></span> <span data-ttu-id="a4992-159">Cet article contient le fragment et toutes les balises précédentes adjacentes (balises de début et de fin ; ces balises précédentes représentent tous les nœuds parents du fragment, jusqu’au nœud HTML).</span><span class="sxs-lookup"><span data-stu-id="a4992-159">This article contains the fragment and all preceding surrounding tags (start and end tags; these preceding surrounding tags represent all the parent nodes of the fragment, until the HTML node).</span></span> <span data-ttu-id="a4992-160">L’article contient également l’en-tête complet et permet aux éléments de BASE et de titre, par exemple, d’être inclus afin que ces informations supplémentaires puissent être obtenues.</span><span class="sxs-lookup"><span data-stu-id="a4992-160">The article also contains the complete HEAD, and allows the BASE and TITLE elements, for example, to be included so this additional information can be obtained.</span></span> <span data-ttu-id="a4992-161">Une application copiant un fragment de code HTML dans le presse-papiers peut choisir de créer un élément de BASE à inclure dans le contexte si ce type d’élément n’est pas déjà présent afin que les URL partielles dans le fragment puissent être résolues.</span><span class="sxs-lookup"><span data-stu-id="a4992-161">An application copying a fragment of HTML to the clipboard can choose to create a BASE element to include in the context if such an element is not already present so that partial URLs in the fragment can be resolved.</span></span>

<span data-ttu-id="a4992-162">Le contexte est facultatif, car des informations suffisantes sont incluses dans le fragment pour que le collage de base d’un fragment HTML soit effectué.</span><span class="sxs-lookup"><span data-stu-id="a4992-162">The context is optional, as sufficient information is included in the fragment for basic pasting of an HTML fragment to take place.</span></span> <span data-ttu-id="a4992-163">Si le contexte n’est pas stocké, le fragment est stocké uniquement et StartHTML = endhtml =-1.</span><span class="sxs-lookup"><span data-stu-id="a4992-163">If the context is not stored, the fragment only is stored and the StartHTML=EndHTML=-1.</span></span>

## <a name="scenarios"></a><span data-ttu-id="a4992-164">Scénarios</span><span class="sxs-lookup"><span data-stu-id="a4992-164">Scenarios</span></span>

<span data-ttu-id="a4992-165">Les scénarios suivants décrivent comment l’éditeur HTML IE4/MSHTML gère les opérations couper-coller HTML. d’autres applications peuvent ou non suivre ces scénarios.</span><span class="sxs-lookup"><span data-stu-id="a4992-165">The following scenarios describe how the IE4/MSHTML HTML editor handles HTML cut and paste; other applications may or may not follow these scenarios.</span></span> <span data-ttu-id="a4992-166">Le format du presse-papiers décrit ici est destiné à permettre la flexibilité de la façon dont une application choisit de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="a4992-166">The clipboard format described here is intended to allow flexibility for how an application chooses to function.</span></span> <span data-ttu-id="a4992-167">(Ces scénarios affichent uniquement du code HTML correct, autrement dit, aucune balise qui se chevauche.)</span><span class="sxs-lookup"><span data-stu-id="a4992-167">(These scenarios show only good HTML, that is, no overlapping tags.)</span></span>

1.  <span data-ttu-id="a4992-168">Fragment de code HTML simple.</span><span class="sxs-lookup"><span data-stu-id="a4992-168">Simple Fragment of HTML.</span></span>
    -   -   <span data-ttu-id="a4992-169">Texte HTML :</span><span class="sxs-lookup"><span data-stu-id="a4992-169">HTML text:</span></span>

            <span data-ttu-id="a4992-170"><BODY>Ceci est normal. Ceci est <B>le gras </B> <I> <B>italique </B>il s’agit</I> de l’italique</BODY></span><span class="sxs-lookup"><span data-stu-id="a4992-170"><BODY>This is normal <B>This is bold </B><I><B>This is bold italic </B>This is italic </I></BODY></span></span>

        -   <span data-ttu-id="a4992-171">Apparaît comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4992-171">Appears as:</span></span>

            <span data-ttu-id="a4992-172">Ceci est normal. Ceci est **le gras**    \* **italique** il   s’agit de l’italique \*</span><span class="sxs-lookup"><span data-stu-id="a4992-172">This is normal **This is bold**  \***This is bold italic**  This is italic\*</span></span>

        -   <span data-ttu-id="a4992-173">Le texte entre le \* \* est sélectionné et copié dans le presse-papiers :</span><span class="sxs-lookup"><span data-stu-id="a4992-173">The text between the \*\* is selected and copied to the clipboard:</span></span>

            <span data-ttu-id="a4992-174">Ceci **est normal.** ceci est le gras \* \*     \* **italique**   ce \* \* \* *est italique*</span><span class="sxs-lookup"><span data-stu-id="a4992-174">This is normal **This is** \*\* **bold**   \***This is bold italic**  This\*\*\* *is italic*</span></span>

        -   <span data-ttu-id="a4992-175">C’est ce qui se trouve dans le presse-papiers (Notez qu’il s’agit de l’interprétation de IE4/MSHTML) :</span><span class="sxs-lookup"><span data-stu-id="a4992-175">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <span data-ttu-id="a4992-176">Version : 0,9</span><span class="sxs-lookup"><span data-stu-id="a4992-176">Version:0.9</span></span>

            <span data-ttu-id="a4992-177">StartHTML : 71</span><span class="sxs-lookup"><span data-stu-id="a4992-177">StartHTML:71</span></span>

            <span data-ttu-id="a4992-178">DHTML : 160</span><span class="sxs-lookup"><span data-stu-id="a4992-178">EndHTML:160</span></span>

            <span data-ttu-id="a4992-179">StartFragment : 130</span><span class="sxs-lookup"><span data-stu-id="a4992-179">StartFragment:130</span></span>

            <span data-ttu-id="a4992-180">EndFragment : 150</span><span class="sxs-lookup"><span data-stu-id="a4992-180">EndFragment:150</span></span>

            <span data-ttu-id="a4992-181">**StartSelection : 130**</span><span class="sxs-lookup"><span data-stu-id="a4992-181">**StartSelection:130**</span></span>

            <span data-ttu-id="a4992-182">**EndSelection : 150**</span><span class="sxs-lookup"><span data-stu-id="a4992-182">**EndSelection:150**</span></span>

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            <span data-ttu-id="a4992-183">**<B>gras</B>en <I><B>italique</B></I>**</span><span class="sxs-lookup"><span data-stu-id="a4992-183">**<B>bold</B><I><B>This is bold italic</B>This</I>**</span></span>

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   <span data-ttu-id="a4992-184">Dans ce scénario, seule la balise BODY et la balise HTML apparaissent dans le contexte, car elle précède le fragment sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a4992-184">In this scenario only the BODY tag and the HTML tag appear in the context as it precedes the selected fragment.</span></span> <span data-ttu-id="a4992-185">Notez que les balises de début et de fin sont incluses dans le contexte.</span><span class="sxs-lookup"><span data-stu-id="a4992-185">Note that start tags and end tags are included in the context.</span></span> <span data-ttu-id="a4992-186">La sélection, délimitée par StartSelection et EndSelection, s’affiche en gras.</span><span class="sxs-lookup"><span data-stu-id="a4992-186">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

2.  <span data-ttu-id="a4992-187">Fragment d’une table en HTML.</span><span class="sxs-lookup"><span data-stu-id="a4992-187">Fragment of a table in HTML.</span></span>
    -   -   <span data-ttu-id="a4992-188">Texte HTML :</span><span class="sxs-lookup"><span data-stu-id="a4992-188">HTML text:</span></span>

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="a4992-189">Head1</span><span class="sxs-lookup"><span data-stu-id="a4992-189">Head1</span></span></TH><TD><span data-ttu-id="a4992-190">Item 1</span><span class="sxs-lookup"><span data-stu-id="a4992-190">Item 1</span></span></TD><TD><span data-ttu-id="a4992-191">Élément 2</span><span class="sxs-lookup"><span data-stu-id="a4992-191">Item 2</span></span></TD><TD><span data-ttu-id="a4992-192">Élément 3</span><span class="sxs-lookup"><span data-stu-id="a4992-192">Item 3</span></span></TD><TD><span data-ttu-id="a4992-193">Élément 4</span><span class="sxs-lookup"><span data-stu-id="a4992-193">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="a4992-194">Élément 5</span><span class="sxs-lookup"><span data-stu-id="a4992-194">Item 5</span></span></TD><TD><span data-ttu-id="a4992-195">Élément 6</span><span class="sxs-lookup"><span data-stu-id="a4992-195">Item 6</span></span></TD><TD><span data-ttu-id="a4992-196">Élément 7</span><span class="sxs-lookup"><span data-stu-id="a4992-196">Item 7</span></span></TD><TD><span data-ttu-id="a4992-197">Élément 8</span><span class="sxs-lookup"><span data-stu-id="a4992-197">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="a4992-198">Head2</span><span class="sxs-lookup"><span data-stu-id="a4992-198">Head2</span></span></TH><TD><span data-ttu-id="a4992-199">Élément 9</span><span class="sxs-lookup"><span data-stu-id="a4992-199">Item 9</span></span></TD><TD><span data-ttu-id="a4992-200">Élément 10</span><span class="sxs-lookup"><span data-stu-id="a4992-200">Item 10</span></span></TD><TD><span data-ttu-id="a4992-201">Élément 11</span><span class="sxs-lookup"><span data-stu-id="a4992-201">Item 11</span></span></TD><TD><span data-ttu-id="a4992-202">Élément 12</span><span class="sxs-lookup"><span data-stu-id="a4992-202">Item 12</span></span></TD></TR></TABLE></BODY>

        -   <span data-ttu-id="a4992-203">S’affiche sous la forme : ></span><span class="sxs-lookup"><span data-stu-id="a4992-203">Appears as: ></span></span><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="a4992-204">Head1</span><span class="sxs-lookup"><span data-stu-id="a4992-204">Head1</span></span></TH><TD><span data-ttu-id="a4992-205">Item 1</span><span class="sxs-lookup"><span data-stu-id="a4992-205">Item 1</span></span></TD><TD><span data-ttu-id="a4992-206">Élément 2</span><span class="sxs-lookup"><span data-stu-id="a4992-206">Item 2</span></span></TD><TD><span data-ttu-id="a4992-207">Élément 3</span><span class="sxs-lookup"><span data-stu-id="a4992-207">Item 3</span></span></TD><TD><span data-ttu-id="a4992-208">Élément 4</span><span class="sxs-lookup"><span data-stu-id="a4992-208">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="a4992-209">Élément 5</span><span class="sxs-lookup"><span data-stu-id="a4992-209">Item 5</span></span></TD><TD><span data-ttu-id="a4992-210">Élément 6</span><span class="sxs-lookup"><span data-stu-id="a4992-210">Item 6</span></span></TD><TD><span data-ttu-id="a4992-211">Élément 7</span><span class="sxs-lookup"><span data-stu-id="a4992-211">Item 7</span></span></TD><TD><span data-ttu-id="a4992-212">Élément 8</span><span class="sxs-lookup"><span data-stu-id="a4992-212">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="a4992-213">Head2</span><span class="sxs-lookup"><span data-stu-id="a4992-213">Head2</span></span></TH><TD><span data-ttu-id="a4992-214">Élément 9</span><span class="sxs-lookup"><span data-stu-id="a4992-214">Item 9</span></span></TD><TD><span data-ttu-id="a4992-215">Élément 10</span><span class="sxs-lookup"><span data-stu-id="a4992-215">Item 10</span></span></TD><TD><span data-ttu-id="a4992-216">Élément 11</span><span class="sxs-lookup"><span data-stu-id="a4992-216">Item 11</span></span></TD><TD><span data-ttu-id="a4992-217">Élément 12</span><span class="sxs-lookup"><span data-stu-id="a4992-217">Item 12</span></span></TD></TR></TABLE><span data-ttu-id="a4992-218">< ! \[ CDATA\[\]\]></span><span class="sxs-lookup"><span data-stu-id="a4992-218"><!\[CDATA\[\]\]></span></span>
        -   <span data-ttu-id="a4992-219">Les éléments élément 6, Item7, élément 10 et élément 11 de la table sont sélectionnés en tant que bloc et copiés dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a4992-219">The Item 6, Item7, Item 10, and Item 11 elements of the table are selected as a block and copied to the clipboard.</span></span>
        -   <span data-ttu-id="a4992-220">C’est ce qui se trouve dans le presse-papiers (Notez qu’il s’agit de l’interprétation de IE4/MSHTML) :</span><span class="sxs-lookup"><span data-stu-id="a4992-220">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            <span data-ttu-id="a4992-221">**<TR><TD>Élément 6 élément </TD> <TD> 7 élément 10 article </TD> </TR> <TR> <TD> </TD> <TD> 11</TD></TR>**</span><span class="sxs-lookup"><span data-stu-id="a4992-221">**<TR><TD>Item 6</TD><TD>Item 7</TD></TR><TR><TD>Item 10</TD><TD>Item 11</TD></TR>**</span></span>

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  <span data-ttu-id="a4992-222">Collage d’un fragment d’une liste triée dans du texte brut.</span><span class="sxs-lookup"><span data-stu-id="a4992-222">Pasting a fragment of an ordered list into plain text.</span></span>
    -   -   <span data-ttu-id="a4992-223">Texte HTML :</span><span class="sxs-lookup"><span data-stu-id="a4992-223">HTML text:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="a4992-224">Item 1</span><span class="sxs-lookup"><span data-stu-id="a4992-224">Item 1</span></span><LI><span data-ttu-id="a4992-225">Élément 2</span><span class="sxs-lookup"><span data-stu-id="a4992-225">Item 2</span></span><LI><span data-ttu-id="a4992-226">Élément 3</span><span class="sxs-lookup"><span data-stu-id="a4992-226">Item 3</span></span><LI><span data-ttu-id="a4992-227">Élément 4</span><span class="sxs-lookup"><span data-stu-id="a4992-227">Item 4</span></span><LI><span data-ttu-id="a4992-228">Élément 5</span><span class="sxs-lookup"><span data-stu-id="a4992-228">Item 5</span></span><LI><span data-ttu-id="a4992-229">Élément 6</span><span class="sxs-lookup"><span data-stu-id="a4992-229">Item 6</span></span></OL></BODY>

        -   <span data-ttu-id="a4992-230">Apparaît comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4992-230">Appears as:</span></span>
            1.  <span data-ttu-id="a4992-231">Item 1</span><span class="sxs-lookup"><span data-stu-id="a4992-231">Item 1</span></span>
            2.  <span data-ttu-id="a4992-232">Élément 2</span><span class="sxs-lookup"><span data-stu-id="a4992-232">Item 2</span></span>
            3.  <span data-ttu-id="a4992-233">Élément 3</span><span class="sxs-lookup"><span data-stu-id="a4992-233">Item 3</span></span>
            4.  <span data-ttu-id="a4992-234">Élément 4</span><span class="sxs-lookup"><span data-stu-id="a4992-234">Item 4</span></span>
            5.  <span data-ttu-id="a4992-235">Élément 5</span><span class="sxs-lookup"><span data-stu-id="a4992-235">Item 5</span></span>
            6.  <span data-ttu-id="a4992-236">Élément 6</span><span class="sxs-lookup"><span data-stu-id="a4992-236">Item 6</span></span>
        -   <span data-ttu-id="a4992-237">L’utilisateur sélectionne et copie les éléments 3 à 5 dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a4992-237">The user selects and copies items 3 through 5 to the clipboard.</span></span> <span data-ttu-id="a4992-238">Le code HTML suivant se trouve dans le presse-papiers :</span><span class="sxs-lookup"><span data-stu-id="a4992-238">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="a4992-239"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="a4992-239"><DOCTYPE...><HTML><BODY></span></span><OL TYPE = a>

            <!-- StartFragment-->

            <span data-ttu-id="a4992-240">**<LI>Élément 3 élément <LI> 4 élément <LI> 5**</span><span class="sxs-lookup"><span data-stu-id="a4992-240">**<LI>Item 3<LI>Item 4<LI>Item 5**</span></span>

            <!-- EndFragment-->

            </OL></BODY></HTML>

            <span data-ttu-id="a4992-241">La sélection, délimitée par StartSelection et EndSelection, est affichée en gras.</span><span class="sxs-lookup"><span data-stu-id="a4992-241">The selection, as delimited by StartSelection and EndSelection, is show in bold.</span></span>

        -   <span data-ttu-id="a4992-242">Si ce fragment est collé dans un document vide, le code HTML suivant sera créé :</span><span class="sxs-lookup"><span data-stu-id="a4992-242">If this fragment is now pasted into an empty document, the following HTML will be created:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="a4992-243">Élément 3</span><span class="sxs-lookup"><span data-stu-id="a4992-243">Item 3</span></span><LI><span data-ttu-id="a4992-244">Élément 4</span><span class="sxs-lookup"><span data-stu-id="a4992-244">Item 4</span></span><LI><span data-ttu-id="a4992-245">Élément 5</span><span class="sxs-lookup"><span data-stu-id="a4992-245">Item 5</span></span></OL></BODY>

        -   <span data-ttu-id="a4992-246">Apparaître comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4992-246">Appearing as:</span></span>
            1.  <span data-ttu-id="a4992-247">Élément 3</span><span class="sxs-lookup"><span data-stu-id="a4992-247">Item 3</span></span>
            2.  <span data-ttu-id="a4992-248">Élément 4</span><span class="sxs-lookup"><span data-stu-id="a4992-248">Item 4</span></span>
            3.  <span data-ttu-id="a4992-249">Élément 5</span><span class="sxs-lookup"><span data-stu-id="a4992-249">Item 5</span></span>

4.  <span data-ttu-id="a4992-250">Collage d’une zone partiellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a4992-250">Pasting a partially selected region.</span></span>
    -   -   <span data-ttu-id="a4992-251">Texte HTML :</span><span class="sxs-lookup"><span data-stu-id="a4992-251">HTML text:</span></span>

            <P> <span data-ttu-id="a4992-252">IE4/MSHTML est un éditeur WYSIWYG qui prend en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a4992-252">IE4/MSHTML is a WYSIWYG Editor that supports :</span></span><UL><LI><span data-ttu-id="a4992-253">Couper</span><span class="sxs-lookup"><span data-stu-id="a4992-253">Cut</span></span><LI><span data-ttu-id="a4992-254">Copier</span><span class="sxs-lookup"><span data-stu-id="a4992-254">Copy</span></span><LI><span data-ttu-id="a4992-255">Coller</span><span class="sxs-lookup"><span data-stu-id="a4992-255">Paste</span></span></UL><P><span data-ttu-id="a4992-256">C’est un excellent outil !</span><span class="sxs-lookup"><span data-stu-id="a4992-256">This is a Great Tool !</span></span>

        -   <span data-ttu-id="a4992-257">Apparaît comme suit : IE4/MSHTML est un éditeur WYSIWYG qui prend en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a4992-257">Appears as:IE4/MSHTML is a WYSIWYG Editor that supports :</span></span>
            -   -   <span data-ttu-id="a4992-258">Couper</span><span class="sxs-lookup"><span data-stu-id="a4992-258">Cut</span></span>
                -   <span data-ttu-id="a4992-259">Copier</span><span class="sxs-lookup"><span data-stu-id="a4992-259">Copy</span></span>
                -   <span data-ttu-id="a4992-260">Coller</span><span class="sxs-lookup"><span data-stu-id="a4992-260">Paste</span></span>

        -   <span data-ttu-id="a4992-261">L’utilisateur sélectionne « WYSIWYG » jusqu’à « COP ». Le code HTML suivant se trouve dans le presse-papiers :</span><span class="sxs-lookup"><span data-stu-id="a4992-261">The user selects from "WYSIWYG" until "Cop".The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="a4992-262"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="a4992-262"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <P>

            <span data-ttu-id="a4992-263">**Éditeur WYSIWYG, qui prend en charge**</span><span class="sxs-lookup"><span data-stu-id="a4992-263">**WYSIWYG Editor, which supports**</span></span>

            <span data-ttu-id="a4992-264">**<UL><LI>Couper <LI> COP**</span><span class="sxs-lookup"><span data-stu-id="a4992-264">**<UL><LI>Cut<LI>Cop**</span></span>

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   <span data-ttu-id="a4992-265">L’utilisateur sélectionne « opier » jusqu’à « belle ».</span><span class="sxs-lookup"><span data-stu-id="a4992-265">The user selects from "opy" until "Great".</span></span>

            <span data-ttu-id="a4992-266">Le code HTML suivant se trouve dans le presse-papiers :</span><span class="sxs-lookup"><span data-stu-id="a4992-266">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="a4992-267"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="a4992-267"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <UL><LI>

            <span data-ttu-id="a4992-268">**copier <LI> coller </UL> <P> c’est un excellent**</span><span class="sxs-lookup"><span data-stu-id="a4992-268">**opy<LI>Paste</UL><P> This is a Great**</span></span>

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            <span data-ttu-id="a4992-269">La sélection, délimitée par StartSelection et EndSelection, s’affiche en gras.</span><span class="sxs-lookup"><span data-stu-id="a4992-269">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

 

 




