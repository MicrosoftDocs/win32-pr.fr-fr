---
title: À propos de la synchronisation des sélections
description: À propos de la synchronisation des sélections
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Lecteur Windows Media, synchronisation des sélections
- Modèle objet du lecteur Windows Media, synchronisation des sélections
- modèle objet, synchronisation des sélections
- Contrôle ActiveX du lecteur Windows Media, synchronisation des sélections
- Contrôle ActiveX, synchronisation des sélections
- Contrôle ActiveX Windows Media Player Mobile, synchronisation des sélections
- Lecteur Windows Media Mobile, synchronisation des sélections
- synchronisation des appareils, des sélections
- synchronisation des appareils, sélections
- sélections, synchronisation
- Sélections de métafichiers Windows Media, synchronisation
- sélections de métafichiers, synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314245"
---
# <a name="about-playlist-synchronization"></a><span data-ttu-id="affff-115">À propos de la synchronisation des sélections</span><span class="sxs-lookup"><span data-stu-id="affff-115">About Playlist Synchronization</span></span>

<span data-ttu-id="affff-116">Le lecteur Windows Media 10 (ou version ultérieure) est conçu pour synchroniser le contenu multimédia numérique sur des appareils à l’aide d’un modèle de synchronisation de sélection.</span><span class="sxs-lookup"><span data-stu-id="affff-116">Windows Media Player 10 or later is designed to synchronize digital media content to devices using a playlist synchronization model.</span></span> <span data-ttu-id="affff-117">Cela signifie que le contenu destiné à être copié sur un appareil doit faire partie d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="affff-117">This means that content intended to be copied to a device must be part of a playlist.</span></span> <span data-ttu-id="affff-118">Lorsque l’utilisateur choisit de transférer le contenu multimédia numérique individuel de son ordinateur vers un appareil, le lecteur Windows Media ajoute le contenu à une sélection par défaut pour la copie.</span><span class="sxs-lookup"><span data-stu-id="affff-118">When the user chooses to transfer individual digital media content from his or her computer to a device, Windows Media Player adds the content to a default playlist for copying.</span></span>

<span data-ttu-id="affff-119">Les API de synchronisation des périphériques du lecteur Windows Media sont également conçues pour fonctionner de la même manière.</span><span class="sxs-lookup"><span data-stu-id="affff-119">The Windows Media Player device synchronization APIs are designed to work like this as well.</span></span> <span data-ttu-id="affff-120">À l’instar de Windows Media Player, votre programme peut présenter à l’utilisateur une liste de sélections qu’il a définies.</span><span class="sxs-lookup"><span data-stu-id="affff-120">Like Windows Media Player, your program can present the user with a list of playlists that he or she has defined.</span></span> <span data-ttu-id="affff-121">Vous pouvez ensuite permettre à l’utilisateur de choisir les playlists à synchroniser avec un périphérique particulier et de définir l’ordre de priorité pour le processus de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="affff-121">You can then enable the user to choose which playlists to synchronize with a particular device and to set the priority order for the synchronization process.</span></span>

<span data-ttu-id="affff-122">Étant donné que les appareils mobiles ont une capacité de stockage limitée, il est possible pour l’utilisateur de choisir de synchroniser plus de contenu multimédia numérique que l’appareil peut stocker.</span><span class="sxs-lookup"><span data-stu-id="affff-122">Because portable devices have a limited storage capacity, it is possible for the user to choose to synchronize more digital media content than the device can store.</span></span> <span data-ttu-id="affff-123">Le lecteur Windows Media synchronise le contenu par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="affff-123">Windows Media Player synchronizes content in priority order.</span></span> <span data-ttu-id="affff-124">L’utilisateur peut définir l’ordre de priorité à l’aide d’une boîte de dialogue à laquelle vous pouvez accéder à partir de la fonctionnalité **appareils** .</span><span class="sxs-lookup"><span data-stu-id="affff-124">The user can define the priority order by using a dialog box that can be accessed from the **Devices** feature.</span></span> <span data-ttu-id="affff-125">En réponse à l’entrée utilisateur de votre programme, vous pouvez modifier l’ordre de priorité par programmation en modifiant les valeurs de certains attributs de sélection.</span><span class="sxs-lookup"><span data-stu-id="affff-125">In response to user input to your program, you can change the priority order programmatically by changing the values of certain playlist attributes.</span></span> <span data-ttu-id="affff-126">Collectivement, ces attributs sont appelés attributs de *synchronisation* .</span><span class="sxs-lookup"><span data-stu-id="affff-126">Collectively, these attributes are called the *Sync* attributes.</span></span>

<span data-ttu-id="affff-127">Chaque playlist d’une bibliothèque a 16 attributs de synchronisation : **Sync01** à **Sync16**.</span><span class="sxs-lookup"><span data-stu-id="affff-127">Each playlist in a library has 16 synchronization attributes: **Sync01** through **Sync16**.</span></span> <span data-ttu-id="affff-128">Chaque attribut représente l’appareil qui a l’index de partenariat correspondant.</span><span class="sxs-lookup"><span data-stu-id="affff-128">Each attribute represents the device that has the corresponding partnership index.</span></span> <span data-ttu-id="affff-129">La valeur de chaque attribut vous indique deux choses :</span><span class="sxs-lookup"><span data-stu-id="affff-129">The value of each attribute tells you two things:</span></span>

