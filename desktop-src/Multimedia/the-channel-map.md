---
title: Carte de canal
description: Carte de canal
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, mappage de canal
- carte de canal
- Mappeur MIDI, messages de canal
- Messages de canal MIDI
- messages de canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100752"
---
# <a name="the-channel-map"></a><span data-ttu-id="d4023-110">Carte de canal</span><span class="sxs-lookup"><span data-stu-id="d4023-110">The Channel Map</span></span>

<span data-ttu-id="d4023-111">Le mappage de canal affecte tous les messages de canal MIDI.</span><span class="sxs-lookup"><span data-stu-id="d4023-111">The channel map affects all MIDI channel messages.</span></span> <span data-ttu-id="d4023-112">Les messages de canaux MIDI incluent les messages de Remarque on, de note de Polyphonic-Key-aftertouch, de contrôle-modification, de modification de programme, de canal aftertouch et de modification de la courbure.</span><span class="sxs-lookup"><span data-stu-id="d4023-112">MIDI channel messages include note-on, note-off, polyphonic-key-aftertouch, control-change, program-change, channel-aftertouch, and pitch-bend-change messages.</span></span> <span data-ttu-id="d4023-113">Le Mappeur MIDI utilise un mappage de canal unique avec une entrée pour chacun des 16 canaux MIDI.</span><span class="sxs-lookup"><span data-stu-id="d4023-113">The MIDI Mapper uses a single channel map with an entry for each of the 16 MIDI channels.</span></span> <span data-ttu-id="d4023-114">Chaque entrée de mappage de canal spécifie les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d4023-114">Each channel-map entry specifies the following:</span></span>

-   <span data-ttu-id="d4023-115">Canal de destination pour le message MIDI</span><span class="sxs-lookup"><span data-stu-id="d4023-115">A destination channel for the MIDI message</span></span>
-   <span data-ttu-id="d4023-116">Périphérique de sortie de destination pour le message MIDI</span><span class="sxs-lookup"><span data-stu-id="d4023-116">A destination output device for the MIDI message</span></span>
-   <span data-ttu-id="d4023-117">Carte de correctif facultative spécifiant d’autres modifications possibles pour le message MIDI</span><span class="sxs-lookup"><span data-stu-id="d4023-117">An optional patch map specifying other possible modifications for the MIDI message</span></span>

<span data-ttu-id="d4023-118">Le canal de destination est défini sur l’un des 16 canaux MIDI.</span><span class="sxs-lookup"><span data-stu-id="d4023-118">The destination channel is set to one of the 16 MIDI channels.</span></span> <span data-ttu-id="d4023-119">Les messages MIDI sont modifiés pour refléter chaque nouvelle attribution de canal.</span><span class="sxs-lookup"><span data-stu-id="d4023-119">MIDI messages are modified to reflect each new channel assignment.</span></span> <span data-ttu-id="d4023-120">Par exemple, si l’entrée de canal de destination pour MIDI Channel 4 est définie sur 6, tous les messages MIDI envoyés vers Channel 4 sont mappés à Channel 6, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d4023-120">For example, if the destination channel entry for MIDI channel 4 is set to 6, all MIDI messages sent to channel 4 will be mapped to channel 6, as shown in the following illustration.</span></span>

![image midi mappée](images/mmap-a05.gif)

<span data-ttu-id="d4023-122">Dans cet exemple, l’octet d’État MIDI 0x93 est mappé à 0x95.</span><span class="sxs-lookup"><span data-stu-id="d4023-122">In this example, the MIDI status byte 0x93 is mapped to 0x95.</span></span> <span data-ttu-id="d4023-123">Le poids faible d’un octet d’État MIDI spécifie le numéro de canal.</span><span class="sxs-lookup"><span data-stu-id="d4023-123">The low-order of a MIDI status byte specifies the channel number.</span></span> <span data-ttu-id="d4023-124">Les canaux source sont activés ou inactifs.</span><span class="sxs-lookup"><span data-stu-id="d4023-124">Source channels are set to either active or inactive.</span></span> <span data-ttu-id="d4023-125">Les messages envoyés aux canaux sources inactifs sont ignorés. un canal inactif est donc en effet muet ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="d4023-125">Messages sent to inactive source channels are ignored, so an inactive channel is in effect muted or turned off.</span></span>

<span data-ttu-id="d4023-126">L’appareil de sortie de destination est défini sur l’un des périphériques de sortie MIDI disponibles.</span><span class="sxs-lookup"><span data-stu-id="d4023-126">The destination output device is set to one of the available MIDI output devices.</span></span> <span data-ttu-id="d4023-127">Un périphérique de sortie MIDI peut être un synthétiseur interne ou un port de sortie MIDI physique.</span><span class="sxs-lookup"><span data-stu-id="d4023-127">A MIDI output device can be an internal synthesizer or a physical MIDI output port.</span></span>

<span data-ttu-id="d4023-128">Les messages système MIDI sont des messages MIDI (avec octets d’État) de 0xF0 à 0xFF.</span><span class="sxs-lookup"><span data-stu-id="d4023-128">MIDI system messages are MIDI messages (with status bytes) from 0xF0 to 0xFF.</span></span> <span data-ttu-id="d4023-129">Il n’existe aucun canal associé aux messages système MIDI, ils ne peuvent donc pas être mappés.</span><span class="sxs-lookup"><span data-stu-id="d4023-129">There is no channel associated with MIDI system messages, so they cannot be mapped.</span></span> <span data-ttu-id="d4023-130">Les messages système MIDI sont envoyés à tous les périphériques de sortie MIDI répertoriés dans une carte de canal.</span><span class="sxs-lookup"><span data-stu-id="d4023-130">MIDI system messages are sent to all MIDI output devices listed in a channel map.</span></span>

 

 




