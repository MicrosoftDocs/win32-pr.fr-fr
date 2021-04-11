---
title: Création de sélections de métafichiers
description: Création de sélections de métafichiers
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Sélections de métafichiers Windows Media, création
- sélections, création
- sélections de métafichiers, création
- création de sélections de métafichiers Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197126"
---
# <a name="creating-metafile-playlists"></a><span data-ttu-id="b1e9e-107">Création de sélections de métafichiers</span><span class="sxs-lookup"><span data-stu-id="b1e9e-107">Creating Metafile Playlists</span></span>

<span data-ttu-id="b1e9e-108">Vous pouvez créer une sélection à l’aide de n’importe quel éditeur de texte, tel que le bloc-notes Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-108">You can create a playlist using any text editor, such as Microsoft Notepad.</span></span> <span data-ttu-id="b1e9e-109">Ouvrez votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-109">Open your text editor.</span></span> <span data-ttu-id="b1e9e-110">Tapez les entrées de script que vous souhaitez implémenter.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-110">Type the script entries you want to implement.</span></span> <span data-ttu-id="b1e9e-111">Une fois que vous avez fini de taper dans le bloc-notes, enregistrez le fichier avec un nom de fichier et une extension de nom de fichier appropriés.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-111">After you have finished typing into Notepad, save the file with an appropriate file name and file name extension.</span></span> <span data-ttu-id="b1e9e-112">Pour plus d’informations sur les extensions, consultez [instructions relatives](metafile-extension-guidelines.md)aux extensions de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-112">For more information about extensions, see [Metafile Extension Guidelines](metafile-extension-guidelines.md).</span></span> <span data-ttu-id="b1e9e-113">En général, le nom de fichier est le nom du fichier ou du flux Windows Media suivi d’une extension. Wax,. wvx ou. asx.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-113">Typically the file name is the name of the Windows Media file or stream followed by an extension of .wax, .wvx, or .asx.</span></span> <span data-ttu-id="b1e9e-114">Par exemple, si votre contenu multimédia est un fichier audio Windows Media qui a une extension. WMA, utilisez l’extension. Wax lors de l’attribution d’un nom à la sélection.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-114">For example, if your media content is a Windows Media audio file that has a .wma extension, use the .wax extension when naming the playlist.</span></span> <span data-ttu-id="b1e9e-115">Les sélections ne doivent inclure aucun code de mise en forme d’un traitement de texte, tel que Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-115">Playlists must not include any formatting codes from a word processor, such as Microsoft Word.</span></span> <span data-ttu-id="b1e9e-116">Pour vous assurer qu’aucun code de mise en forme n’est inclus dans la sélection, enregistrez le fichier sous forme de fichier ASCII ou texte brut.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-116">To be sure no formatting codes are included in the playlist, save the file as a plain text or ASCII file.</span></span>

> [!Note]  
> <span data-ttu-id="b1e9e-117">Les éléments et les attributs ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-117">Elements and attributes are not case sensitive.</span></span> <span data-ttu-id="b1e9e-118">Le texte utilisé dans la sélection pour définir un élément ou un attribut peut être en majuscules ou en minuscules, ou un mélange des deux.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-118">The text used in the playlist to define an element or attribute can be either uppercase or lowercase, or a mixture of both.</span></span>

 

<span data-ttu-id="b1e9e-119">Si un élément n’a pas d’éléments enfants (ceux qui modifient ou sont contenus dans un autre élément), une barre oblique (/) peut être utilisée à la fin de la balise d’ouverture, juste avant le' > ', à la place d’une balise de fermeture.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-119">If an element does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag, just before the '>', in place of a closing tag.</span></span> <span data-ttu-id="b1e9e-120">Les éléments enfants d’un élément doivent apparaître entre les balises d’ouverture et de fermeture de cet élément ; dans le cas contraire, ils ne sont pas des éléments enfants pour cet élément et sont ignorés ou provoquent une erreur dans la syntaxe de la playlist.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-120">Child elements of an element must appear between the opening and closing tag for that element; otherwise they are not child elements for that element, and are ignored or cause an error in the syntax of the playlist.</span></span>

