---
title: Utilisation de liens relatifs dans les sous-fichiers
description: Utilisation de liens relatifs dans les sous-fichiers
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Sélections de métafichiers Windows Media, liens relatifs
- sélections, liens relatifs
- sélections de métafichiers, liens relatifs
- sous-fichiers, liens relatifs
- Fichiers Windows Media, liens relatifs
- liens relatifs
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839726"
---
# <a name="using-relative-links-in-metafiles"></a><span data-ttu-id="b514e-109">Utilisation de liens relatifs dans les sous-fichiers</span><span class="sxs-lookup"><span data-stu-id="b514e-109">Using Relative Links in Metafiles</span></span>

<span data-ttu-id="b514e-110">Les liens relatifs sont une fonctionnalité entièrement prise en charge des fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b514e-110">Relative links are a fully supported feature of Windows Media metafiles.</span></span> <span data-ttu-id="b514e-111">Vous pouvez utiliser des liens relatifs dans les sous-fichiers de la même façon que vous les utilisez dans des documents HTML.</span><span class="sxs-lookup"><span data-stu-id="b514e-111">You can use relative links in metafiles much like you use them in HTML documents.</span></span> <span data-ttu-id="b514e-112">L’utilisation de liens relatifs vous permet de créer des métafichiers portables, ce qui signifie que vous pouvez copier ou déplacer l’intégralité d’une structure de répertoires vers un autre serveur sans mettre à jour les chemins d’accès aux fichiers graphiques utilisés comme bannières ou les attributs **href** des éléments **moreinfo** (s’ils font référence à des fichiers sur le même serveur Web que le métafichier stocké).</span><span class="sxs-lookup"><span data-stu-id="b514e-112">The use of relative links enables you to create metafiles that are portable, meaning you can copy or move an entire directory structure to another server without updating the paths to graphic files used as banners or the **HREF** attributes of **MOREINFO** elements (if they reference files on the same web server as the stored metafile).</span></span> <span data-ttu-id="b514e-113">Les liens relatifs fonctionnent, dans toutes les applications qui les prennent en charge, car les parties de l’URL non incluses dans l’attribut **href** d’un élément sont incluses dans l’URL envoyée par l’application au serveur lorsque cette URL est demandée.</span><span class="sxs-lookup"><span data-stu-id="b514e-113">Relative links work, in any application that supports them, because the parts of the URL not included in the **HREF** attribute of an element are included in the URL sent by the application to the server when that URL is requested.</span></span> <span data-ttu-id="b514e-114">Cela signifie que le protocole (par exemple, https://), le nom du serveur et le répertoire virtuel dans lequel se trouve le fichier contenant le lien relatif sont tous inclus dans l’URL qui est envoyée au serveur.</span><span class="sxs-lookup"><span data-stu-id="b514e-114">This means that the protocol (such as https://), the server name, and the virtual directory in which the file containing the relative link is located are all included in the URL that is sent to the server.</span></span> <span data-ttu-id="b514e-115">Si le fichier multimédia, ou l’URL que vous liez à l’aide d’un lien relatif ne réside pas sur le même serveur que le métafichier, le lien relatif n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b514e-115">If the media file, or URL you link to using a relative link does not reside on the same server as the metafile, the relative link is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="b514e-116">Ces informations sur les liens relatifs sont correctes uniquement lors de l’utilisation d’un lien vers les fichiers de données ouverts dans le lecteur Windows Media autonome.</span><span class="sxs-lookup"><span data-stu-id="b514e-116">This information on relative links is correct only when using a link to metafiles that are opened in the stand-alone Windows Media Player.</span></span> <span data-ttu-id="b514e-117">Quand vous utilisez le contrôle du lecteur Windows Media incorporé, tous les liens sont relatifs à la page sur laquelle le contrôle est hébergé, sauf si l’élément enfant de **base** de l’élément **ASX** est utilisé pour rediriger le chemin d’accès relatif.</span><span class="sxs-lookup"><span data-stu-id="b514e-117">When you use the embedded Windows Media Player control, all links are relative to the page on which the control is hosted, unless the **BASE** child element of the **ASX** element is used to redirect the relative path.</span></span>

 

<span data-ttu-id="b514e-118">Tous les liens relatifs dans le métafichier doivent être entièrement relatifs, et non relatifs au lecteur, pour la diffusion multimédia en continu.</span><span class="sxs-lookup"><span data-stu-id="b514e-118">All relative links in the metafile must be fully relative, not drive-relative, for streaming media.</span></span> <span data-ttu-id="b514e-119">Quand une URL commence par un \\ caractère «», le lien est relatif au lecteur.</span><span class="sxs-lookup"><span data-stu-id="b514e-119">When a URL begins with a "\\" character, the link is drive-relative.</span></span> <span data-ttu-id="b514e-120">Le lecteur Windows Media tente d’ouvrir le fichier auquel il est lié sur le lecteur à partir duquel le métafichier a été ouvert, généralement un serveur Web.</span><span class="sxs-lookup"><span data-stu-id="b514e-120">Windows Media Player attempts to open the file linked to on the drive where the metafile was opened from, usually a web server.</span></span> <span data-ttu-id="b514e-121">Étant donné que les serveurs Web utilisent des répertoires virtuels, le lecteur Windows Media tente de trouver le fichier multimédia ou le flux spécifié dans un sous-répertoire d’un répertoire virtuel sur le serveur Web à partir duquel le métafichier a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="b514e-121">Because web servers use virtual directories, Windows Media Player tries to find the specified stream or media file in a subdirectory of a virtual directory on the web server where the metafile was opened from.</span></span> <span data-ttu-id="b514e-122">Un utilisateur n’a pas accès à un répertoire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b514e-122">A user would not have access to a server directory.</span></span> <span data-ttu-id="b514e-123">L’exemple de cette section illustre l’utilisation d’un lien complet.</span><span class="sxs-lookup"><span data-stu-id="b514e-123">The example in this section illustrates the use of a fully relative link.</span></span>

