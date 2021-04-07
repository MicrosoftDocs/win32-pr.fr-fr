---
title: À propos de MIDI
description: À propos de MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Multimédia Windows, MIDI (Musical Instrument Digital Interface)
- multimédia, MIDI (Musical Instrument Digital Interface)
- audio multimédia, MIDI (Musical Instrument Digital Interface)
- audio, MIDI (Musical Instrument Digital Interface)
- Interface MIDI (Musical Instrument Digital Interface), à propos de
- MIDI (Musical Instrument Digital Interface), à propos de
- Interface MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), services MIDI
- MIDI (Musical Instrument Digital Interface), services MIDI
- MCI (Media Control Interface), MIDI (Musical Instrument Digital Interface)
- MCI (Media Control Interface), MIDI (Musical Instrument Digital Interface)
- mémoires tampons de flux, à propos de
- Services MIDI, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672150"
---
# <a name="about-midi"></a><span data-ttu-id="8b9c3-119">À propos de MIDI</span><span class="sxs-lookup"><span data-stu-id="8b9c3-119">About MIDI</span></span>

<span data-ttu-id="8b9c3-120">L’interface de programmation d’applications (API) Microsoft Win32 fournit les méthodes suivantes pour que les applications fonctionnent avec des données MIDI :</span><span class="sxs-lookup"><span data-stu-id="8b9c3-120">The Microsoft Win32 application programming interface (API) provides the following methods for applications to work with MIDI data:</span></span>

-   <span data-ttu-id="8b9c3-121">L’interface MCI (Media Control Interface).</span><span class="sxs-lookup"><span data-stu-id="8b9c3-121">The Media Control Interface (MCI).</span></span> <span data-ttu-id="8b9c3-122">Bien que la façon la plus simple de lire un fichier MIDI consiste à utiliser la classe de fenêtre MCIWnd, vous pouvez également utiliser des commandes MCI pour créer une interface personnalisée sur un appareil MIDI.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-122">Although the simplest way to play a MIDI file is to use the MCIWnd window class, you can also use MCI commands to create a customized interface to a MIDI device.</span></span> <span data-ttu-id="8b9c3-123">Pour plus d’informations sur la classe de fenêtre MCIWnd, consultez [classe de fenêtre MCIWnd](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="8b9c3-123">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span> <span data-ttu-id="8b9c3-124">Pour plus d’informations sur MCI, consultez [MCI](mci.md)ou [MCI (Media Control Interface)](media-control-interface--mci.md).</span><span class="sxs-lookup"><span data-stu-id="8b9c3-124">For more information about MCI, see [MCI](mci.md), or [Media Control Interface (MCI)](media-control-interface--mci.md).</span></span>
-   <span data-ttu-id="8b9c3-125">[Mémoires tampons de flux](stream-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="8b9c3-125">[Stream Buffers](stream-buffers.md).</span></span> <span data-ttu-id="8b9c3-126">Ce format permet à une application de manipuler des mémoires tampons de données MIDI horodatées pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-126">This format allows an application to manipulate buffers of time-stamped MIDI data for playback.</span></span> <span data-ttu-id="8b9c3-127">Les mémoires tampons de flux sont utiles pour les applications qui requièrent un contrôle plus précis de la sortie que les offres MCI.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-127">Stream buffers are useful to applications that require more precise control over output than MCI offers.</span></span>
-   <span data-ttu-id="8b9c3-128">[Services midi](midi-services.md).</span><span class="sxs-lookup"><span data-stu-id="8b9c3-128">[MIDI Services](midi-services.md).</span></span> <span data-ttu-id="8b9c3-129">Les applications qui ont besoin d’un contrôle plus précis des données MIDI utilisent généralement ces services de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-129">Applications that need the most precise control of MIDI data typically use these low-level services.</span></span>

<span data-ttu-id="8b9c3-130">Les rubriques suivantes décrivent chacune de ces méthodes et fournissent une vue d’ensemble du mappeur MIDI.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-130">The following topics discuss each of these methods and provides an overview of the MIDI Mapper.</span></span>

-   [<span data-ttu-id="8b9c3-131">Le Mappeur MIDI</span><span class="sxs-lookup"><span data-stu-id="8b9c3-131">The MIDI Mapper</span></span>](the-midi-mapper.md)
-   [<span data-ttu-id="8b9c3-132">MCI (Media Control Interface)</span><span class="sxs-lookup"><span data-stu-id="8b9c3-132">Media Control Interface (MCI)</span></span>](media-control-interface--mci.md)
-   [<span data-ttu-id="8b9c3-133">Mémoires tampons de flux</span><span class="sxs-lookup"><span data-stu-id="8b9c3-133">Stream Buffers</span></span>](stream-buffers.md)
-   [<span data-ttu-id="8b9c3-134">Services MIDI</span><span class="sxs-lookup"><span data-stu-id="8b9c3-134">MIDI Services</span></span>](midi-services.md)
-   [<span data-ttu-id="8b9c3-135">Jeux de fichiers MIDI en train de fonctionner</span><span class="sxs-lookup"><span data-stu-id="8b9c3-135">Playing MIDI Files</span></span>](playing-midi-files.md)
-   [<span data-ttu-id="8b9c3-136">Enregistrement d’un fichier audio MIDI</span><span class="sxs-lookup"><span data-stu-id="8b9c3-136">Recording MIDI Audio</span></span>](recording-midi-audio.md)
-   [<span data-ttu-id="8b9c3-137">Traitement des données MIDI à partir de deux sources MIDI</span><span class="sxs-lookup"><span data-stu-id="8b9c3-137">Processing MIDI Data from Two MIDI Sources</span></span>](processing-midi-data-from-two-midi-sources.md)
-   [<span data-ttu-id="8b9c3-138">Création de fichiers MIDI</span><span class="sxs-lookup"><span data-stu-id="8b9c3-138">Creating MIDI Files</span></span>](creating-midi-files.md)

 

 