<span data-ttu-id="b1e9e-121">Les quatre premiers caractères d’une sélection doivent être « &lt; ASX ».</span><span class="sxs-lookup"><span data-stu-id="b1e9e-121">The first four characters of a playlist must be "&lt;ASX".</span></span> <span data-ttu-id="b1e9e-122">L’élément **ASX** est utilisé dans toutes les sélections, que son extension soit. Wax,. wvx ou. asx.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-122">The **ASX** element is used in all playlists whether their extension is .wax, .wvx, or .asx.</span></span> <span data-ttu-id="b1e9e-123">Il ne doit y avoir qu’un seul élément **ASX** par playlist.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-123">There must be only one **ASX** element per playlist.</span></span> <span data-ttu-id="b1e9e-124">Cet élément identifie le fichier comme une sélection de métafichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-124">This element identifies the file as a Windows Media metafile playlist.</span></span> <span data-ttu-id="b1e9e-125">Elle ne spécifie pas le type de sélection.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-125">It does not specify the type of playlist.</span></span>

<span data-ttu-id="b1e9e-126">L’élément **ASX** a trois attributs possibles :</span><span class="sxs-lookup"><span data-stu-id="b1e9e-126">The **ASX** element has three possible attributes:</span></span>

<span data-ttu-id="b1e9e-127">**VERSION**</span><span class="sxs-lookup"><span data-stu-id="b1e9e-127">**VERSION**</span></span>

<span data-ttu-id="b1e9e-128">L’attribut **version** est obligatoire et doit suivre immédiatement après l’élément **ASX** , par exemple « <ASX version = "3,0" &gt; ».</span><span class="sxs-lookup"><span data-stu-id="b1e9e-128">The **VERSION** attribute is required and must follow immediately after the **ASX** element, for example "<ASX version = "3.0"&gt;".</span></span> <span data-ttu-id="b1e9e-129">Le numéro de version actuel est 3,0.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-129">The current version number is 3.0.</span></span> <span data-ttu-id="b1e9e-130">Le lecteur Windows Media prend en charge toutes les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-130">Windows Media Player supports all previous versions.</span></span> <span data-ttu-id="b1e9e-131">Les valeurs acceptables pour l’attribut **version** incluent à la fois 3,0 et 3 (sans virgule décimale).</span><span class="sxs-lookup"><span data-stu-id="b1e9e-131">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="b1e9e-132">**PREVIEWMODE**</span><span class="sxs-lookup"><span data-stu-id="b1e9e-132">**PREVIEWMODE**</span></span>

<span data-ttu-id="b1e9e-133">L’attribut **PREVIEWMODE** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-133">The **PREVIEWMODE** attribute is optional.</span></span> <span data-ttu-id="b1e9e-134">Il fournit un autre mécanisme pour spécifier la durée de rendu d’un clip.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-134">It provides another mechanism for specifying how long to render a clip.</span></span> <span data-ttu-id="b1e9e-135">Si la valeur de l’attribut **PREVIEWMODE** est Yes, le lecteur Windows Media affiche chaque clip pendant la durée spécifiée par l’élément **PREVIEWDURATION**.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-135">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player will render each clip for the duration specified by the element **PREVIEWDURATION**.</span></span> <span data-ttu-id="b1e9e-136">Un **PREVIEWDURATION** peut être spécifié pour chaque clip.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-136">Each clip can have a **PREVIEWDURATION** specified.</span></span>

<span data-ttu-id="b1e9e-137">**BANNERBAR**</span><span class="sxs-lookup"><span data-stu-id="b1e9e-137">**BANNERBAR**</span></span>

