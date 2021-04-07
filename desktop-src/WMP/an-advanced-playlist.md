---
title: Une sélection avancée
description: Une sélection avancée
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Sélections de métafichiers Windows Media, exemples de sélection
- sélections, exemples de sélection
- sélections de métafichiers, exemples de sélection
- Sélections de métafichiers Windows Media, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Sélections de métafichiers Windows Media, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Sélections de métafichiers Windows Media, exemple de code
- sélections, exemple de code
- sélections de métafichiers, exemple de code
- Sélections de métafichiers Windows Media, exemple de sélection avancée
- sélections, exemple de sélection avancée
- sélections de métafichiers, exemple de sélection avancée
- Windows Media Player, exemples de sélection
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemple de sélection avancée
- exemples de sélection
- exemples de sélections
- exemples de sélections
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029000"
---
# <a name="an-advanced-playlist"></a><span data-ttu-id="864d1-125">Une sélection avancée</span><span class="sxs-lookup"><span data-stu-id="864d1-125">An Advanced Playlist</span></span>

<span data-ttu-id="864d1-126">L’exemple de sélection suivant montre comment utiliser un ensemble plus complet d’éléments de sélection.</span><span class="sxs-lookup"><span data-stu-id="864d1-126">The following playlist example shows how to use a more complete set of playlist elements.</span></span> <span data-ttu-id="864d1-127">Lorsque vous écrivez votre propre code, vous devez remplacer toutes les URL et tous les noms de fichiers par des noms de fichiers valides accessibles à votre lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="864d1-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="864d1-128">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="864d1-128">Example Code</span></span>


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="864d1-129">Le tableau suivant décrit la sélection avancée précédente.</span><span class="sxs-lookup"><span data-stu-id="864d1-129">The following table describes the preceding advanced playlist.</span></span>



