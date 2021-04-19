---
title: Acheter l’intégration pour les magasins de type 2 en ligne
description: Acheter l’intégration pour les magasins de type 2 en ligne
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player Online stores, intégration des achats
- magasins en ligne, intégration des achats
- type 2 magasins en ligne, intégration d’achat
- Windows Media Player Online stores, intégration des achats
- magasins en ligne, intégration des achats
- type 2 magasins en ligne, intégration des achats
- Windows Media Player, intégration des achats
- Windows Media Player, intégration des achats
- intégration des achats
- intégration des achats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511029"
---
# <a name="purchase-integration-for-type-2-online-stores"></a><span data-ttu-id="dfb33-113">Acheter l’intégration pour les magasins de type 2 en ligne</span><span class="sxs-lookup"><span data-stu-id="dfb33-113">Purchase Integration for Type 2 Online Stores</span></span>

<span data-ttu-id="dfb33-114">Lorsque le lecteur Windows Media lit du contenu multimédia numérique ou que l’utilisateur choisit l’option **Rechercher les informations** de l’album, le lecteur offre à l’utilisateur un lien pour acheter le CD ou DVD dont provient le contenu si un tel lien est disponible.</span><span class="sxs-lookup"><span data-stu-id="dfb33-114">When Windows Media Player plays digital media content or the user chooses **Find Album Info**, the Player offers the user a link to buy the CD or DVD from which the content originated if such a link is available.</span></span> <span data-ttu-id="dfb33-115">Lorsque l’utilisateur clique sur le lien, le lecteur Windows Media 10 ou une version ultérieure appelle sur le magasin musical actuel pour gérer la demande d’achat.</span><span class="sxs-lookup"><span data-stu-id="dfb33-115">When the user clicks the link, Windows Media Player 10 or later calls on the current music store to handle the purchase request.</span></span> <span data-ttu-id="dfb33-116">Dans ce cas, le lecteur accède au volet des tâches du premier service (dans le lecteur Windows Media 10) ou à l’onglet des magasins en ligne (dans le lecteur Windows Media 11) et affiche la page Web spécifiée par l’attribut **MediaPlayerURL** de l’élément **BuyCD** du document serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="dfb33-116">When this happens, the Player navigates to the first service task pane (in Windows Media Player 10) or the Online Stores tab (in Windows Media Player 11) and displays the webpage specified by the **MediaPlayerURL** attribute of the **BuyCD** element of the ServiceInfo document.</span></span> <span data-ttu-id="dfb33-117">(Les attributs **MediaCenterURL** et **BrowserURL** sont utilisés de la même manière pour gérer les appels de Windows xp Media Center Edition 2004 et Windows XP Service Pack 2).</span><span class="sxs-lookup"><span data-stu-id="dfb33-117">(The **MediaCenterURL** and **BrowserURL** attributes are used in a similar manner to handle calls from Windows XP Media Center Edition 2004 and Windows XP Service Pack 2).</span></span>

<span data-ttu-id="dfb33-118">Le lecteur Windows Media ajoute une chaîne de requête à l’URL pour fournir des informations au magasin en ligne sur le contenu que l’utilisateur a choisi d’acheter.</span><span class="sxs-lookup"><span data-stu-id="dfb33-118">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user chose to purchase.</span></span> <span data-ttu-id="dfb33-119">La chaîne de requête comprend des attributs tels que **titre**, **album** et **artiste**, que le magasin en ligne peut utiliser pour déterminer l’album à vendre.</span><span class="sxs-lookup"><span data-stu-id="dfb33-119">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to sell.</span></span> <span data-ttu-id="dfb33-120">La documentation de référence de l’élément **BuyCD** fournit la liste complète des attributs de chaîne de requête et leurs descriptions.</span><span class="sxs-lookup"><span data-stu-id="dfb33-120">The reference documentation for the **BuyCD** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-the-buycd-page"></a><span data-ttu-id="dfb33-121">Instructions pour la page BuyCD</span><span class="sxs-lookup"><span data-stu-id="dfb33-121">Guidelines for the BuyCD Page</span></span>

<span data-ttu-id="dfb33-122">Lorsque vous créez votre page Web BuyCD, suivez les instructions ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="dfb33-122">When creating your BuyCD webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="dfb33-123">La page doit clairement identifier la Banque en ligne qui fournit les informations.</span><span class="sxs-lookup"><span data-stu-id="dfb33-123">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="dfb33-124">Pour ce faire, vous pouvez afficher de manière visible votre logo, par exemple.</span><span class="sxs-lookup"><span data-stu-id="dfb33-124">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="dfb33-125">La page doit inclure un lien vers la déclaration de confidentialité de votre société.</span><span class="sxs-lookup"><span data-stu-id="dfb33-125">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="dfb33-126">Il est préférable de fournir des informations d’achat initiales sans que l’utilisateur soit obligé d’installer des programmes ou de se connecter à votre boutique en ligne.</span><span class="sxs-lookup"><span data-stu-id="dfb33-126">It is best to provide initial purchasing information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfb33-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfb33-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfb33-128">**À propos des magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="dfb33-128">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="dfb33-129">**Élément BuyCD**</span><span class="sxs-lookup"><span data-stu-id="dfb33-129">**BuyCD Element**</span></span>](buycd-element.md)
</dt> </dl>

 

 




