---
title: Utilisation de pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media
description: Utilisation de pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Sélections de métafichiers Windows Media, création
- sélections de métafichiers, création
- sélections, création
- Sélections de métafichiers Windows Media, création dynamique
- sélections de métafichiers, création dynamique
- sélections, création dynamique
- Sélections de métafichiers Windows Media, pages ASP
- sélections de métafichiers, pages ASP
- sélections, pages ASP
- création de sélections de métafichiers Windows Media
- création dynamique de sélections de métafichiers Windows Media
- pages ASP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507182"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a><span data-ttu-id="e92ba-115">Utilisation de pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="e92ba-115">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>

<span data-ttu-id="e92ba-116">Vous pouvez utiliser les pages de Active Server (fichiers ASP ou. asp) pour générer dynamiquement des sélections en fonction des informations fournies par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e92ba-116">You can use Active Server Pages (ASP, or .asp files) to dynamically generate playlists based on information provided by users.</span></span> <span data-ttu-id="e92ba-117">Une page ASP est une page Web dynamique utilisée conjointement avec Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="e92ba-117">An ASP page is a dynamic webpage used in conjunction with Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="e92ba-118">ASP est un environnement dans lequel vous pouvez combiner du code HTML, des scripts et des composants serveur ActiveX réutilisables pour créer des solutions métier dynamiques et puissantes basées sur le Web.</span><span class="sxs-lookup"><span data-stu-id="e92ba-118">ASP is an environment in which you can combine HTML, scripts, and reusable ActiveX server components to create dynamic and powerful Web-based business solutions.</span></span> <span data-ttu-id="e92ba-119">Les pages ASP activent les scripts côté serveur pour IIS avec la prise en charge native pour Microsoft Visual Basic Scripting Edition (VBScript) et Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="e92ba-119">ASP pages enable server-side scripting for IIS with native support for both Microsoft Visual Basic Scripting Edition (VBScript) and Microsoft JScript.</span></span> <span data-ttu-id="e92ba-120">Cette discussion part du principe que vous êtes familiarisé avec ASP et en définissant des variables.</span><span class="sxs-lookup"><span data-stu-id="e92ba-120">This discussion assumes that you are familiar with ASP and defining variables.</span></span>

<span data-ttu-id="e92ba-121">Toutes les informations d’en-tête doivent être contenues sur la première ligne de la chaîne de page ASP retournée au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e92ba-121">All header information must be contained on the first line of the ASP page string returned to Windows Media Player.</span></span>

<span data-ttu-id="e92ba-122">Lorsque vous utilisez des pages ASP pour générer des sélections, vous devez spécifier des valeurs pour les propriétés **ContentType** et **Expires** de l’objet de **réponse** dans la page ASP en raison de problèmes de latence avec le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e92ba-122">When you use ASP pages to generate playlists, you must specify values for the **Response** object's **ContentType** and **expires** properties in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="e92ba-123">La valeur **Response. ContentType** doit être une extension de nom de fichier valide pour les fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e92ba-123">The **Response.ContentType** value must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="e92ba-124">Les valeurs acceptables sont WMA, Wax, WMV, wvx, ASF et asx.</span><span class="sxs-lookup"><span data-stu-id="e92ba-124">Acceptable values include wma, wax, wmv, wvx, asf, and asx.</span></span>

<span data-ttu-id="e92ba-125">La propriété **Response. Expires** spécifie la durée, en secondes, pendant laquelle le lecteur Windows Media met en cache le fichier de sélection.</span><span class="sxs-lookup"><span data-stu-id="e92ba-125">The **Response.expires** property specifies the length of time, in seconds, that Windows Media Player caches the playlist file.</span></span> <span data-ttu-id="e92ba-126">Si vous spécifiez la valeur zéro, le lecteur Windows Media demande une nouvelle sélection à partir du serveur chaque fois que l’utilisateur actualise la page.</span><span class="sxs-lookup"><span data-stu-id="e92ba-126">Specifying a value of zero results in Windows Media Player requesting a new playlist from the server each time the user refreshes the page.</span></span>

<span data-ttu-id="e92ba-127">Pour plus d’informations sur l’utilisation de l’objet de **réponse** dans Active Server pages, consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="e92ba-127">See the Platform SDK for details about using the **Response** object in Active Server Pages.</span></span>

<span data-ttu-id="e92ba-128">Le code suivant est un exemple de page ASP utilisée pour générer une sélection de métafichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e92ba-128">The following code is an example of an ASP page used to generate a Windows Media metafile playlist.</span></span>


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="e92ba-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e92ba-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e92ba-130">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="e92ba-130">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




