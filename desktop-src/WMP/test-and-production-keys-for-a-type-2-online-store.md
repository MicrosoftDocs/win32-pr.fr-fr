---
title: Clés de test et de production pour un magasin de type 2 en ligne
description: Clés de test et de production pour un magasin de type 2 en ligne
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Windows Media Player Online stores, clés de test
- magasins en ligne, clés de test
- type 2 magasins en ligne, clés de test
- Windows Media Player Online stores, clés de production
- magasins en ligne, clés de production
- type 2 magasins en ligne, clés de production
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- clés de test
- clés de production
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940237"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a><span data-ttu-id="7c501-115">Clés de test et de production pour un magasin de type 2 en ligne</span><span class="sxs-lookup"><span data-stu-id="7c501-115">Test and Production Keys for a Type 2 Online Store</span></span>

<span data-ttu-id="7c501-116">Lorsque vous commencez le développement de votre boutique en ligne, Microsoft vous propose deux clés numériques : une clé de test et une clé de production.</span><span class="sxs-lookup"><span data-stu-id="7c501-116">When you begin development of your online store, Microsoft provides you with two numeric keys: a test key and a production key.</span></span> <span data-ttu-id="7c501-117">En même temps, vous devez fournir à Microsoft deux URL : une qui pointe vers votre document ServiceInfo de test et une autre qui pointe vers votre document ServiceInfo de production.</span><span class="sxs-lookup"><span data-stu-id="7c501-117">At the same time, you must provide Microsoft with two URLs: one that points to your test ServiceInfo document and one that points to your production ServiceInfo document.</span></span>

<span data-ttu-id="7c501-118">Pendant la phase de développement et de test, votre magasin en ligne est visible dans le lecteur Windows Media uniquement si votre clé de test ou votre clé de production se trouve dans le registre sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7c501-118">During the development and testing stage, your online store is visible in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="7c501-119">Si votre clé de test est dans le registre, le lecteur Windows Media récupère votre document ServiceInfo de test, qui pointe vers le plug-in, les pages Web et les images qui appartiennent à votre magasin de test.</span><span class="sxs-lookup"><span data-stu-id="7c501-119">If your test key is in the registry, Windows Media Player retrieves your test ServiceInfo document, which points to the plug-in, webpages, and images that belong to your test store.</span></span> <span data-ttu-id="7c501-120">Si votre clé de production se trouve dans le registre, le lecteur Windows Media récupère votre document ServiceInfo de production, qui pointe vers le plug-in, les pages Web et les images qui appartiennent à votre magasin de production.</span><span class="sxs-lookup"><span data-stu-id="7c501-120">If your production key is in the registry, Windows Media Player retrieves your production ServiceInfo document, which points to the plug-in, webpages, and images that belong to your production store.</span></span>

<span data-ttu-id="7c501-121">Vous pouvez utiliser vos magasins de test et de production de la manière qui vous convient.</span><span class="sxs-lookup"><span data-stu-id="7c501-121">You can use your test and production stores in any way you find useful.</span></span> <span data-ttu-id="7c501-122">Toutefois, en règle générale, la distinction est la suivante :</span><span class="sxs-lookup"><span data-stu-id="7c501-122">Typically, however, the distinction is as follows:</span></span>

-   <span data-ttu-id="7c501-123">Votre magasin de test est l’endroit où vous apportez des modifications quotidiennes à votre plug-in, vos pages Web, vos images et d’autres composants de votre service.</span><span class="sxs-lookup"><span data-stu-id="7c501-123">Your test store is the place where you make daily changes to your plug-in, webpages, images, and other components of your service.</span></span>
-   <span data-ttu-id="7c501-124">Votre magasin de production est l’endroit où vous gardez une version stable de votre service, qui comprend votre plug-in, vos pages Web, vos images et d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="7c501-124">Your production store is the place where you keep a stable release of your service, which includes your plug-in, webpages, images, and other components.</span></span>

<span data-ttu-id="7c501-125">Pour que votre magasin en ligne puisse être publié dans le lecteur Windows Media, Microsoft doit vérifier que votre service fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="7c501-125">Before your online store can be published in Windows Media Player, Microsoft must validate that your service performs correctly.</span></span> <span data-ttu-id="7c501-126">Au cours de la phase de validation, Microsoft utilise votre clé de production.</span><span class="sxs-lookup"><span data-stu-id="7c501-126">During the validation phase, Microsoft uses your production key.</span></span> <span data-ttu-id="7c501-127">Microsoft n’utilise pas votre clé de test pendant la phase de validation.</span><span class="sxs-lookup"><span data-stu-id="7c501-127">Microsoft does not use your test key during the validation phase.</span></span>

<span data-ttu-id="7c501-128">Lorsque votre magasin en ligne de production termine avec succès le processus de validation, Microsoft publie votre magasin, ce qui signifie que votre magasin de production apparaît dans le lecteur Windows Media pour tous les utilisateurs, et pas seulement ceux qui ont votre clé de production dans le registre.</span><span class="sxs-lookup"><span data-stu-id="7c501-128">When your production online store successfully completes the validation process, Microsoft publishes your store, which means that your production store appears in Windows Media Player for all users, not just the ones who have your production key in the registry.</span></span> <span data-ttu-id="7c501-129">Une fois votre magasin publié, les clés de test et de production ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7c501-129">After your store is published, the test and production keys are no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="7c501-130">Les utilisateurs peuvent être en mesure de deviner la clé de test ou de production de votre boutique en ligne et d’afficher votre boutique pendant son développement.</span><span class="sxs-lookup"><span data-stu-id="7c501-130">Users might be able to guess the test or production key for your online store and view your store while it is being developed.</span></span> <span data-ttu-id="7c501-131">Vous devez faire attention à l’exposition des fonctionnalités que vous souhaitez conserver secrètes jusqu’à la publication publique.</span><span class="sxs-lookup"><span data-stu-id="7c501-131">You should be careful about exposing features that you want to keep secret until public release.</span></span>

 

<span data-ttu-id="7c501-132">Pour plus d’informations sur l’emplacement de vos clés de production et de test dans le registre de l’utilisateur, consultez [clés et entrées de Registre pour un magasin de type 2 en ligne](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="7c501-132">For detailed information about where to put your production and test keys in the user's registry, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c501-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c501-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c501-134">**À propos des magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="7c501-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7c501-135">**Exemples de magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="7c501-135">**Type 2 Online Store Samples**</span></span>](type-2-online-store-samples.md)
</dt> </dl>

 

 




