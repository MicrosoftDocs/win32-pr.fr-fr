---
title: MCI (Media Control Interface)
description: MCI (Media Control Interface)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Multimédia Windows, MCI (Media Control Interface)
- multimédia, MCI (Media Control Interface)
- audio multimédia, MCI (Media Control Interface)
- audio, MCI (Media Control Interface)
- Interface MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MCI (Media Control Interface), MIDI (Musical Instrument Digital Interface)
- MCI (Media Control Interface), MIDI (Musical Instrument Digital Interface)
- MCI (Media Control Interface), MIDI Sequencer
- MCI (Media Control Interface), MIDI Sequencer
- Séquenceur MIDI MCI, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029135"
---
# <a name="media-control-interface-mci"></a><span data-ttu-id="e63bb-114">MCI (Media Control Interface)</span><span class="sxs-lookup"><span data-stu-id="e63bb-114">Media Control Interface (MCI)</span></span>

<span data-ttu-id="e63bb-115">MCI MIDI Sequencer est le composant système MCI qui lit les fichiers MIDI.</span><span class="sxs-lookup"><span data-stu-id="e63bb-115">The MCI MIDI sequencer is the MCI system component that plays MIDI files.</span></span> <span data-ttu-id="e63bb-116">Les applications peuvent lire des fichiers MIDI facilement à l’aide de MCI, mais MCI impose les restrictions suivantes sur les fonctionnalités MIDI :</span><span class="sxs-lookup"><span data-stu-id="e63bb-116">Applications can play MIDI files easily using MCI, but MCI imposes the following restrictions on MIDI capabilities:</span></span>

-   <span data-ttu-id="e63bb-117">MCI prend en charge la sortie MIDI uniquement.</span><span class="sxs-lookup"><span data-stu-id="e63bb-117">MCI supports MIDI output only.</span></span>
-   <span data-ttu-id="e63bb-118">MCI n’autorise pas la synchronisation étroite entre les événements MIDI et les autres événements en temps réel (tels que la vidéo).</span><span class="sxs-lookup"><span data-stu-id="e63bb-118">MCI does not allow close synchronization between MIDI events and other real-time events (such as video).</span></span>

<span data-ttu-id="e63bb-119">Si vous avez besoin d’une synchronisation MIDI exacte, vous devez utiliser les mémoires tampons de flux ou les services MIDI.</span><span class="sxs-lookup"><span data-stu-id="e63bb-119">If you need accurate MIDI synchronization, you must use the stream buffers or the MIDI services.</span></span> <span data-ttu-id="e63bb-120">Si vous avez besoin de fonctionnalités d’entrée MIDI, vous devez utiliser les services MIDI.</span><span class="sxs-lookup"><span data-stu-id="e63bb-120">If you need MIDI input capabilities, you must use the MIDI services.</span></span>

<span data-ttu-id="e63bb-121">Le séquenceur MIDI MCI lit les fichiers MIDI standard et les fichiers MIDI RIFF (Resource Interchange File Format), appelés fichiers RMID.</span><span class="sxs-lookup"><span data-stu-id="e63bb-121">The MCI MIDI sequencer plays standard MIDI files and resource interchange file format (RIFF) MIDI files, known as RMID files.</span></span> <span data-ttu-id="e63bb-122">Les fichiers MIDI standard sont conformes à la spécification [1,0 des fichiers MIDI standard](creating-midi-files.md) .</span><span class="sxs-lookup"><span data-stu-id="e63bb-122">Standard MIDI files conform to the [Standard MIDI Files 1.0](creating-midi-files.md) specification.</span></span> <span data-ttu-id="e63bb-123">Étant donné que les fichiers RMID sont des fichiers MIDI standard avec un en-tête RIFF, les informations sur les fichiers MIDI standard s’appliquent également aux fichiers RMID.</span><span class="sxs-lookup"><span data-stu-id="e63bb-123">Because RMID files are standard MIDI files with a RIFF header, information about standard MIDI files also applies to RMID files.</span></span> <span data-ttu-id="e63bb-124">Pour plus d’informations sur les fichiers RIFF, consultez [services de format de fichier](resource-interchange-file-format-services.md)de l’échange de ressources.</span><span class="sxs-lookup"><span data-stu-id="e63bb-124">For more information about RIFF files, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

<span data-ttu-id="e63bb-125">Bien qu’il existe actuellement trois types de fichiers MIDI standard, le séquenceur MCI ne lit que deux d’entre eux : le format 0 et le format 1 fichiers MIDI.</span><span class="sxs-lookup"><span data-stu-id="e63bb-125">Although there are currently three kinds of standard MIDI files, the MCI sequencer plays only two of them: Format 0 and Format 1 MIDI files.</span></span>

<span data-ttu-id="e63bb-126">Pour plus d’informations sur le contrôle des appareils multimédias (y compris les séquenceurs) à l’aide des commandes MCI, consultez [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="e63bb-126">For more information about controlling multimedia devices (including sequencers) using MCI commands, see [MCI](mci.md).</span></span>

 

 