<span data-ttu-id="b1e9e-138">L’attribut facultatif **BANNERBAR** définit si le contrôle du lecteur Windows Media réserve de l’espace pour un graphique de bannière.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-138">The optional **BANNERBAR** attribute defines whether the Windows Media Player control reserves space for a banner graphic.</span></span> <span data-ttu-id="b1e9e-139">(Utilisez l’élément **bannière** pour spécifier le graphique à afficher.) Si la valeur de **BANNERBAR** est fixe, le lecteur Windows Media réserve de l’espace de bannière pour l’affichage et pour chaque clip, que la sélection de métafichier spécifie une bannière pour le diaporama ou le clip.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-139">(Use the **BANNER** element to specify the graphic to display.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for the show and for every clip, whether the metafile playlist specifies a banner for the show or clip.</span></span> <span data-ttu-id="b1e9e-140">Cela permet de conserver la taille de la fenêtre du lecteur Windows Media le même (sauf si la taille de la vidéo change) indépendamment de l’absence ou de la présence d’un graphique de bannière.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-140">This will keep the size of the Windows Media Player window the same (except when the video size changes) regardless of the absence or presence of a banner graphic.</span></span> <span data-ttu-id="b1e9e-141">Si aucune bannière n’est associée à l’affichage ou au clip, l’espace réservé pour celui-ci est noir.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-141">If the show or clip does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="b1e9e-142">Si la valeur de l’attribut **BANNERBAR** est auto, le lecteur Windows Media réserve de l’espace pour la bannière uniquement lorsque le diaporama ou le clip en contient un.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-142">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the show or clip includes one.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



<span data-ttu-id="b1e9e-143">Pour plus d’informations sur les trois attributs de l’élément **ASX** , consultez l’entrée de référence de l' [élément ASX](asx-element.md).</span><span class="sxs-lookup"><span data-stu-id="b1e9e-143">For more information about the three attributes of the **ASX** element, see the reference entry for the [ASX Element](asx-element.md).</span></span>

<span data-ttu-id="b1e9e-144">Un élément **ASX** contient des éléments enfants d' **entrée** qui définissent des informations sur les fichiers multimédias à accéder.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-144">An **ASX** element contains **ENTRY** child elements that define information about the media files to be accessed.</span></span> <span data-ttu-id="b1e9e-145">Chaque élément d' **entrée** doit contenir un élément **ref** qui spécifie le chemin d’accès au fichier multimédia à diffuser en continu.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-145">Each **ENTRY** element must contain a **REF** element that specifies the path to the media file to be streamed.</span></span> <span data-ttu-id="b1e9e-146">Il doit y avoir au moins une **entrée** ou un élément **ENTRYREF** dans un élément **ASX** .</span><span class="sxs-lookup"><span data-stu-id="b1e9e-146">There must be at least one **ENTRY** or **ENTRYREF** element within an **ASX** element.</span></span>

<span data-ttu-id="b1e9e-147">Les autres éléments définis dans l’étendue de l’élément **ASX** , tels que **title** et **Author**, sont associés aux métadonnées affichées par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-147">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the metadata displayed by Windows Media Player.</span></span>

<span data-ttu-id="b1e9e-148">Les sélections les plus simples sont créées en ajoutant plusieurs éléments d' **entrée** avec un seul élément **ref** à un métafichier.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-148">The simplest playlists are created by adding multiple **ENTRY** elements with a single **REF** element to a metafile.</span></span> <span data-ttu-id="b1e9e-149">Chaque élément d' **entrée** d’une sélection de métafichier est restitué dans l’ordre dans lequel il apparaît dans le fichier comme si l’utilisateur avait ouvert manuellement chaque clip.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-149">Each **ENTRY** element in a metafile playlist is rendered in the order it appears in the file as though the user had manually opened each clip.</span></span>

<span data-ttu-id="b1e9e-150">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="b1e9e-150">Example Code</span></span>


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



<span data-ttu-id="b1e9e-151">Assurez-vous que la sélection fonctionne en double-cliquant dessus dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-151">Be sure that the playlist is working by double-clicking it in Windows Explorer.</span></span> <span data-ttu-id="b1e9e-152">Le lecteur Windows Media doit ouvrir et démarrer la diffusion en continu du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-152">Windows Media Player should open and start streaming the media content.</span></span> <span data-ttu-id="b1e9e-153">Une fois que vous avez confirmé que la sélection fonctionne, enregistrez-la sur votre serveur Web avec vos pages Web, et liez-la au moyen d’un élément **href** , ou incorporez-la dans une page Web à l’aide de l’élément **objet** du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b1e9e-153">After you have confirmed that the playlist works, save it to your web server along with your webpages, and link to it by means of an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** element.</span></span>

<span data-ttu-id="b1e9e-154">Les sections suivantes contiennent des informations supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="b1e9e-154">The following sections contain more information:</span></span>

-   [<span data-ttu-id="b1e9e-155">Imbrication de refichiers</span><span class="sxs-lookup"><span data-stu-id="b1e9e-155">Nesting Metafiles</span></span>](nesting-metafiles.md)
-   [<span data-ttu-id="b1e9e-156">Utilisation de pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="b1e9e-156">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="b1e9e-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1e9e-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1e9e-158">**Élément BANNER**</span><span class="sxs-lookup"><span data-stu-id="b1e9e-158">**BANNER Element**</span></span>](banner-element.md)
</dt> <dt>

[<span data-ttu-id="b1e9e-159">**Exemples de sélections**</span><span class="sxs-lookup"><span data-stu-id="b1e9e-159">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="b1e9e-160">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b1e9e-160">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b1e9e-161">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b1e9e-161">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




