---
title: Envoi de messages MIDI individuels
description: Envoi de messages MIDI individuels
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- Jeux de fichiers MIDI, envoi de messages
- envoi de messages MIDI
- MIDI (Musical Instrument Digital Interface), messages individuels
- MIDI (Musical Instrument Digital Interface), messages individuels
- Jeux de fichiers MIDI, messages individuels
- messages MIDI individuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106545743"
---
# <a name="sending-individual-midi-messages"></a><span data-ttu-id="32455-111">Envoi de messages MIDI individuels</span><span class="sxs-lookup"><span data-stu-id="32455-111">Sending Individual MIDI Messages</span></span>

<span data-ttu-id="32455-112">Vous pouvez utiliser des messages MIDI individuels à l’aide des fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="32455-112">You can work with individual MIDI messages by using the following functions.</span></span>



| <span data-ttu-id="32455-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="32455-113">Value</span></span>                                      | <span data-ttu-id="32455-114">Signification</span><span class="sxs-lookup"><span data-stu-id="32455-114">Meaning</span></span>                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32455-115">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="32455-115">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | <span data-ttu-id="32455-116">Envoie une mémoire tampon de données MIDI au périphérique de sortie MIDI spécifié.</span><span class="sxs-lookup"><span data-stu-id="32455-116">Sends a buffer of MIDI data to the specified MIDI output device.</span></span> <span data-ttu-id="32455-117">Utilisez cette fonction pour envoyer des messages système-exclusifs à un appareil MIDI.</span><span class="sxs-lookup"><span data-stu-id="32455-117">Use this function to send system-exclusive messages to a MIDI device.</span></span>                                              |
| [<span data-ttu-id="32455-118">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="32455-118">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | <span data-ttu-id="32455-119">Désactive toutes les notes sur tous les canaux pour un périphérique de sortie MIDI spécifié.</span><span class="sxs-lookup"><span data-stu-id="32455-119">Turns off all notes on all channels for a specified MIDI output device.</span></span> <span data-ttu-id="32455-120">Les mémoires tampons de flux et les mémoires tampons de flux System-exclusive en attente sont marquées comme terminées et retournées à l’application.</span><span class="sxs-lookup"><span data-stu-id="32455-120">Any pending system-exclusive buffers and stream buffers are marked as done and returned to the application.</span></span> |
| [<span data-ttu-id="32455-121">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="32455-121">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | <span data-ttu-id="32455-122">Envoie un message MIDI à un appareil de sortie MIDI spécifié.</span><span class="sxs-lookup"><span data-stu-id="32455-122">Sends a MIDI message to a specified MIDI output device.</span></span>                                                                                                                             |



 

<span data-ttu-id="32455-123">Pour envoyer un message MIDI (à l’exception des messages système exclusifs), utilisez [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span><span class="sxs-lookup"><span data-stu-id="32455-123">To send any MIDI message (except for system-exclusive messages), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span></span>

 

 