---
title: Référence pour les magasins en ligne de type 1
description: Référence pour les magasins en ligne de type 1
ms.assetid: e6f45a50-029e-4347-9b25-10e9e32a56eb
keywords:
- Windows Media Player Online stores, référence
- magasins en ligne, référence
- tapez 1 magasins en ligne, référence
- référence pour les magasins en ligne de type 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475f7dee43f2f6152c3b3ebd0e6090a1efb33a72
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381688"
---
# <a name="reference-for-type-1-online-stores"></a><span data-ttu-id="e3e80-107">Référence pour les magasins en ligne de type 1</span><span class="sxs-lookup"><span data-stu-id="e3e80-107">Reference for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="e3e80-108">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="e3e80-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e3e80-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e3e80-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e3e80-110">Le lecteur Windows Media 11 fournit un compilateur de catalogue, un objet et plusieurs interfaces qui prennent en charge les magasins de type 1 en ligne.</span><span class="sxs-lookup"><span data-stu-id="e3e80-110">Windows Media Player 11 provides a catalog compiler, an object, and several interfaces that support type 1 online stores.</span></span> <span data-ttu-id="e3e80-111">Les sections suivantes documentent ces informations en détail.</span><span class="sxs-lookup"><span data-stu-id="e3e80-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="e3e80-112">Section</span><span class="sxs-lookup"><span data-stu-id="e3e80-112">Section</span></span>                                                                                    | <span data-ttu-id="e3e80-113">Description</span><span class="sxs-lookup"><span data-stu-id="e3e80-113">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3e80-114">Compilateur de catalogue pour les magasins en ligne de type 1</span><span class="sxs-lookup"><span data-stu-id="e3e80-114">Catalog Compiler for Type 1 Online Stores</span></span>](catalog-compiler-for-type-1-online-stores.md) | <span data-ttu-id="e3e80-115">Fournit des documents de référence pour le compilateur qu’un magasin en ligne utilise pour compiler son catalogue musical.</span><span class="sxs-lookup"><span data-stu-id="e3e80-115">Provides reference material for the compiler that an online store uses to compile its music catalog.</span></span>                                                                                                                               |
| [<span data-ttu-id="e3e80-116">Interface IWMPContentContainer</span><span class="sxs-lookup"><span data-stu-id="e3e80-116">IWMPContentContainer Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)                                 | <span data-ttu-id="e3e80-117">Fournit des pages de référence pour les méthodes que le plug-in du magasin en ligne appelle pour inspecter un conteneur de contenu.</span><span class="sxs-lookup"><span data-stu-id="e3e80-117">Provides reference pages for methods that the online store's plug-in calls to inspect a content container.</span></span> <span data-ttu-id="e3e80-118">Un conteneur de contenu représente un ensemble d’éléments multimédias à télécharger ou à acheter.</span><span class="sxs-lookup"><span data-stu-id="e3e80-118">A content container represents a set of media items to be downloaded or purchased.</span></span> <span data-ttu-id="e3e80-119">Implémenté par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e3e80-119">Implemented by Windows Media Player.</span></span> |
| [<span data-ttu-id="e3e80-120">Interface IWMPContentContainerList</span><span class="sxs-lookup"><span data-stu-id="e3e80-120">IWMPContentContainerList Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)                         | <span data-ttu-id="e3e80-121">Fournit des pages de référence pour les méthodes que le plug-in du magasin en ligne appelle pour inspecter une liste de conteneurs de contenu.</span><span class="sxs-lookup"><span data-stu-id="e3e80-121">Provides reference pages for methods that the online store's plug-in calls to inspect a list of content containers.</span></span> <span data-ttu-id="e3e80-122">Implémenté par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e3e80-122">Implemented by Windows Media Player.</span></span>                                                                           |
| [<span data-ttu-id="e3e80-123">Interface IWMPContentPartner</span><span class="sxs-lookup"><span data-stu-id="e3e80-123">IWMPContentPartner Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)                                     | <span data-ttu-id="e3e80-124">Fournit des pages de référence pour les méthodes appelées par le lecteur Windows Media pour obtenir des informations à partir du magasin en ligne et pour informer le magasin en ligne des actions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e3e80-124">Provides reference pages for methods that Windows Media Player calls to get information from the online store and to notify the online store about the user's actions.</span></span> <span data-ttu-id="e3e80-125">Implémenté par le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e3e80-125">Implemented by the online store's plug-in.</span></span>                  |
| [<span data-ttu-id="e3e80-126">Interface IWMPContentPartnerCallback</span><span class="sxs-lookup"><span data-stu-id="e3e80-126">IWMPContentPartnerCallback Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)                     | <span data-ttu-id="e3e80-127">Fournit des pages de référence pour les méthodes que le plug-in du magasin en ligne appelle pour notifier le lecteur Windows Media de la fin des opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="e3e80-127">Provides reference pages for methods that the online store's plug-in calls to notify Windows Media Player about the completion of asynchronous operations.</span></span> <span data-ttu-id="e3e80-128">Implémenté par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e3e80-128">Implemented by Windows Media Player.</span></span>                                    |
| [<span data-ttu-id="e3e80-129">Objet externe pour les magasins de type 1 en ligne</span><span class="sxs-lookup"><span data-stu-id="e3e80-129">External Object for Type 1 Online Stores</span></span>](external-object-for-type-1-online-stores.md)   | <span data-ttu-id="e3e80-130">Fournit des pages de référence pour les propriétés, les méthodes et les événements utilisés par le script dans les pages Web fournies par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e3e80-130">Provides reference pages for properties, methods, and events used by script in webpages provided by the online store.</span></span>                                                                                                              |
| [<span data-ttu-id="e3e80-131">Énumérations pour les magasins de type 1 en ligne</span><span class="sxs-lookup"><span data-stu-id="e3e80-131">Enumerations for Type 1 Online Stores</span></span>](enumerations-for-type-1-online-stores.md)         | <span data-ttu-id="e3e80-132">Fournit des pages de référence pour les énumérations utilisées dans la communication entre le lecteur Windows Media et le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e3e80-132">Provides reference pages for the enumerations used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                               |
| [<span data-ttu-id="e3e80-133">Structures pour les magasins de type 1 en ligne</span><span class="sxs-lookup"><span data-stu-id="e3e80-133">Structures for Type 1 Online Stores</span></span>](structures-for-type-1-online-stores.md)             | <span data-ttu-id="e3e80-134">Fournit des pages de référence pour les structures utilisées dans la communication entre le lecteur Windows Media et le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e3e80-134">Provides reference pages for the structures used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="e3e80-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3e80-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3e80-136">**Tapez 1 magasins en ligne**</span><span class="sxs-lookup"><span data-stu-id="e3e80-136">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