| <span data-ttu-id="864d1-130">Lignes</span><span class="sxs-lookup"><span data-stu-id="864d1-130">Line</span></span>                                                                                            | <span data-ttu-id="864d1-131">Description</span><span class="sxs-lookup"><span data-stu-id="864d1-131">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | <span data-ttu-id="864d1-132">L’élément [ASX](asx-element.md) identifie pour le client (lecteur Windows Media) qu’il s’agit d’une sélection de métafichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="864d1-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="864d1-133">L’attribut **version** spécifie le numéro de version des éléments du métafichier.</span><span class="sxs-lookup"><span data-stu-id="864d1-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | <span data-ttu-id="864d1-134">L’élément [title](title-element--metafile.md) identifie le titre de la sélection dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="864d1-134">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="864d1-135">Le lecteur Windows Media affiche ces métadonnées en tant que titre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="864d1-135">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | <span data-ttu-id="864d1-136">L’élément [abstract](abstract-element.md) fournit l’info-bulle pour le titre de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="864d1-136">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the show title.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | <span data-ttu-id="864d1-137">L’élément [moreinfo](moreinfo-element.md) lie le titre d’affichage à une URL.</span><span class="sxs-lookup"><span data-stu-id="864d1-137">The [MOREINFO](moreinfo-element.md) element links the show title to an URL.</span></span> <span data-ttu-id="864d1-138">La suspension du pointeur de la souris sur le titre du diaporama accède à l’info-bulle, si elle est définie.</span><span class="sxs-lookup"><span data-stu-id="864d1-138">Pausing the mouse pointer over the show title accesses the ToolTip, if defined.</span></span> <span data-ttu-id="864d1-139">Sélectionnez l’option Afficher le titre pour ouvrir l’URL désignée.</span><span class="sxs-lookup"><span data-stu-id="864d1-139">Selecting the show title will then open the designated URL.</span></span>                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | <span data-ttu-id="864d1-140">L’élément [bannière](banner-element.md) crée une bannière publicitaire dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="864d1-140">The [BANNER](banner-element.md) element creates an advertising banner in Windows Media Player.</span></span> <span data-ttu-id="864d1-141">L’attribut **href** spécifie le graphique de bannière (qui doit être de 194 pixels de largeur par 32 pixels de haut).</span><span class="sxs-lookup"><span data-stu-id="864d1-141">The **HREF** attribute specifies the banner graphic (which must be 194 pixels wide by 32 pixels tall).</span></span>                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | <span data-ttu-id="864d1-142">L’élément [abstract](abstract-element.md) fournit l’info-bulle de la **bannière**.</span><span class="sxs-lookup"><span data-stu-id="864d1-142">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the **BANNER**.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | <span data-ttu-id="864d1-143">L’élément [moreinfo](moreinfo-element.md) lie le graphique de **bannière** à une URL.</span><span class="sxs-lookup"><span data-stu-id="864d1-143">The [MOREINFO](moreinfo-element.md) element links the **BANNER** graphic to a URL.</span></span> <span data-ttu-id="864d1-144">Le maintien du pointeur de la souris sur la **bannière** accède à une info-bulle, si elle est définie.</span><span class="sxs-lookup"><span data-stu-id="864d1-144">Holding the mouse pointer over the **BANNER** accesses a ToolTip, if defined.</span></span> <span data-ttu-id="864d1-145">La sélection de la **bannière** permet d’ouvrir l’URL désignée.</span><span class="sxs-lookup"><span data-stu-id="864d1-145">Selecting the **BANNER** will open the designated URL.</span></span>                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | <span data-ttu-id="864d1-146">L’élément [param](param-element.md) définit un paramètre personnalisé.</span><span class="sxs-lookup"><span data-stu-id="864d1-146">The [PARAM](param-element.md) element defines a custom parameter.</span></span> <span data-ttu-id="864d1-147">L’attribut **Name** définit le nom du paramètre personnalisé comme « Track ».</span><span class="sxs-lookup"><span data-stu-id="864d1-147">The **name** attribute defines the name of the custom parameter as "track".</span></span> <span data-ttu-id="864d1-148">L’attribut **value** définit la valeur de « Track » sur « 1 ».</span><span class="sxs-lookup"><span data-stu-id="864d1-148">The **value** attribute defines the value of "track" to be "1".</span></span>                                                                                                                          |
| `</BANNER>`                                                                                 | <span data-ttu-id="864d1-149">Ferme l’élément de **bannière**</span><span class="sxs-lookup"><span data-stu-id="864d1-149">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | <span data-ttu-id="864d1-150">Commence le bloc d’élément d' [entrée](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="864d1-150">Begins the [ENTRY](entry-element.md) element block.</span></span> <span data-ttu-id="864d1-151">Cet élément définit un élément dans une playlist en spécifiant un lien dans l’élément **ref** .</span><span class="sxs-lookup"><span data-stu-id="864d1-151">This element defines a clip in a playlist by specifying a link in the **REF** element.</span></span> <span data-ttu-id="864d1-152">La définition de **ClientSkip** sur « no » signifie que l’utilisateur ne peut pas avancer rapidement ou passer au clip suivant</span><span class="sxs-lookup"><span data-stu-id="864d1-152">Setting **ClientSkip** to "no" means that the user cannot fast forward or jump to the next clip</span></span>                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | <span data-ttu-id="864d1-153">Crée une bannière de publicité.</span><span class="sxs-lookup"><span data-stu-id="864d1-153">Creates an advertising banner.</span></span> <span data-ttu-id="864d1-154">Le **href** est le graphique de bannière (194x32 pixels).</span><span class="sxs-lookup"><span data-stu-id="864d1-154">The **HREF** is the banner graphic (194x32 pixels).</span></span>                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | <span data-ttu-id="864d1-155">Fournit l’info-bulle de la bannière.</span><span class="sxs-lookup"><span data-stu-id="864d1-155">Provides the ToolTip for the banner.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="864d1-156">Fournit un lien vers l’URL de la bannière.</span><span class="sxs-lookup"><span data-stu-id="864d1-156">Provides a link to the URL for the banner.</span></span> <span data-ttu-id="864d1-157">La sélection de la bannière permet de se connecter à l’URL.</span><span class="sxs-lookup"><span data-stu-id="864d1-157">Selecting the banner connects to the URL.</span></span>                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | <span data-ttu-id="864d1-158">Ferme l’élément de **bannière**</span><span class="sxs-lookup"><span data-stu-id="864d1-158">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="864d1-159">Fournit un lien vers l’URL du texte du **titre** du clip.</span><span class="sxs-lookup"><span data-stu-id="864d1-159">Provides a link to the URL for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | <span data-ttu-id="864d1-160">Commentaire.</span><span class="sxs-lookup"><span data-stu-id="864d1-160">A comment.</span></span> <span data-ttu-id="864d1-161">Les [Commentaires](comments.md) ne sont visibles que lorsque le code est affiché.</span><span class="sxs-lookup"><span data-stu-id="864d1-161">[Comments](comments.md) are only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | <span data-ttu-id="864d1-162">Fournit l’info-bulle pour le texte du **titre** du clip.</span><span class="sxs-lookup"><span data-stu-id="864d1-162">Provides the ToolTip for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | <span data-ttu-id="864d1-163">Identifie le titre du clip.</span><span class="sxs-lookup"><span data-stu-id="864d1-163">Identifies the title of the clip.</span></span> <span data-ttu-id="864d1-164">Il s’agit du **titre** du clip, car il est imbriqué dans un élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="864d1-164">It is the clip **TITLE** because it is nested within an **ENTRY** element.</span></span> <span data-ttu-id="864d1-165">Le lecteur Windows Media affiche ces métadonnées en tant que titre du clip.</span><span class="sxs-lookup"><span data-stu-id="864d1-165">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | <span data-ttu-id="864d1-166">Identifie l’auteur du clip multimédia.</span><span class="sxs-lookup"><span data-stu-id="864d1-166">Identifies the author of the media clip.</span></span> <span data-ttu-id="864d1-167">Ces métadonnées s’affichent en tant qu' **auteur** du clip par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="864d1-167">This metadata is displayed as the clip **AUTHOR** by Windows Media Player.</span></span>                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | <span data-ttu-id="864d1-168">L’élément [Copyright](copyright-element.md) spécifie les droits d’auteur associés au clip multimédia.</span><span class="sxs-lookup"><span data-stu-id="864d1-168">The [COPYRIGHT](copyright-element.md) element specifies the copyrights associated with the media clip.</span></span> <span data-ttu-id="864d1-169">Le lecteur Windows Media affiche ces métadonnées sous forme de COPYRIGHT.</span><span class="sxs-lookup"><span data-stu-id="864d1-169">Windows Media Player displays this metadata as the clip COPYRIGHT.</span></span>                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="864d1-170">Commentaire, dans le même format que les commentaires **XML** .</span><span class="sxs-lookup"><span data-stu-id="864d1-170">A comment, in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | <span data-ttu-id="864d1-171">URL du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="864d1-171">URL for the media content.</span></span> <span data-ttu-id="864d1-172">L’élément [ref](ref-element.md) identifie la ligne comme un pointeur vers du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="864d1-172">The [REF](ref-element.md) element identifies the line as a pointer to media content.</span></span> <span data-ttu-id="864d1-173">L’attribut **href** est l’URL du fichier. Notez l’utilisation de la fermeture de l’élément de type XML, « /> » au lieu de « &lt; /Ref &gt; ».</span><span class="sxs-lookup"><span data-stu-id="864d1-173">The **HREF** attribute is the URL to the file.Note the use of the XML-like closing of the element , "/>" instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="864d1-174">Étant donné que cet élément n’a pas d’éléments enfants, il se ferme lui-même.</span><span class="sxs-lookup"><span data-stu-id="864d1-174">Because this element does not have child elements, it closes itself.</span></span><br/> |
| `</ENTRY>`                                                                                  | <span data-ttu-id="864d1-175">Spécifie la fin du du premier élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="864d1-175">Specifies the end of the of the first **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | <span data-ttu-id="864d1-176">Commence le deuxième élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="864d1-176">Begins the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | <span data-ttu-id="864d1-177">Identifie le titre du deuxième clip.</span><span class="sxs-lookup"><span data-stu-id="864d1-177">Identifies the title of the second clip.</span></span>                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | <span data-ttu-id="864d1-178">Identifie l’auteur du deuxième clip multimédia.</span><span class="sxs-lookup"><span data-stu-id="864d1-178">Identifies the author of the second media clip.</span></span>                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | <span data-ttu-id="864d1-179">Commentaire.</span><span class="sxs-lookup"><span data-stu-id="864d1-179">A comment.</span></span> <span data-ttu-id="864d1-180">Elle est visible uniquement lorsque le code est affiché.</span><span class="sxs-lookup"><span data-stu-id="864d1-180">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | <span data-ttu-id="864d1-181">Il s’agit du texte d’info-bulle pour le texte du **titre** du clip.</span><span class="sxs-lookup"><span data-stu-id="864d1-181">This is the ToolTip text for the **TITLE** text of the clip.</span></span>                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="864d1-182">Commentaire.</span><span class="sxs-lookup"><span data-stu-id="864d1-182">A comment.</span></span> <span data-ttu-id="864d1-183">Elle est visible uniquement lorsque le code est affiché.</span><span class="sxs-lookup"><span data-stu-id="864d1-183">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | <span data-ttu-id="864d1-184">Identifie la ligne comme pointeur vers du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="864d1-184">Identifies the line as a pointer to media content.</span></span> <span data-ttu-id="864d1-185">L’attribut **href** est l’URL du fichier.</span><span class="sxs-lookup"><span data-stu-id="864d1-185">The **HREF** attribute is the URL to the file.</span></span>                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | <span data-ttu-id="864d1-186">Spécifie la fin du deuxième élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="864d1-186">Specifies the end of the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | <span data-ttu-id="864d1-187">Spécifie la fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="864d1-187">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="864d1-188">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="864d1-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="864d1-189">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="864d1-189">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="864d1-190">**Exemples de sélections**</span><span class="sxs-lookup"><span data-stu-id="864d1-190">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="864d1-191">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="864d1-191">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="864d1-192">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="864d1-192">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="864d1-193">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="864d1-193">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





