---
title: Paramètres de ligne de commande d’installation pour les magasins en ligne
description: Paramètres de ligne de commande d’installation pour les magasins en ligne
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player Online stores, paramètres de ligne de commande du programme d’installation
- magasins en ligne, paramètres de ligne de commande du programme d’installation
- tapez 1 magasins en ligne, paramètres de ligne de commande du programme d’installation
- tapez 2 magasins en ligne, paramètres de ligne de commande du programme d’installation
- paramètres de ligne de commande du programme d’installation
- Windows Media Player Online stores, paramètres de ligne de commande
- magasins en ligne, paramètres de ligne de commande
- types 1 magasins en ligne, paramètres de ligne de commande
- types 2 magasins en ligne, paramètres de ligne de commande
- paramètres de ligne de commande
- Magasins en ligne du lecteur Windows Media, paramètres
- magasins en ligne, paramètres
- types 1 magasins en ligne, paramètres
- type 2 magasins en ligne, paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029143"
---
# <a name="setup-command-line-parameters-for-online-stores"></a><span data-ttu-id="4e581-117">Paramètres de ligne de commande d’installation pour les magasins en ligne</span><span class="sxs-lookup"><span data-stu-id="4e581-117">Setup Command-line Parameters for Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="4e581-118">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="4e581-118">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4e581-119">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e581-119">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4e581-120">Lors de l’installation du lecteur Windows Media 10 ou du lecteur Windows Media 11 sur Windows XP, vous pouvez ajouter des paramètres de ligne de commande pour spécifier le premier magasin en ligne que l’utilisateur voit.</span><span class="sxs-lookup"><span data-stu-id="4e581-120">When installing Windows Media Player 10 or Windows Media Player 11 on Windows XP, you can append command-line parameters to specify the first online store that the user sees.</span></span>

<span data-ttu-id="4e581-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e581-121">Syntax</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



<span data-ttu-id="4e581-122">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e581-122">Parameters</span></span>

<span data-ttu-id="4e581-123">DefaultService (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="4e581-123">DefaultService (required)</span></span>

<span data-ttu-id="4e581-124">Nom de la clé du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="4e581-124">The key name for the online store.</span></span> <span data-ttu-id="4e581-125">Cette valeur doit correspondre au nom de clé dans l’attribut de **clé** de l’élément **ServiceInfo** du document serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="4e581-125">This value must match the key name in the **Key** attribute of the **ServiceInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="4e581-126">ServiceInfo (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="4e581-126">ServiceInfo (required)</span></span>

<span data-ttu-id="4e581-127">Le chemin d’accès complet à un document ServiceInfo installé sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e581-127">The fully qualified path to a ServiceInfo document installed on the user's computer.</span></span>

<span data-ttu-id="4e581-128">ServiceExtra (facultatif)</span><span class="sxs-lookup"><span data-stu-id="4e581-128">ServiceExtra (optional)</span></span>

<span data-ttu-id="4e581-129">Chaîne de requête que le lecteur Windows Media 10 ajoutera à l’URL du document ServiceInfo lorsqu’il récupère le document en ligne.</span><span class="sxs-lookup"><span data-stu-id="4e581-129">A query string that Windows Media Player 10 will append to the URL for the ServiceInfo document when it retrieves the document online.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e581-130">Notes</span><span class="sxs-lookup"><span data-stu-id="4e581-130">Remarks</span></span>

<span data-ttu-id="4e581-131">Pour plus d’informations sur la redistribution du logiciel Windows Media Player avec votre application, consultez [redistribution du logiciel Windows Media Player](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="4e581-131">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="4e581-132">Lorsque l’ordinateur de l’utilisateur n’est pas connecté à Internet, les informations contenues dans le document ServiceInfo local sont utilisées pour configurer le lecteur Windows Media pour le service actif initial.</span><span class="sxs-lookup"><span data-stu-id="4e581-132">When the user's computer is not connected to the Internet, the information contained in the local ServiceInfo document is used to configure Windows Media Player for the initial active service.</span></span>

<span data-ttu-id="4e581-133">Les paramètres de ligne de commande respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="4e581-133">Command-line parameters are case sensitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e581-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e581-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e581-135">**Co-personnalisation des magasins en ligne**</span><span class="sxs-lookup"><span data-stu-id="4e581-135">**Co-Branding Online Stores**</span></span>](co-branding-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4e581-136">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="4e581-136">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4e581-137">**Élément d’installation**</span><span class="sxs-lookup"><span data-stu-id="4e581-137">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="4e581-138">**Définition de la boutique en ligne initiale**</span><span class="sxs-lookup"><span data-stu-id="4e581-138">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