-   <span data-ttu-id="affff-130">Indique si la sélection doit être synchronisée avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="affff-130">Whether the playlist should be synchronized with the device.</span></span>
-   <span data-ttu-id="affff-131">Valeur de priorité pour la sélection.</span><span class="sxs-lookup"><span data-stu-id="affff-131">The priority value for the playlist.</span></span>

<span data-ttu-id="affff-132">La valeur zéro indique que le lecteur Windows Media ne doit pas tenter de synchroniser la playlist avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="affff-132">A value of zero indicates that Windows Media Player should not attempt to synchronize the playlist with the device.</span></span> <span data-ttu-id="affff-133">Toute autre valeur est un numéro de priorité.</span><span class="sxs-lookup"><span data-stu-id="affff-133">Any other value is a priority number.</span></span> <span data-ttu-id="affff-134">Les valeurs inférieures reçoivent une priorité plus élevée au moment de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="affff-134">Lower values receive higher priority at synchronization time.</span></span>

<span data-ttu-id="affff-135">Les sélections ont également un attribut **SyncOnly** qui indique si la sélection est disponible uniquement pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="affff-135">Playlists also have a **SyncOnly** attribute that indicates whether the playlist is available only for synchronization.</span></span>

<span data-ttu-id="affff-136">Les éléments individuels du contenu multimédia numérique contiennent également des métadonnées sur la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="affff-136">Individual items of digital media content contain metadata about synchronization as well.</span></span> <span data-ttu-id="affff-137">Lorsque vous récupérez un objet **média** à partir de la bibliothèque, vous pouvez inspecter la valeur de l’attribut **SyncState** .</span><span class="sxs-lookup"><span data-stu-id="affff-137">When you retrieve a **Media** object from the library, you can inspect the value of the **SyncState** attribute.</span></span> <span data-ttu-id="affff-138">Cet attribut fournit des informations étendues indiquant si le contenu a été correctement copié sur l’appareil ou si la copie du contenu a échoué en raison de l’impossibilité de le faire.</span><span class="sxs-lookup"><span data-stu-id="affff-138">This attribute provides extended information about whether the content has been successfully copied to the device or whether copying the content failed because it would not fit.</span></span>

> [!Note]  
> <span data-ttu-id="affff-139">Vous devez éviter de fournir des éléments d’interface utilisateur qui permettent à l’utilisateur de créer des listes de lecture à partir de tout le contenu de la bibliothèque pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="affff-139">You should avoid providing user interface elements that enable the user to create playlists from all library content for synchronization.</span></span>

 

<span data-ttu-id="affff-140">Pour optimiser les performances, le lecteur Windows Media met en œuvre un ensemble de règles pour la création de sélections de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="affff-140">To optimize performance, Windows Media Player enforces a set of rules for creating synchronization playlists.</span></span> <span data-ttu-id="affff-141">Votre programme doit uniquement créer des sélections de synchronisation pour le contenu que vous avez fourni.</span><span class="sxs-lookup"><span data-stu-id="affff-141">Your program should only create synchronization playlists for content you provided.</span></span> <span data-ttu-id="affff-142">Autoriser le lecteur Windows Media à créer des sélections de synchronisation pour le contenu que l’utilisateur a ajouté à la bibliothèque à partir d’autres sources.</span><span class="sxs-lookup"><span data-stu-id="affff-142">Allow Windows Media Player to create synchronization playlists for content that the user added to the library from other sources.</span></span>

<span data-ttu-id="affff-143">Au lieu de créer votre propre interface utilisateur de sélection, vous pouvez présenter aux utilisateurs une boîte de dialogue par défaut pour choisir des sélections et gérer le partenariat pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="affff-143">As an alternative to creating your own playlist user interface, you can present users with a default dialog box for choosing playlists and managing the partnership for a device.</span></span> <span data-ttu-id="affff-144">Pour ce faire, appelez [IWMPSyncDevice :: showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span><span class="sxs-lookup"><span data-stu-id="affff-144">To do this, call [IWMPSyncDevice::showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span></span> <span data-ttu-id="affff-145">Lorsque vous appelez cette méthode, le lecteur Windows Media affiche la boîte de dialogue Paramètres de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="affff-145">When you invoke this method, Windows Media Player displays its synchronization settings dialog box.</span></span> <span data-ttu-id="affff-146">Lorsque l’utilisateur ferme la boîte de dialogue, le lecteur Windows Media revient automatiquement à son état d’ancrage antérieur et transmet le contrôle à votre programme distant.</span><span class="sxs-lookup"><span data-stu-id="affff-146">When the user closes the dialog box, Windows Media Player automatically returns to its prior docking state and passes control back to your remoted program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="affff-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="affff-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="affff-148">**À propos de la synchronisation des appareils**</span><span class="sxs-lookup"><span data-stu-id="affff-148">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="affff-149">**Gestion des sélections de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="affff-149">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="affff-150">**Attributs de sélection**</span><span class="sxs-lookup"><span data-stu-id="affff-150">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> </dl>

 

 




