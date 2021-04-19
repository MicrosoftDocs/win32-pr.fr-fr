---
title: Conteneurs de contenu
description: Conteneurs de contenu
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Magasins en ligne du lecteur Windows Media, conteneurs de contenu
- magasins en ligne, conteneurs de contenu
- types 1 magasins en ligne, conteneurs de contenu
- Windows Media Player Online stores, interface IWMPContentContainer
- magasins en ligne, interface IWMPContentContainer
- types 1 magasins en ligne, interface IWMPContentContainer
- Windows Media Player, conteneurs de contenu
- Lecteur Windows Media, interface IWMPContentContainer
- conteneurs de contenu
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "106542845"
---
# <a name="content-containers"></a><span data-ttu-id="2e201-113">Conteneurs de contenu</span><span class="sxs-lookup"><span data-stu-id="2e201-113">Content Containers</span></span>

<span data-ttu-id="2e201-114">Le lecteur Windows Media utilise des conteneurs de contenu pour représenter le contenu multimédia numérique dans un téléchargement d’abonnement ou une transaction d’achat.</span><span class="sxs-lookup"><span data-stu-id="2e201-114">Windows Media Player uses content containers to represent digital media content in a subscription download or purchase transaction.</span></span> <span data-ttu-id="2e201-115">Un conteneur de contenu est représenté par l’interface **IWMPContentContainer** .</span><span class="sxs-lookup"><span data-stu-id="2e201-115">A content container is represented by the **IWMPContentContainer** interface.</span></span> <span data-ttu-id="2e201-116">Un conteneur de contenu peut contenir une liste de contenu associé, tel qu’un album, ou un ensemble d’éléments de contenu non liés, ou des *suivis*.</span><span class="sxs-lookup"><span data-stu-id="2e201-116">A content container might contain a list of related content, such as an album, or a set of unrelated content items, or *tracks*.</span></span> <span data-ttu-id="2e201-117">Vous pouvez utiliser l’interface **IWMPContentContainer** pour énumérer les pistes du conteneur de contenu et récupérer le prix de chaque piste. Vous pouvez également récupérer des informations sur le conteneur de contenu lui-même, telles que l’ID de conteneur, le type de contenu dans le conteneur et le prix total des pistes dans le conteneur (qui peut être différent de la somme des prix des différentes pistes, comme dans le cas d’un achat d’album).</span><span class="sxs-lookup"><span data-stu-id="2e201-117">You can use the **IWMPContentContainer** interface to enumerate the tracks of the content container and retrieve the price of each track. You can also retrieve information about the content container itself, such as the container ID, the type of content in the container, and the total price for the tracks in the container (which might differ from the sum of the prices of the individual tracks, as in the case of an album purchase).</span></span>

<span data-ttu-id="2e201-118">Pour fournir un mécanisme d’empaquetage de plusieurs conteneurs de contenu dans un seul objet, le lecteur Windows Media prend en charge l’interface **IWMPContentContainerList** .</span><span class="sxs-lookup"><span data-stu-id="2e201-118">To provide a mechanism for packaging multiple content containers into a single object, Windows Media Player supports the **IWMPContentContainerList** interface.</span></span> <span data-ttu-id="2e201-119">**IWMPContentContainerList** fournit des méthodes pour énumérer et récupérer les conteneurs de contenu de la liste.</span><span class="sxs-lookup"><span data-stu-id="2e201-119">**IWMPContentContainerList** provides methods to enumerate and retrieve the content containers in the list.</span></span> <span data-ttu-id="2e201-120">Pour déterminer si la liste de conteneurs de contenu représente un achat ou un téléchargement d’abonnement, appelez [IWMPContentContainerList :: GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) pour récupérer une valeur [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) .</span><span class="sxs-lookup"><span data-stu-id="2e201-120">To discover whether the content container list represents a purchase or a subscription download, call [IWMPContentContainerList::GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) to retrieve a [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e201-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2e201-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e201-122">**À propos des magasins en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="2e201-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="2e201-123">**Interface IWMPContentContainer**</span><span class="sxs-lookup"><span data-stu-id="2e201-123">**IWMPContentContainer Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[<span data-ttu-id="2e201-124">**Interface IWMPContentContainerList**</span><span class="sxs-lookup"><span data-stu-id="2e201-124">**IWMPContentContainerList Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




