---
title: À propos de la synchronisation des appareils
description: À propos de la synchronisation des appareils
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Lecteur Windows Media, synchronisation des appareils
- Modèle objet du lecteur Windows Media, synchronisation des appareils
- modèle objet, synchronisation des appareils
- Contrôle ActiveX du lecteur Windows Media, synchronisation des appareils
- Contrôle ActiveX, synchronisation des appareils
- Windows Media Player Mobile contrôle ActiveX, synchronisation des appareils
- Windows Media Player Mobile, synchronisation des appareils
- synchronisation des appareils, à propos de
- synchronisation des appareils, à propos de
- synchronisation des appareils, transfert manuel
- synchronisation des appareils, transfert manuel
- synchronisation des appareils, synchronisation automatique
- synchronisation des appareils, synchronisation automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511419"
---
# <a name="about-device-synchronization"></a><span data-ttu-id="11dd4-116">À propos de la synchronisation des appareils</span><span class="sxs-lookup"><span data-stu-id="11dd4-116">About Device Synchronization</span></span>

<span data-ttu-id="11dd4-117">Le lecteur Windows Media 10 a introduit un nouveau modèle pour la synchronisation de contenu multimédia numérique avec des appareils portables.</span><span class="sxs-lookup"><span data-stu-id="11dd4-117">Windows Media Player 10 introduced a new model for synchronizing digital media content with portable devices.</span></span> <span data-ttu-id="11dd4-118">Du point de vue de l’utilisateur, cela signifie que vous pouvez spécifier les sélections (y compris les sélections automatiques) à synchroniser automatiquement avec les appareils.</span><span class="sxs-lookup"><span data-stu-id="11dd4-118">From the user's perspective, this means you can specify which playlists (including auto playlists) synchronize automatically with devices.</span></span> <span data-ttu-id="11dd4-119">Vous pouvez également transférer manuellement du contenu multimédia numérique vers des appareils.</span><span class="sxs-lookup"><span data-stu-id="11dd4-119">You can also manually transfer digital media content to devices.</span></span> <span data-ttu-id="11dd4-120">Du point de vue du développeur, cela signifie qu’il existe de nouvelles fonctionnalités que vous pouvez exploiter dans vos applications.</span><span class="sxs-lookup"><span data-stu-id="11dd4-120">From the developer's perspective, this means there is new functionality exposed that you can take advantage of in your applications.</span></span> <span data-ttu-id="11dd4-121">Pour ce faire, vous devez créer une instance distante du contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="11dd4-121">To do this, you must create a remoted instance of the Windows Media Player control.</span></span>

<span data-ttu-id="11dd4-122">Il existe deux façons pour un utilisateur de copier du contenu multimédia numérique sur un appareil :</span><span class="sxs-lookup"><span data-stu-id="11dd4-122">There are two ways a user can copy digital media content to a device:</span></span>

-   <span data-ttu-id="11dd4-123">**Transfert manuel.**</span><span class="sxs-lookup"><span data-stu-id="11dd4-123">**Manual transfer.**</span></span> <span data-ttu-id="11dd4-124">L’utilisateur sélectionne le contenu multimédia numérique dans la bibliothèque, puis lance un transfert du contenu vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11dd4-124">The user selects digital media content in the library and then initiates a transfer of the content to the device.</span></span> <span data-ttu-id="11dd4-125">Cela est similaire à la fonctionnalité fournie par les versions précédentes du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="11dd4-125">This is similar to the functionality provided by previous versions of Windows Media Player.</span></span> <span data-ttu-id="11dd4-126">Le kit de développement logiciel (SDK) du lecteur Windows Media ne fournit pas de méthodes pour transférer des médias numériques sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="11dd4-126">The Windows Media Player SDK does not provide methods for transferring digital media to a device.</span></span>
-   <span data-ttu-id="11dd4-127">**Synchronisation automatique.**</span><span class="sxs-lookup"><span data-stu-id="11dd4-127">**Automatic synchronization.**</span></span> <span data-ttu-id="11dd4-128">L’utilisateur spécifie les sélections qui se synchronisent automatiquement avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11dd4-128">The user specifies playlists that automatically synchronize with the device.</span></span> <span data-ttu-id="11dd4-129">Il s’agit d’une fonctionnalité du lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="11dd4-129">This is a feature of Windows Media Player 10 or later.</span></span> <span data-ttu-id="11dd4-130">Le kit de développement logiciel (SDK) Windows Media Player fournit des fonctionnalités permettant de gérer la synchronisation automatique.</span><span class="sxs-lookup"><span data-stu-id="11dd4-130">The Windows Media Player SDK provides functionality for managing automatic synchronization.</span></span> <span data-ttu-id="11dd4-131">Cette fonctionnalité est conçue pour vous permettre de créer une interface utilisateur personnalisée pour votre application afin de spécifier le comportement de la synchronisation des appareils et de fournir des informations d’État aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="11dd4-131">This functionality is designed to let you build a custom user interface for your application to specify how device synchronization happens and to provide status information to users.</span></span>

<span data-ttu-id="11dd4-132">Pour que la synchronisation automatique fonctionne, une relation spéciale doit être établie entre le lecteur Windows Media et l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11dd4-132">For automatic synchronization to work, a special relationship must be established between Windows Media Player and the device.</span></span> <span data-ttu-id="11dd4-133">Cette relation est appelée *partenariat*.</span><span class="sxs-lookup"><span data-stu-id="11dd4-133">This relationship is called a *partnership*.</span></span>

<span data-ttu-id="11dd4-134">Les sections suivantes fournissent plus d’informations sur la synchronisation des appareils.</span><span class="sxs-lookup"><span data-stu-id="11dd4-134">The following sections provide more information about device synchronization.</span></span>

-   [<span data-ttu-id="11dd4-135">À propos des appareils</span><span class="sxs-lookup"><span data-stu-id="11dd4-135">About Devices</span></span>](about-devices.md)
-   [<span data-ttu-id="11dd4-136">À propos des partenariats</span><span class="sxs-lookup"><span data-stu-id="11dd4-136">About Partnerships</span></span>](about-partnerships.md)
-   [<span data-ttu-id="11dd4-137">À propos du moteur de synchronisation</span><span class="sxs-lookup"><span data-stu-id="11dd4-137">About the Synchronization Engine</span></span>](about-the-synchronization-engine.md)
-   [<span data-ttu-id="11dd4-138">À propos de la synchronisation des sélections</span><span class="sxs-lookup"><span data-stu-id="11dd4-138">About Playlist Synchronization</span></span>](about-playlist-synchronization.md)

## <a name="related-topics"></a><span data-ttu-id="11dd4-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11dd4-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11dd4-140">**À propos du modèle objet Player**</span><span class="sxs-lookup"><span data-stu-id="11dd4-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="11dd4-141">**Utilisation à distance du contrôle Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="11dd4-141">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="11dd4-142">**Utilisation d’appareils mobiles**</span><span class="sxs-lookup"><span data-stu-id="11dd4-142">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




