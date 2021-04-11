---
title: Personnalisation de la distribution des médias
description: Personnalisation de la distribution des médias
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Sélections de métafichiers Windows Media, personnalisation de la distribution de médias
- sélections, personnalisation de la distribution des médias
- sélections de métafichiers, personnalisation de la distribution de médias
- Sélections de métafichiers Windows Media, personnalisation de la remise de médias
- sélections, personnalisation de la distribution des médias
- sélections de métafichiers, personnalisation de la remise de médias
- personnalisation de la livraison des médias
- personnalisation de la distribution des médias
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190843"
---
# <a name="personalizing-media-delivery"></a><span data-ttu-id="0411b-111">Personnalisation de la distribution des médias</span><span class="sxs-lookup"><span data-stu-id="0411b-111">Personalizing Media Delivery</span></span>

<span data-ttu-id="0411b-112">Contrairement à la communication unidirectionnelle qui diffuse du contenu identique à un public de masse, les technologies Windows Media vous fournissent les outils nécessaires à l’utilisation de données démographiques pour individualiser les diffusions.</span><span class="sxs-lookup"><span data-stu-id="0411b-112">Unlike one-way communication that broadcasts identical content to a mass audience, Windows Media Technologies provides you with the tools to use demographics to individualize broadcasts.</span></span> <span data-ttu-id="0411b-113">Avec Internet, une communication bidirectionnelle à grande échelle est facilement disponible.</span><span class="sxs-lookup"><span data-stu-id="0411b-113">With the Internet, two-way communication on a large scale is readily available.</span></span> <span data-ttu-id="0411b-114">Cet échange d’informations dynamique permet aux fournisseurs de contenu de connaître leur public et de répondre aux présentations personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0411b-114">This dynamic interchange of information enables content providers to know their audience and respond with customized presentations.</span></span>

<span data-ttu-id="0411b-115">L’exemple suivant, qui utilise une société fictive, illustre la manière dont la distribution de contenu de diffusion en continu peut être personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0411b-115">The following example, using a fictional company, illustrates how delivery of streaming content can be personalized.</span></span> <span data-ttu-id="0411b-116">Cette discussion part du principe que vous êtes familiarisé avec les pages de Active Server (fichiers ASP ou. asp) et à la définition des variables.</span><span class="sxs-lookup"><span data-stu-id="0411b-116">This discussion assumes that you are familiar with Active Server Pages (ASP, or .asp files) and defining variables.</span></span>

<span data-ttu-id="0411b-117">News Network est une organisation d’actualités de diffusion fictive qui a développé ses opérations pour inclure un site Web.</span><span class="sxs-lookup"><span data-stu-id="0411b-117">News Network is a fictional broadcast news organization that has expanded its operations to include a website.</span></span> <span data-ttu-id="0411b-118">La principale fonctionnalité du site est une section dans laquelle les utilisateurs peuvent créer leurs propres newscasts personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0411b-118">The main feature of the site is a section where users can create their own personalized newscasts.</span></span> <span data-ttu-id="0411b-119">Au lieu d’afficher un Newscast traditionnel destiné à un public de masse, un utilisateur voit un programme complet qui contient uniquement des sujets d’intérêt personnel.</span><span class="sxs-lookup"><span data-stu-id="0411b-119">Instead of viewing a traditional newscast that is aimed at a mass audience, a user views a complete news program that contains only topics of personal interest.</span></span> <span data-ttu-id="0411b-120">La séquence suivante décrit une expérience utilisateur typique.</span><span class="sxs-lookup"><span data-stu-id="0411b-120">The following sequence describes a typical user experience.</span></span>

1.  <span data-ttu-id="0411b-121">Un nouvel utilisateur accède au site et clique sur **créer votre Newscast personnel**.</span><span class="sxs-lookup"><span data-stu-id="0411b-121">A new user goes to the site, and clicks **Create Your Personal Newscast**.</span></span>
2.  <span data-ttu-id="0411b-122">Un formulaire de préférences s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="0411b-122">A preference form opens.</span></span> <span data-ttu-id="0411b-123">Sur ce formulaire, l’utilisateur répond à des questions concernant les préférences personnelles, telles que les articles d’actualité préférés, les articles les plus préférés, les hobbies et la méthode habituelle de réception d’actualités quotidiennes.</span><span class="sxs-lookup"><span data-stu-id="0411b-123">On this form, the user answers questions regarding personal preferences, such as favorite news stories, least favorite news stories, hobbies, and usual method of receiving daily news.</span></span>
3.  <span data-ttu-id="0411b-124">L’utilisateur envoie ces informations, et quelques secondes plus tard, affichent un Newscast personnel complet de 15 minutes, contenant le contenu du programme, les transitions et les commerciaux.</span><span class="sxs-lookup"><span data-stu-id="0411b-124">The user sends this information, and a few seconds later views a complete, 15-minute, personal newscast containing program content, transitions, and commercials.</span></span> <span data-ttu-id="0411b-125">La sélection de chaque élément multimédia, y compris les commerciaux, est basée sur le profil utilisateur et est effectuée automatiquement avec les composants des technologies Windows Media et les outils Internet prêts à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="0411b-125">Selection of each media element, including commercials, is based on the user profile, and is accomplished automatically with Windows Media Technologies components and off-the-shelf Internet tools.</span></span>

