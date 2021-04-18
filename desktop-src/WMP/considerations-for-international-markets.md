---
title: Considérations relatives aux marchés internationaux
description: Considérations relatives aux marchés internationaux
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player Online stores, marchés internationaux
- magasins en ligne, marchés internationaux
- types 1 magasins en ligne, marchés internationaux
- types 2 magasins en ligne, marchés internationaux
- marchés internationaux
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511838"
---
# <a name="considerations-for-international-markets"></a><span data-ttu-id="a54ab-113">Considérations relatives aux marchés internationaux</span><span class="sxs-lookup"><span data-stu-id="a54ab-113">Considerations for International Markets</span></span>

<span data-ttu-id="a54ab-114">Si votre société crée des magasins en ligne pour plusieurs marchés, vous devez fournir à Microsoft l’URL d’un document ServiceInfo pour chaque marché.</span><span class="sxs-lookup"><span data-stu-id="a54ab-114">If your company creates online stores for multiple markets, you must provide Microsoft with the URL of a ServiceInfo document for each market.</span></span> <span data-ttu-id="a54ab-115">Vous pouvez procéder de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="a54ab-115">You can do this one of the following two ways:</span></span>

-   <span data-ttu-id="a54ab-116">Créez un document ServiceInfo distinct pour chaque marché.</span><span class="sxs-lookup"><span data-stu-id="a54ab-116">Create a separate ServiceInfo document for each market.</span></span> <span data-ttu-id="a54ab-117">Dans ce cas, vous fournissez à Microsoft des URL qui pointent vers des documents ServiceInfo individuels pour chaque magasin en ligne de chaque marché.</span><span class="sxs-lookup"><span data-stu-id="a54ab-117">In this case, you provide Microsoft with URLs that point to individual ServiceInfo documents for each online store in each market.</span></span>
-   <span data-ttu-id="a54ab-118">Créez un seul document ServiceInfo pour tous les marchés.</span><span class="sxs-lookup"><span data-stu-id="a54ab-118">Create a single ServiceInfo document for all markets.</span></span> <span data-ttu-id="a54ab-119">Dans ce cas, vous fournissez à Microsoft la même URL pour chaque marché.</span><span class="sxs-lookup"><span data-stu-id="a54ab-119">When you do this, you provide Microsoft with the same URL for each market.</span></span> <span data-ttu-id="a54ab-120">Votre document ServiceInfo, créé en tant que page ASP, peut détecter dynamiquement l’emplacement de l’utilisateur en fonction des paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="a54ab-120">Your ServiceInfo document, created as an ASP page, can then dynamically detect the user's location based on query string parameters.</span></span>

<span data-ttu-id="a54ab-121">Le lecteur Windows Media ajoute une chaîne de requête à la demande d’URL ServiceInfo qui fournit des informations sur les paramètres régionaux et d’emplacement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a54ab-121">Windows Media Player appends a query string to the ServiceInfo URL request that provides information about the user's locale and location settings.</span></span> <span data-ttu-id="a54ab-122">Si votre magasin en ligne utilise ces informations pour déterminer le contenu à afficher, vous devez ajouter dynamiquement ces valeurs à vos propres URL dans votre document ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="a54ab-122">If your online store uses this information to determine which content to display, you should dynamically append these values to your own URLs in your ServiceInfo document.</span></span> <span data-ttu-id="a54ab-123">C’est la meilleure façon de s’assurer que les URL de votre page Web contiendront toujours les paramètres attendus.</span><span class="sxs-lookup"><span data-stu-id="a54ab-123">This is the best way to ensure that your webpage URLs will always contain the parameters you expect.</span></span>

<span data-ttu-id="a54ab-124">Une fois que vous avez déterminé l’emplacement et la préférence de langue de l’utilisateur, vous souhaiterez peut-être conserver ces informations pour des sessions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a54ab-124">Once you have determined the user's location and language preference, you may want to persist this information for future sessions.</span></span> <span data-ttu-id="a54ab-125">Vous pouvez le faire à l’aide de l’une des techniques que vous utiliseriez normalement dans une page Web, telle que les cookies, ou à l’aide de votre objet COM.</span><span class="sxs-lookup"><span data-stu-id="a54ab-125">You can do this using any of the techniques you would normally use in a webpage, such as cookies, or by using your COM object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a54ab-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a54ab-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a54ab-127">**Création du document ServiceInfo de manière dynamique**</span><span class="sxs-lookup"><span data-stu-id="a54ab-127">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="a54ab-128">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="a54ab-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="a54ab-129">**Élément ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="a54ab-129">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> </dl>

 

 




