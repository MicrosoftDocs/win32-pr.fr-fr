---
title: À propos des magasins en ligne de type 1
description: À propos des magasins en ligne de type 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player Online stores, tapez 1 magasins en ligne
- magasins en ligne, type 1 magasins en ligne
- tapez 1 magasins en ligne, à propos de
- Windows Media Player, type 1 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512299"
---
# <a name="about-type-1-online-stores"></a><span data-ttu-id="a05c3-107">À propos des magasins en ligne de type 1</span><span class="sxs-lookup"><span data-stu-id="a05c3-107">About Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="a05c3-108">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="a05c3-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a05c3-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a05c3-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a05c3-110">Le lecteur Microsoft Windows Media 11 prend en charge deux types de magasins en ligne : type 1 et type 2.</span><span class="sxs-lookup"><span data-stu-id="a05c3-110">Microsoft Windows Media Player 11 supports two kinds of online stores: type 1 and type 2.</span></span> <span data-ttu-id="a05c3-111">Les magasins de type 1 sont plus profondément intégrés au lecteur Windows Media que les magasins de type 2.</span><span class="sxs-lookup"><span data-stu-id="a05c3-111">Type 1 stores are more deeply integrated into Windows Media Player than type 2 stores.</span></span> <span data-ttu-id="a05c3-112">Un magasin en ligne de type 1 fournit un catalogue musical téléchargeable afin que le lecteur Windows Media puisse mettre le contenu du magasin à la disposition de l’utilisateur comme si le contenu se trouvait dans la bibliothèque multimédia locale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a05c3-112">A type 1 online store provides a downloadable music catalog so that Windows Media Player can make the store's content available to the user as if the content were in the user's local media library.</span></span>

<span data-ttu-id="a05c3-113">Un magasin en ligne de type 1 doit fournir un plug-in qui implémente l’interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="a05c3-113">A type 1 online store must provide a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="a05c3-114">Lorsque l’utilisateur navigue dans l’interface utilisateur du lecteur Windows Media, le lecteur appelle le plug-in afin que le magasin en ligne puisse améliorer l’expérience de l’utilisateur en fournissant des pages Web qui s’affichent dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="a05c3-114">As the user navigates in the Windows Media Player user interface, the Player calls the plug-in so that the online store can enhance the user's experience by providing webpages that are displayed in the Player.</span></span>

<span data-ttu-id="a05c3-115">Les fonctionnalités des magasins en ligne de type 1 qui les distinguent des magasins de type 2 sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a05c3-115">Features of type 1 online stores that distinguish them from type 2 stores include the following:</span></span>

-   <span data-ttu-id="a05c3-116">**Facilité d’utilisation.**</span><span class="sxs-lookup"><span data-stu-id="a05c3-116">**Ease of use.**</span></span> <span data-ttu-id="a05c3-117">Les utilisateurs peuvent rechercher de la musique dans le catalogue du magasin en ligne à l’aide de la même interface utilisateur du lecteur Windows Media que celle qui est utilisée actuellement pour gérer leur bibliothèque personnelle.</span><span class="sxs-lookup"><span data-stu-id="a05c3-117">Users can browse for music from the online store catalog using the same, familiar Windows Media Player user interface that they currently use to manage their personal library.</span></span> <span data-ttu-id="a05c3-118">Les utilisateurs ne peuvent afficher qu’un seul catalogue de magasins en ligne dans la fonctionnalité parcourir à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="a05c3-118">Users can view only a single online store catalog in the Browse feature at any particular time.</span></span>
-   <span data-ttu-id="a05c3-119">**Pure.**</span><span class="sxs-lookup"><span data-stu-id="a05c3-119">**Convenience.**</span></span> <span data-ttu-id="a05c3-120">Les utilisateurs peuvent échantillonner ou acheter de la musique sans passer de la fonctionnalité parcourir à une autre partie de l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a05c3-120">Users can sample or purchase music without switching from the Browse feature to another part of the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="a05c3-121">**Fonctionnalités enrichies.**</span><span class="sxs-lookup"><span data-stu-id="a05c3-121">**Rich features.**</span></span> <span data-ttu-id="a05c3-122">Étant donné que le catalogue du magasin en ligne est stocké de manière similaire à la bibliothèque de l’utilisateur, de nombreuses fonctionnalités de la bibliothèque du lecteur Windows Media peuvent être appliquées au catalogue.</span><span class="sxs-lookup"><span data-stu-id="a05c3-122">Because the online store catalog is stored in a fashion similar to the user's library, many of the Windows Media Player library features can be applied to the catalog.</span></span> <span data-ttu-id="a05c3-123">Par exemple, les utilisateurs peuvent utiliser le mot Wheel de la fonctionnalité parcourir pour filtrer le catalogue du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="a05c3-123">For example, users can use the Browse feature's word wheel to filter the online store catalog.</span></span>

