---
title: Une sélection de base
description: Une sélection de base
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Sélections de métafichiers Windows Media, exemple de sélection de base
- sélections, exemple de sélection de base
- sélections de métafichiers, exemple de sélection de base
- Windows Media Player, exemples de sélection
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemple de sélection de base
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
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314782"
---
# <a name="a-basic-playlist"></a><span data-ttu-id="69056-125">Une sélection de base</span><span class="sxs-lookup"><span data-stu-id="69056-125">A Basic Playlist</span></span>

<span data-ttu-id="69056-126">L’exemple de sélection suivant montre un ensemble de base d’éléments de sélection.</span><span class="sxs-lookup"><span data-stu-id="69056-126">The following playlist example shows a basic set of playlist elements.</span></span> <span data-ttu-id="69056-127">Lorsque vous écrivez votre propre code, vous devez remplacer toutes les URL et tous les noms de fichiers par des noms de fichiers valides accessibles à votre lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="69056-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="69056-128">**Exemple de code**</span><span class="sxs-lookup"><span data-stu-id="69056-128">**Code Example**</span></span>


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="69056-129">Le tableau suivant fournit des détails sur l’utilisation de chaque élément dans l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="69056-129">The following table provides details on the use of each element in the example code.</span></span>



| <span data-ttu-id="69056-130">Courbes</span><span class="sxs-lookup"><span data-stu-id="69056-130">Line</span></span>                                                                                            | <span data-ttu-id="69056-131">Description</span><span class="sxs-lookup"><span data-stu-id="69056-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | <span data-ttu-id="69056-132">L’élément [ASX](asx-element.md) identifie pour le client (lecteur Windows Media) qu’il s’agit d’une sélection de métafichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="69056-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="69056-133">L’attribut **version** spécifie le numéro de version des éléments du métafichier.</span><span class="sxs-lookup"><span data-stu-id="69056-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="69056-134">\<TITLE>Démonstration de la playlist de base\</TITLE></span><span class="sxs-lookup"><span data-stu-id="69056-134">\<TITLE>Basic Playlist Demo\</TITLE></span></span>                                                  | <span data-ttu-id="69056-135">L’élément [title](title-element--metafile.md) identifie le titre de la sélection dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="69056-135">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="69056-136">Le lecteur Windows Media affiche ces métadonnées en tant que titre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="69056-136">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | <span data-ttu-id="69056-137">Commence l’élément [entry](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="69056-137">Begins the [ENTRY](entry-element.md) element.</span></span> <span data-ttu-id="69056-138">Un élément d' **entrée** permet de définir un clip particulier dans une sélection</span><span class="sxs-lookup"><span data-stu-id="69056-138">An **ENTRY** element is a way to define a particular clip in a playlist</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="69056-139">\<TITLE>Entrée dans une sélection de base\</TITLE></span><span class="sxs-lookup"><span data-stu-id="69056-139">\<TITLE>An Entry in a basic playlist\</TITLE></span></span>                                         | <span data-ttu-id="69056-140">Identifie le titre du clip de la sélection.</span><span class="sxs-lookup"><span data-stu-id="69056-140">Identifies the title of the playlist clip .</span></span> <span data-ttu-id="69056-141">Elle est différente de l’élément **title** précédent, car celle-ci est imbriquée dans un élément **entry** .</span><span class="sxs-lookup"><span data-stu-id="69056-141">It is different than the previous **TITLE** element because this one is nested within an **ENTRY** element.</span></span> <span data-ttu-id="69056-142">Le lecteur Windows Media affiche ces métadonnées en tant que titre du clip.</span><span class="sxs-lookup"><span data-stu-id="69056-142">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="69056-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span><span class="sxs-lookup"><span data-stu-id="69056-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span></span>                                              | <span data-ttu-id="69056-144">L’élément [Author](author-element.md) identifie l’auteur du clip multimédia.</span><span class="sxs-lookup"><span data-stu-id="69056-144">The [AUTHOR](author-element.md) element identifies the author of the media clip .</span></span> <span data-ttu-id="69056-145">Le lecteur Windows Media affiche ces métadonnées en tant qu' **auteur** de clip.</span><span class="sxs-lookup"><span data-stu-id="69056-145">Windows Media Player displays this metadata as the clip **AUTHOR**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | <span data-ttu-id="69056-146">Commentaire.</span><span class="sxs-lookup"><span data-stu-id="69056-146">A comment.</span></span> <span data-ttu-id="69056-147">Les [Commentaires](comments.md) sont visibles uniquement lorsque le code est affiché et sont au même format que les commentaires **XML** .</span><span class="sxs-lookup"><span data-stu-id="69056-147">[Comments](comments.md) are visible only when the code is viewed, and are in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | <span data-ttu-id="69056-148">Pointeur réel vers le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="69056-148">Actual pointer to the media file.</span></span> <span data-ttu-id="69056-149">L’élément [ref](ref-element.md) identifie la ligne comme un pointeur vers du contenu multimédia, tandis que l’attribut **href** est l’URL du fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="69056-149">The [REF](ref-element.md) element identifies the line as a pointer to media content, while the **HREF** attribute is the URL to the media file.</span></span> <span data-ttu-id="69056-150">Dans ce cas, l’URL utilise le protocole MMS, de sorte qu’elle pointe vers un serveur Windows Media. Les fichiers multimédias sur votre serveur multimédia ne sont généralement pas conservés dans le même emplacement que vos documents HTML.</span><span class="sxs-lookup"><span data-stu-id="69056-150">In this case, the URL uses the MMS protocol, so it points to a Windows Media server.Media files on your media server are not usually kept in the same location as your HTML documents.</span></span><br/> <span data-ttu-id="69056-151">Notez l’utilisation de la fermeture de l’élément, par exemple « /> », au lieu de « &lt; /Ref &gt; ».</span><span class="sxs-lookup"><span data-stu-id="69056-151">Note the use of the XML-like closing of the element , "/>", instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="69056-152">Étant donné que cet élément n’a pas d’éléments enfants, il se ferme lui-même.</span><span class="sxs-lookup"><span data-stu-id="69056-152">Because this element does not have child elements, it closes itself.</span></span><br/> |
| \</ENTRY>                                                                                  | <span data-ttu-id="69056-153">Spécifie la fin de l’élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="69056-153">Specifies the end of the **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | <span data-ttu-id="69056-154">Spécifie la fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="69056-154">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="69056-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69056-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69056-156">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="69056-156">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="69056-157">**Exemples de sélections**</span><span class="sxs-lookup"><span data-stu-id="69056-157">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="69056-158">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="69056-158">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="69056-159">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="69056-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="69056-160">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="69056-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





