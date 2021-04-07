---
title: Mémoires tampons de flux
description: Mémoires tampons de flux
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Multimédia Windows, mémoires tampons de flux
- multimédia, mémoires tampons de flux
- audio multimédia, mémoires tampons de flux
- audio, mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- mémoires tampons de flux, à propos de
- MIDIHDR, structure
- MIDIEVENT, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725349"
---
# <a name="stream-buffers"></a><span data-ttu-id="d4d3b-112">Mémoires tampons de flux</span><span class="sxs-lookup"><span data-stu-id="d4d3b-112">Stream Buffers</span></span>

<span data-ttu-id="d4d3b-113">Les applications peuvent utiliser des mémoires tampons de flux pour envoyer des flux d’événements MIDI à un appareil.</span><span class="sxs-lookup"><span data-stu-id="d4d3b-113">Applications can use stream buffers to send streams of MIDI events to a device.</span></span> <span data-ttu-id="d4d3b-114">Chaque mémoire tampon de flux est un bloc de mémoire vers lequel pointe une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="d4d3b-114">Each stream buffer is a block of memory pointed to by a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span> <span data-ttu-id="d4d3b-115">Ce bloc de mémoire contient des données pour un ou plusieurs événements MIDI, chacun d’eux étant défini par une structure [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="d4d3b-115">This block of memory contains data for one or more MIDI events, each of which is defined by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="d4d3b-116">Une application contrôle la mémoire tampon en appelant les fonctions de manipulation de flux, telles que [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)et [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span><span class="sxs-lookup"><span data-stu-id="d4d3b-116">An application controls the buffer by calling the stream-manipulation functions, such as [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout), and [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span></span>

-   [<span data-ttu-id="d4d3b-117">Format de mémoire tampon de flux</span><span class="sxs-lookup"><span data-stu-id="d4d3b-117">Stream Buffer Format</span></span>](stream-buffer-format.md)
-   [<span data-ttu-id="d4d3b-118">Informations de minutage</span><span class="sxs-lookup"><span data-stu-id="d4d3b-118">Timing Information</span></span>](timing-information.md)
-   [<span data-ttu-id="d4d3b-119">Types d’événements MIDI</span><span class="sxs-lookup"><span data-stu-id="d4d3b-119">MIDI Event Types</span></span>](midi-event-types.md)
-   [<span data-ttu-id="d4d3b-120">Flux MIDI</span><span class="sxs-lookup"><span data-stu-id="d4d3b-120">MIDI Streams</span></span>](midi-streams.md)

 

 