<span data-ttu-id="a05c3-124">Pour un fournisseur de magasin en ligne, les avantages de la fourniture d’un magasin de type 1 au lieu d’un magasin de type 2 sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="a05c3-124">For an online store provider, the advantages of providing a type 1 store rather than a type 2 store include the following:</span></span>

-   <span data-ttu-id="a05c3-125">Nœud personnalisé très visible dans l’arborescence de la bibliothèque du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a05c3-125">A highly visible custom node in the Windows Media Player library tree.</span></span>
-   <span data-ttu-id="a05c3-126">Système conçu pour les achats musicaux.</span><span class="sxs-lookup"><span data-stu-id="a05c3-126">A system designed for music purchases.</span></span>
-   <span data-ttu-id="a05c3-127">Connexions améliorées aux processus du lecteur.</span><span class="sxs-lookup"><span data-stu-id="a05c3-127">Improved connections to Player processes.</span></span>
-   <span data-ttu-id="a05c3-128">Gestionnaire de téléchargement plus facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a05c3-128">A better, easier-to-use download manager.</span></span>
-   <span data-ttu-id="a05c3-129">Possibilité de naviguer entre les différentes fonctionnalités du lecteur (y compris l’ouverture d’un nœud d’arborescence de bibliothèque spécifique).</span><span class="sxs-lookup"><span data-stu-id="a05c3-129">The ability to navigate between various features in the Player (including opening specific library tree nodes).</span></span>
-   <span data-ttu-id="a05c3-130">Notifications relatives à l’expiration de la licence pour le contenu de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="a05c3-130">Notifications about license expiration for subscription content.</span></span>
-   <span data-ttu-id="a05c3-131">Notifications pour l’utilisation de lecteurs musicaux portables connectés.</span><span class="sxs-lookup"><span data-stu-id="a05c3-131">Notifications for working with connected portable music players.</span></span>

<span data-ttu-id="a05c3-132">Les sections suivantes fournissent des informations générales sur les magasins de type 1 en ligne.</span><span class="sxs-lookup"><span data-stu-id="a05c3-132">The following sections provide overview information about type 1 online stores.</span></span>



