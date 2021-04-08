---
title: Flux MIDI
description: Flux MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- MIDI (Musical Instrument Digital Interface), flux
- MIDI (Musical Instrument Digital Interface), flux
- mémoires tampons de flux, flux MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101596"
---
# <a name="midi-streams"></a><span data-ttu-id="fd794-106">Flux MIDI</span><span class="sxs-lookup"><span data-stu-id="fd794-106">MIDI Streams</span></span>

<span data-ttu-id="fd794-107">Les événements MIDI se produisent dans le contexte d’un flux de données MIDI.</span><span class="sxs-lookup"><span data-stu-id="fd794-107">MIDI events occur in the context of a stream of MIDI data.</span></span> <span data-ttu-id="fd794-108">Bien qu’une application puisse utiliser plusieurs flux pour définir des données musicales, le Mappeur MIDI ne reconnaît pas plusieurs flux.</span><span class="sxs-lookup"><span data-stu-id="fd794-108">Although an application can use several streams to define musical data, the MIDI mapper does not recognize multiple streams.</span></span> <span data-ttu-id="fd794-109">La plupart des applications qui utilisent des flux utilisent un flux MIDI unique.</span><span class="sxs-lookup"><span data-stu-id="fd794-109">Most applications that use streams use a single MIDI stream.</span></span>

<span data-ttu-id="fd794-110">Les fonctions suivantes fonctionnent avec les flux.</span><span class="sxs-lookup"><span data-stu-id="fd794-110">The following functions work with streams.</span></span>



| <span data-ttu-id="fd794-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd794-111">Value</span></span>                                            | <span data-ttu-id="fd794-112">Signification</span><span class="sxs-lookup"><span data-stu-id="fd794-112">Meaning</span></span>                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="fd794-113">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="fd794-113">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | <span data-ttu-id="fd794-114">Ferme un flux MIDI.</span><span class="sxs-lookup"><span data-stu-id="fd794-114">Closes a MIDI stream.</span></span>                                                   |
| [<span data-ttu-id="fd794-115">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="fd794-115">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | <span data-ttu-id="fd794-116">Ouvre un flux MIDI et récupère un handle.</span><span class="sxs-lookup"><span data-stu-id="fd794-116">Opens a MIDI stream and retrieves a handle.</span></span>                             |
| [<span data-ttu-id="fd794-117">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="fd794-117">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | <span data-ttu-id="fd794-118">Lit ou met en file d’attente un flux (mémoire tampon) de données MIDI sur un appareil de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="fd794-118">Plays or queues a stream (buffer) of MIDI data to a MIDI output device.</span></span> |
| [<span data-ttu-id="fd794-119">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="fd794-119">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | <span data-ttu-id="fd794-120">Suspend la lecture d’un flux MIDI spécifié.</span><span class="sxs-lookup"><span data-stu-id="fd794-120">Pauses playback of a specified MIDI stream.</span></span>                             |
| [<span data-ttu-id="fd794-121">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="fd794-121">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | <span data-ttu-id="fd794-122">Récupère la position actuelle dans un flux MIDI.</span><span class="sxs-lookup"><span data-stu-id="fd794-122">Retrieves the current position in a MIDI stream.</span></span>                        |
| [<span data-ttu-id="fd794-123">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="fd794-123">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | <span data-ttu-id="fd794-124">Définit et récupère les propriétés du flux.</span><span class="sxs-lookup"><span data-stu-id="fd794-124">Sets and retrieves stream properties.</span></span>                                   |
| [<span data-ttu-id="fd794-125">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="fd794-125">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | <span data-ttu-id="fd794-126">Redémarre la lecture d’un flux MIDI suspendu.</span><span class="sxs-lookup"><span data-stu-id="fd794-126">Restarts playback of a paused MIDI stream.</span></span>                              |
| [<span data-ttu-id="fd794-127">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="fd794-127">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | <span data-ttu-id="fd794-128">Désactive toutes les notes sur tous les canaux MIDI pour le flux MIDI spécifié.</span><span class="sxs-lookup"><span data-stu-id="fd794-128">Turns off all notes on all MIDI channels for the specified MIDI stream.</span></span> |



 

 

 