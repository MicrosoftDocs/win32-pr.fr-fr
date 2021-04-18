---
title: Allocation et préparation des blocs de données MIDI
description: Allocation et préparation des blocs de données MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Interface MIDI (Musical Instrument Digital Interface), allouer des blocs de données
- MIDI (Musical Instrument Digital Interface), allouer des blocs de données
- Services MIDI, allouer des blocs de données
- allouer des blocs de données MIDI
- Interface MIDI (Musical Instrument Digital Interface), préparation des blocs de données
- MIDI (Musical Instrument Digital Interface), préparation des blocs de données
- Services MIDI, préparation des blocs de données
- préparation des blocs de données MIDI
- MIDI (Musical Instrument Digital Interface), blocs de données
- MIDI (Musical Instrument Digital Interface), blocs de données
- Services MIDI, blocs de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509440"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a><span data-ttu-id="a19b8-114">Allocation et préparation des blocs de données MIDI</span><span class="sxs-lookup"><span data-stu-id="a19b8-114">Allocating and Preparing MIDI Data Blocks</span></span>

<span data-ttu-id="a19b8-115">Les fonctions [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)et [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) requièrent que les applications allouent des blocs de données à transmettre aux pilotes de périphérique à des fins de lecture ou d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a19b8-115">The [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer), and [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) functions require that applications to allocate data blocks to pass to the device drivers for playback or recording purposes.</span></span> <span data-ttu-id="a19b8-116">Chacune de ces fonctions utilise une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) pour décrire son bloc de données.</span><span class="sxs-lookup"><span data-stu-id="a19b8-116">Each of these functions uses a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure to describe its data block.</span></span>

<span data-ttu-id="a19b8-117">Avant d’utiliser l’une de ces fonctions pour passer un bloc de données à un pilote de périphérique, vous devez allouer de la mémoire pour la mémoire tampon et la structure d’en-tête qui décrit le bloc de données.</span><span class="sxs-lookup"><span data-stu-id="a19b8-117">Before you use one of these functions to pass a data block to a device driver, you must allocate memory for the buffer and the header structure that describes the data block.</span></span>

<span data-ttu-id="a19b8-118">Windows fournit les fonctions suivantes pour la préparation et le nettoyage des blocs de données MIDI.</span><span class="sxs-lookup"><span data-stu-id="a19b8-118">Windows provides the following functions for preparing and cleaning up MIDI data blocks.</span></span>



| <span data-ttu-id="a19b8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a19b8-119">Value</span></span>                                                    | <span data-ttu-id="a19b8-120">Signification</span><span class="sxs-lookup"><span data-stu-id="a19b8-120">Meaning</span></span>                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="a19b8-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="a19b8-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | <span data-ttu-id="a19b8-122">Prépare un bloc de données d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="a19b8-122">Prepares a MIDI input data block.</span></span>                      |
| [<span data-ttu-id="a19b8-123">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="a19b8-123">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | <span data-ttu-id="a19b8-124">Nettoie la préparation d’un bloc de données d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="a19b8-124">Cleans up the preparation of a MIDI input data block.</span></span>  |
| [<span data-ttu-id="a19b8-125">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="a19b8-125">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | <span data-ttu-id="a19b8-126">Prépare un bloc de données de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="a19b8-126">Prepares a MIDI output data block.</span></span>                     |
| [<span data-ttu-id="a19b8-127">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="a19b8-127">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | <span data-ttu-id="a19b8-128">Nettoie la préparation d’un bloc de données de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="a19b8-128">Cleans up the preparation of a MIDI output data block.</span></span> |



 

<span data-ttu-id="a19b8-129">Avant de passer un bloc de données MIDI à un pilote de périphérique, vous devez préparer la mémoire tampon en la transmettant à la fonction [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) ou [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) .</span><span class="sxs-lookup"><span data-stu-id="a19b8-129">Before you pass a MIDI data block to a device driver, you must prepare the buffer by passing it to the [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) or [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function.</span></span> <span data-ttu-id="a19b8-130">Lorsque le pilote de périphérique est terminé avec la mémoire tampon et le retourne, vous devez nettoyer cette préparation en passant la mémoire tampon à la fonction [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) ou [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) avant que toute mémoire allouée puisse être libérée.</span><span class="sxs-lookup"><span data-stu-id="a19b8-130">When the device driver is finished with the buffer and returns it, you must clean up this preparation by passing the buffer to the [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) or [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) function before any allocated memory can be freed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a19b8-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a19b8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a19b8-132">Services MIDI</span><span class="sxs-lookup"><span data-stu-id="a19b8-132">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 