<span data-ttu-id="b514e-124">Vous pouvez utiliser des liens relatifs au lecteur lors de l’utilisation de métafichiers sur un seul ordinateur sur lequel tous les fichiers multimédias liés dans la sélection de métafichiers existent sur un dispositif de stockage sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b514e-124">You can use drive-relative links when using metafiles on a single computer where all media files linked to in the metafile playlist exist on a storage device in that computer.</span></span> <span data-ttu-id="b514e-125">Toutefois, vous ne pouvez pas diffuser le contenu multimédia de cette manière.</span><span class="sxs-lookup"><span data-stu-id="b514e-125">However, you cannot stream media in this manner.</span></span>

<span data-ttu-id="b514e-126">Lorsque vous utilisez un lien vers un autre métafichier pour autoriser les liens relatifs, le nom affiché comme titre par le lecteur Windows Media est le titre dans le métafichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="b514e-126">When you use a link to another metafile to allow for relative links, the name displayed as the Title by Windows Media Player is the Title in the original metafile.</span></span>

<span data-ttu-id="b514e-127">Les liens relatifs ne peuvent pas être utilisés pour les URL vers un serveur multimédia de diffusion en continu, car différents protocoles sont utilisés pour accéder au contenu multimédia en continu.</span><span class="sxs-lookup"><span data-stu-id="b514e-127">Relative links cannot be used for URLs to a streaming media server because different protocols are used for accessing streaming media content.</span></span>

<span data-ttu-id="b514e-128">Dans l’exemple de sélection suivant, le premier **ENTRYREF** contient une URL pour une autre playlist, relative. Wax.</span><span class="sxs-lookup"><span data-stu-id="b514e-128">In the following example playlist, the first **ENTRYREF** contains a URL for another playlist, relative.wax.</span></span>


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



<span data-ttu-id="b514e-129">L’exemple suivant est le fichier relative. Wax, qui contient des liens relatifs.</span><span class="sxs-lookup"><span data-stu-id="b514e-129">The following example is the file relative.wax, which contains relative links.</span></span>


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="b514e-130">L’URL qui contient la référence à la playlist, relative. Wax, peut exister dans une sélection de métafichiers partout où elle est accessible à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b514e-130">The URL containing the reference to the playlist, relative.wax, can exist in a metafile playlist anywhere that is accessible to the user.</span></span> <span data-ttu-id="b514e-131">Pour que l’URL soit traitée avec succès, il doit y avoir un serveur Web nommé « example.microsoft.com ».</span><span class="sxs-lookup"><span data-stu-id="b514e-131">For the URL to be processed successfully, there must be a web server named "example.microsoft.com".</span></span> <span data-ttu-id="b514e-132">Ce serveur Web doit avoir un répertoire virtuel défini en tant que « sous-fichiers ».</span><span class="sxs-lookup"><span data-stu-id="b514e-132">That web server must have a virtual directory defined as "metafiles".</span></span> <span data-ttu-id="b514e-133">La sélection référencée, relative. Wax, doit exister sur le serveur Web nommé « example.microsoft.com » dans le répertoire virtuel « cafiles ».</span><span class="sxs-lookup"><span data-stu-id="b514e-133">The referenced playlist, relative.wax, must exist on the web server named "example.microsoft.com" in the virtual directory "metafiles".</span></span>

<span data-ttu-id="b514e-134">Pour que les fichiers multimédias référencés dans la playlist relative. Wax soient correctement accessibles et joués, il doit y avoir un répertoire nommé « Graphics », qui est un sous-répertoire du répertoire virtuel du serveur « metadirectorys ».</span><span class="sxs-lookup"><span data-stu-id="b514e-134">For the referenced media files in the playlist relative.wax to be successfully accessed and played, there must be a directory named "Graphics" which is a subdirectory of the server's virtual directory "metafiles".</span></span> <span data-ttu-id="b514e-135">Le fichier graphique Logo1.jpg, référencé dans l’élément **Banner** , doit être le sous-répertoire nommé Graphics.</span><span class="sxs-lookup"><span data-stu-id="b514e-135">The graphics file Logo1.jpg, referenced in the **BANNER** element, must be the subdirectory named Graphics.</span></span>

<span data-ttu-id="b514e-136">De même, un document nommé Category1.htm doit résider dans un sous-répertoire nommé Category1.</span><span class="sxs-lookup"><span data-stu-id="b514e-136">Similarly a document named Category1.htm must reside in a subdirectory named Category1.</span></span> <span data-ttu-id="b514e-137">Le répertoire nommé Category1 doit exister sous la forme d’un sous-répertoire du répertoire virtuel « méta-fichiers » sur le serveur Web example.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="b514e-137">The directory named Category1 must exist as a subdirectory of the virtual directory "metafiles" on the web server example.microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b514e-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b514e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b514e-139">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="b514e-139">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="b514e-140">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="b514e-140">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="b514e-141">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b514e-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b514e-142">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b514e-142">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




