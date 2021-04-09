---
title: Intégration des informations de l’album
description: Intégration des informations de l’album
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player Online stores, album info Integration
- magasins en ligne, intégration des informations sur les albums
- types 2 magasins en ligne, intégration des informations sur les albums
- Windows Media Player Online stores, intégration des informations relatives aux albums
- magasins en ligne, intégration des informations relatives aux albums
- tapez 2 magasins en ligne, en intégrant les informations de l’album
- Lecteur Windows Media, intégration des informations relatives aux albums
- Windows Media Player, intégration des informations sur les albums
- intégration des informations de l’album
- intégration des informations relatives aux albums
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029129"
---
# <a name="album-info-integration"></a><span data-ttu-id="146aa-113">Intégration des informations de l’album</span><span class="sxs-lookup"><span data-stu-id="146aa-113">Album Info Integration</span></span>

<span data-ttu-id="146aa-114">Le lecteur Windows Media permet aux utilisateurs de demander des informations détaillées sur le CD ou le DVD à partir duquel le contenu multimédia numérique provient en cliquant sur un bouton, par exemple **plus d’informations**.</span><span class="sxs-lookup"><span data-stu-id="146aa-114">Windows Media Player enables users to request detailed information about the CD or DVD from which digital media content originated by clicking a button, such as **More Info**.</span></span> <span data-ttu-id="146aa-115">Lorsque l’utilisateur clique sur le bouton, le lecteur Windows Media 10 ou une version ultérieure appelle sur le magasin musical actuel pour afficher les détails de l’album.</span><span class="sxs-lookup"><span data-stu-id="146aa-115">When the user clicks the button, Windows Media Player 10 or later calls on the current music store to display the album details.</span></span> <span data-ttu-id="146aa-116">Dans ce cas, le lecteur ouvre le volet informations sur l’album et affiche la page Web spécifiée par l’attribut **URL** de l’élément **AlbumInfo** du document serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="146aa-116">When this happens, the Player opens the album information pane and displays the webpage specified by the **URL** attribute of the **AlbumInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="146aa-117">Le lecteur Windows Media ajoute une chaîne de requête à l’URL pour fournir des informations au magasin en ligne sur le contenu demandé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="146aa-117">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user requested.</span></span> <span data-ttu-id="146aa-118">La chaîne de requête comprend des attributs tels que **titre**, **album** et **artiste**, que le magasin en ligne peut utiliser pour déterminer l’album approprié à afficher.</span><span class="sxs-lookup"><span data-stu-id="146aa-118">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to display.</span></span> <span data-ttu-id="146aa-119">La documentation de référence de l’élément **AlbumInfo** fournit la liste complète des attributs de chaîne de requête et leurs descriptions.</span><span class="sxs-lookup"><span data-stu-id="146aa-119">The reference documentation for the **AlbumInfo** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-album-info"></a><span data-ttu-id="146aa-120">Instructions pour les informations relatives aux albums</span><span class="sxs-lookup"><span data-stu-id="146aa-120">Guidelines for Album Info</span></span>

<span data-ttu-id="146aa-121">Lorsque vous créez votre page Web d’informations sur l’album, suivez les instructions ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="146aa-121">When creating your album information webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="146aa-122">La page doit clairement identifier la Banque en ligne qui fournit les informations.</span><span class="sxs-lookup"><span data-stu-id="146aa-122">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="146aa-123">Pour ce faire, vous pouvez afficher de manière visible votre logo, par exemple.</span><span class="sxs-lookup"><span data-stu-id="146aa-123">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="146aa-124">La page doit inclure un lien vers la déclaration de confidentialité de votre société.</span><span class="sxs-lookup"><span data-stu-id="146aa-124">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="146aa-125">Évitez autant que possible la navigation entre les pages dans la fonctionnalité d’informations sur les albums.</span><span class="sxs-lookup"><span data-stu-id="146aa-125">Avoid page navigation within the album information feature whenever possible.</span></span> <span data-ttu-id="146aa-126">Vous devez accéder à votre magasin en ligne pour la plupart des activités.</span><span class="sxs-lookup"><span data-stu-id="146aa-126">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="146aa-127">Nous vous recommandons de fournir des informations précieuses sans que l’utilisateur soit obligé d’installer des programmes ou de se connecter à votre boutique en ligne.</span><span class="sxs-lookup"><span data-stu-id="146aa-127">We recommend that you provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="146aa-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="146aa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="146aa-129">**À propos des magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="146aa-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="146aa-130">**Élément AlbumInfo**</span><span class="sxs-lookup"><span data-stu-id="146aa-130">**AlbumInfo Element**</span></span>](albuminfo-element.md)
</dt> </dl>

 

 