<span data-ttu-id="0411b-126">La liste suivante décrit comment les différents outils interagissent pour créer un Newscast personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0411b-126">The following list describes how the various tools interact to create a personalized newscast.</span></span>

1.  <span data-ttu-id="0411b-127">Le formulaire de préférence que l’utilisateur remplit est une page de Active Server (ASP) (Choices. asp).</span><span class="sxs-lookup"><span data-stu-id="0411b-127">The preference form that the user fills out is an Active Server Page (ASP) (Choices.asp).</span></span> <span data-ttu-id="0411b-128">Les données obtenues à partir de la forme de préférence sont analysées par deux composants serveur.</span><span class="sxs-lookup"><span data-stu-id="0411b-128">Data obtained from the preference form is analyzed by two server components.</span></span> <span data-ttu-id="0411b-129">Un composant utilise les informations pour interroger une base de données Microsoft SQL Server de nouvelles histoires.</span><span class="sxs-lookup"><span data-stu-id="0411b-129">One component uses the information to query a Microsoft SQL Server database of news stories.</span></span> <span data-ttu-id="0411b-130">L’autre composant est un serveur AD qui utilise un ensemble complexe de règles basées sur les exigences contractuelles et démographiques pour planifier des publicités appropriées à l’utilisateur à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="0411b-130">The other component is an ad server that uses a complex set of rules based on contractual requirements and demographics to schedule ads appropriate to the user at that time.</span></span>
2.  <span data-ttu-id="0411b-131">Les deux bases de données retournent différentes parties d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="0411b-131">The two databases return different portions of a playlist.</span></span> <span data-ttu-id="0411b-132">La base de données News Story retourne un ensemble d’entrées d’histoires appropriées, et le serveur Active Directory renvoie un ensemble d’entrées commerciales appropriées.</span><span class="sxs-lookup"><span data-stu-id="0411b-132">The news story database returns a set of appropriate story Entries, and the ad server returns a set of appropriate commercial Entries.</span></span>
3.  <span data-ttu-id="0411b-133">Une deuxième page ASP (PlayShow. asp) reçoit les entrées de la base de données d’actualités et d’AD Server, et les combine avec les entrées standard afficher ouvrir, fermer et transition.</span><span class="sxs-lookup"><span data-stu-id="0411b-133">A second ASP page (PlayShow.asp) receives the Entries from the news story database and ad server, and combines those with standard show open, close, and transition Entries.</span></span> <span data-ttu-id="0411b-134">Toutes les entrées sont ensuite présentées en fonction du modèle fourni par PlayShow. asp, et la page ASP renvoie une sélection à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0411b-134">All Entries are then laid out according to the template provided by PlayShow.asp, and the ASP page returns a playlist to the user.</span></span>
4.  <span data-ttu-id="0411b-135">Le contrôle du lecteur Windows Media incorporé sur l’ordinateur de l’utilisateur lit la sélection du début à la fin, et l’utilisateur voit un Newscast personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0411b-135">The embedded Windows Media Player control on the user's computer plays the playlist from beginning to end, and the user views a personalized newscast.</span></span>

<span data-ttu-id="0411b-136">L’exemple suivant est une partie d’un fichier de sélection qu’un utilisateur peut recevoir.</span><span class="sxs-lookup"><span data-stu-id="0411b-136">The following example is a portion of a playlist file that a user might receive.</span></span> <span data-ttu-id="0411b-137">Des bannières Active Directory, des liens MOREINFO et des RÉSUMÉs ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="0411b-137">Ad banners, MOREINFO links, and ABSTRACTS have been added to it.</span></span>


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   <span data-ttu-id="0411b-138">Les exemples de sociétés, organisations, produits, personnes et événements utilisés dans les exemples sont fictifs.</span><span class="sxs-lookup"><span data-stu-id="0411b-138">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="0411b-139">Toute ressemblance avec des noms ou des événements réels est purement fortuite et involontaire.</span><span class="sxs-lookup"><span data-stu-id="0411b-139">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0411b-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0411b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0411b-141">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="0411b-141">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0411b-142">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="0411b-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0411b-143">**Utilisation des sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="0411b-143">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0411b-144">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0411b-144">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0411b-145">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0411b-145">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




