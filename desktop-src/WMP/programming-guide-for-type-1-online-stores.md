---
title: Guide de programmation pour les magasins de type 1 en ligne
description: Guide de programmation pour les magasins de type 1 en ligne
ms.assetid: 6950cab8-4355-4699-8245-f2817c3e25fc
keywords:
- Windows Media Player Online stores, Guide de programmation
- magasins en ligne, Guide de programmation
- tapez 1 magasins en ligne, Guide de programmation
- Guide de programmation, type 1 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea04cb188a68c85173b5b1682235b6964840d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197184"
---
# <a name="programming-guide-for-type-1-online-stores"></a><span data-ttu-id="464ba-107">Guide de programmation pour les magasins de type 1 en ligne</span><span class="sxs-lookup"><span data-stu-id="464ba-107">Programming Guide for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="464ba-108">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="464ba-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="464ba-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="464ba-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="464ba-110">Cette section contient les rubriques suivantes pour vous aider à créer un magasin en ligne de type 1.</span><span class="sxs-lookup"><span data-stu-id="464ba-110">This section contains the following topics to help you create a type 1 online store.</span></span>



| <span data-ttu-id="464ba-111">Section</span><span class="sxs-lookup"><span data-stu-id="464ba-111">Section</span></span>                                                                                                              | <span data-ttu-id="464ba-112">Description</span><span class="sxs-lookup"><span data-stu-id="464ba-112">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="464ba-113">Exemple de document ServiceInfo pour une boutique en ligne de type 1</span><span class="sxs-lookup"><span data-stu-id="464ba-113">Example ServiceInfo Document for a Type 1 Online Store</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="464ba-114">Montre un exemple de document ServiceInfo que vous pouvez utiliser comme point de départ.</span><span class="sxs-lookup"><span data-stu-id="464ba-114">Shows an example ServiceInfo document that you can use as a starting point.</span></span>                                                                    |
| [<span data-ttu-id="464ba-115">Création du plug-in pour un magasin de type 1 en ligne</span><span class="sxs-lookup"><span data-stu-id="464ba-115">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)                 | <span data-ttu-id="464ba-116">Explique comment générer le plug-in requis pour un magasin de type 1 en ligne.</span><span class="sxs-lookup"><span data-stu-id="464ba-116">Explains how to build the required plug-in for a type 1 online store.</span></span>                                                                          |
| [<span data-ttu-id="464ba-117">Afficher des boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="464ba-117">Displaying Dialog Boxes</span></span>](displaying-dialog-boxes.md)                                                               | <span data-ttu-id="464ba-118">Explique comment appeler des boîtes de dialogue par le biais du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="464ba-118">Explains how to invoke dialog boxes through Windows Media Player.</span></span>                                                                              |
| [<span data-ttu-id="464ba-119">Gestion de la connexion</span><span class="sxs-lookup"><span data-stu-id="464ba-119">Managing Login</span></span>](managing-login.md)                                                                                 | <span data-ttu-id="464ba-120">Explique comment interagir avec les éléments de l’interface utilisateur du lecteur Windows Media qui permettent aux utilisateurs de se connecter à et de se déconnecter du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="464ba-120">Explains how to interact with Windows Media Player user interface elements that let users log in to and log out from the online store.</span></span>         |
| [<span data-ttu-id="464ba-121">Achat de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="464ba-121">Purchasing Media Content</span></span>](purchasing-media-content.md)                                                             | <span data-ttu-id="464ba-122">Explique comment le lecteur Windows Media et le plug-in du magasin en ligne interagissent lorsque l’utilisateur achète du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="464ba-122">Explains how Windows Media Player and the online store's plug-in interact when the user purchases media content.</span></span>                               |
| [<span data-ttu-id="464ba-123">Téléchargement du contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="464ba-123">Downloading Media Content</span></span>](downloading-media-content.md)                                                           | <span data-ttu-id="464ba-124">Explique comment le lecteur Windows Media et le plug-in du magasin en ligne interagissent quand l’utilisateur télécharge du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="464ba-124">Explains how Windows Media Player and the online store's plug-in interact when the user downloads media content.</span></span>                               |
| [<span data-ttu-id="464ba-125">Mise à jour des licences</span><span class="sxs-lookup"><span data-stu-id="464ba-125">Updating Licenses</span></span>](updating-licenses.md)                                                                           | <span data-ttu-id="464ba-126">Explique comment le lecteur Windows Media et le plug-in de la boutique en ligne interagissent pour maintenir à jour les licences de médias de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="464ba-126">Explains how Windows Media Player and the online store's plug-in interact to keep the user's media licenses current.</span></span>                           |
| [<span data-ttu-id="464ba-127">Mise à jour des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="464ba-127">Updating Portable Devices</span></span>](updating-portable-devices.md)                                                           | <span data-ttu-id="464ba-128">Explique comment le lecteur Windows Media et le plug-in de la boutique en ligne interagissent lorsque le contenu multimédia se déplace entre l’ordinateur et un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="464ba-128">Explains how Windows Media Player and the online store's plug-in interact when media content moves between the computer and a portable device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="464ba-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="464ba-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="464ba-130">**Tapez 1 magasins en ligne**</span><span class="sxs-lookup"><span data-stu-id="464ba-130">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