| <span data-ttu-id="a05c3-133">Section</span><span class="sxs-lookup"><span data-stu-id="a05c3-133">Section</span></span>                                                                                              | <span data-ttu-id="a05c3-134">Description</span><span class="sxs-lookup"><span data-stu-id="a05c3-134">Description</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a05c3-135">Catalogue musical</span><span class="sxs-lookup"><span data-stu-id="a05c3-135">Music Catalog</span></span>](music-catalog.md)                                                                   | <span data-ttu-id="a05c3-136">Décrit le catalogue musical fourni par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="a05c3-136">Describes the music catalog provided by the online store.</span></span> <span data-ttu-id="a05c3-137">Décrit le compilateur de catalogue fourni par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a05c3-137">Describes the catalog compiler provided by Microsoft.</span></span>                                                                     |
| [<span data-ttu-id="a05c3-138">Conteneurs de contenu</span><span class="sxs-lookup"><span data-stu-id="a05c3-138">Content Containers</span></span>](content-containers.md)                                                         | <span data-ttu-id="a05c3-139">Décrit l’interface de conteneur de contenu ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), qui est utilisée pour représenter une collection d’éléments multimédias à acheter ou à télécharger.</span><span class="sxs-lookup"><span data-stu-id="a05c3-139">Describes the content container interface ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), which is used to represent a collection of media items to be purchased or downloaded.</span></span> |
| [<span data-ttu-id="a05c3-140">Intégration de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a05c3-140">Library Integration</span></span>](library-integration.md)                                                       | <span data-ttu-id="a05c3-141">Décrit comment le catalogue de musique de la boutique en ligne est intégré à la vue Bibliothèque du lecteur.</span><span class="sxs-lookup"><span data-stu-id="a05c3-141">Describes how the online store's music catalog is integrated into the Player's library view.</span></span>                                                                                        |
| [<span data-ttu-id="a05c3-142">Pages de découverte</span><span class="sxs-lookup"><span data-stu-id="a05c3-142">Discovery Pages</span></span>](discovery-pages.md)                                                               | <span data-ttu-id="a05c3-143">Décrit l’interaction entre le lecteur Windows Media et les pages Web fournies par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="a05c3-143">Describes the interaction between Windows Media Player and webpages provided by the online store.</span></span>                                                                                   |
| [<span data-ttu-id="a05c3-144">Menus contextuels</span><span class="sxs-lookup"><span data-stu-id="a05c3-144">Context Menus</span></span>](context-menus.md)                                                                   | <span data-ttu-id="a05c3-145">Décrit comment le magasin en ligne peut fournir des menus contextuels au fur et à mesure que l’utilisateur navigue dans l’interface utilisateur du joueur.</span><span class="sxs-lookup"><span data-stu-id="a05c3-145">Describes how the online store can provide context menus as the user navigates the Player's user interface.</span></span>                                                                         |
| [<span data-ttu-id="a05c3-146">Flux audio</span><span class="sxs-lookup"><span data-stu-id="a05c3-146">Audio Streams</span></span>](audio-streams.md)                                                                   | <span data-ttu-id="a05c3-147">Décrit comment le magasin en ligne fournit le lecteur Windows Media avec l’URL de diffusion en continu de contenu audio.</span><span class="sxs-lookup"><span data-stu-id="a05c3-147">Describes how the online store provides Windows Media Player with the URL for streaming audio content.</span></span>                                                                              |
| [<span data-ttu-id="a05c3-148">Document ServiceInfo pour une boutique en ligne de type 1</span><span class="sxs-lookup"><span data-stu-id="a05c3-148">ServiceInfo Document for a Type 1 Online Store</span></span>](serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="a05c3-149">Décrit le document XML ServiceInfo fourni par un magasin en ligne de type 1.</span><span class="sxs-lookup"><span data-stu-id="a05c3-149">Describes the ServiceInfo XML document provided by a type 1 online store.</span></span>                                                                                                           |
| [<span data-ttu-id="a05c3-150">Type 1 plug-in de magasin en ligne</span><span class="sxs-lookup"><span data-stu-id="a05c3-150">Type 1 Online Store Plug-in</span></span>](type-1-online-store-plug-in.md)                                       | <span data-ttu-id="a05c3-151">Décrit le plug-in qu’un magasin en ligne de type 1 doit fournir.</span><span class="sxs-lookup"><span data-stu-id="a05c3-151">Describes the plug-in that a type 1 online store must provide.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="a05c3-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a05c3-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a05c3-153">**Tapez 1 magasins en ligne**</span><span class="sxs-lookup"><span data-stu-id="a05c3-153">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




