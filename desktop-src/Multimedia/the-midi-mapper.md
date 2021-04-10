---
title: Le Mappeur MIDI
description: Le Mappeur MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows Multimedia, Mappeur MIDI
- multimédia, Mappeur MIDI
- audio multimédia, Mappeur MIDI
- audio, Mappeur MIDI
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, à propos de
- Mappeur MIDI, source
- Mappeur MIDI, destination
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029036"
---
# <a name="the-midi-mapper"></a><span data-ttu-id="cbaea-112">Le Mappeur MIDI</span><span class="sxs-lookup"><span data-stu-id="cbaea-112">The MIDI Mapper</span></span>

<span data-ttu-id="cbaea-113">Les services de correctif standard du mappeur MIDI fournissent une lecture de fichier MIDI indépendante de l’appareil pour les applications.</span><span class="sxs-lookup"><span data-stu-id="cbaea-113">The MIDI Mapper's standard patch services provide device-independent MIDI file playback for applications.</span></span> <span data-ttu-id="cbaea-114">Le Mappeur MIDI peut être utilisé avec MCI MIDI Sequencer ou avec des services de sortie MIDI de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="cbaea-114">The MIDI Mapper can be used with the MCI MIDI sequencer or with low-level MIDI output services.</span></span>

<span data-ttu-id="cbaea-115">Sauf indication contraire, toutes les références aux numéros de canaux MIDI utilisent les nombres de canaux logiques 1 à 16.</span><span class="sxs-lookup"><span data-stu-id="cbaea-115">Unless stated otherwise, all references to MIDI channel numbers use the logical channel numbers 1 through 16.</span></span> <span data-ttu-id="cbaea-116">Ces numéros de canaux logiques correspondent aux numéros de canaux physiques de 0 à 15 qui font en fait partie du message MIDI.</span><span class="sxs-lookup"><span data-stu-id="cbaea-116">These logical channel numbers correspond to the physical channel numbers 0 through 15 that are actually part of the MIDI message.</span></span> <span data-ttu-id="cbaea-117">Toutes les références aux valeurs de clé et de modification de programme MIDI utilisent les valeurs physiques 0 à 127.</span><span class="sxs-lookup"><span data-stu-id="cbaea-117">All references to MIDI program-change and key values use the physical values 0 through 127.</span></span> <span data-ttu-id="cbaea-118">Tous les nombres sont décimaux sauf s’ils sont précédés du préfixe « 0x », auquel cas ils sont hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="cbaea-118">All numbers are decimal unless preceded by "0x" prefix, in which case they are hexadecimal.</span></span>

<span data-ttu-id="cbaea-119">Dans la discussion sur le Mappeur MIDI, le terme *source* fait référence à la partie entrée du mappeur midi.</span><span class="sxs-lookup"><span data-stu-id="cbaea-119">In the discussion of the MIDI Mapper, the term *source* refers to the input side of the MIDI Mapper.</span></span> <span data-ttu-id="cbaea-120">Le terme *destination* fait référence au côté sortie du mappeur midi.</span><span class="sxs-lookup"><span data-stu-id="cbaea-120">The term *destination* refers to the output side of the MIDI Mapper.</span></span> <span data-ttu-id="cbaea-121">Par exemple, un canal source est le canal MIDI d’un message envoyé au mappeur MIDI, et un canal de destination est le canal MIDI d’un message envoyé du mappeur MIDI à un périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="cbaea-121">For example, a source channel is the MIDI channel of a message sent to the MIDI Mapper, and a destination channel is the MIDI channel of a message sent from the MIDI Mapper to an output device.</span></span>

-   [<span data-ttu-id="cbaea-122">Le Mappeur MIDI et Windows</span><span class="sxs-lookup"><span data-stu-id="cbaea-122">The MIDI Mapper and Windows</span></span>](the-midi-mapper-and-windows.md)
-   [<span data-ttu-id="cbaea-123">Architecture du mappeur MIDI</span><span class="sxs-lookup"><span data-stu-id="cbaea-123">The MIDI Mapper Architecture</span></span>](the-midi-mapper-architecture.md)
-   [<span data-ttu-id="cbaea-124">Carte de canal</span><span class="sxs-lookup"><span data-stu-id="cbaea-124">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="cbaea-125">Mappages de correctifs</span><span class="sxs-lookup"><span data-stu-id="cbaea-125">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="cbaea-126">Le volume scalaire</span><span class="sxs-lookup"><span data-stu-id="cbaea-126">The Volume Scalar</span></span>](the-volume-scalar.md)
-   [<span data-ttu-id="cbaea-127">Cartes clés</span><span class="sxs-lookup"><span data-stu-id="cbaea-127">Key Maps</span></span>](key-maps.md)
-   [<span data-ttu-id="cbaea-128">Résumé des cartes et des messages MIDI</span><span class="sxs-lookup"><span data-stu-id="cbaea-128">Summary of Maps and MIDI Messages</span></span>](summary-of-maps-and-midi-messages.md)

 

 




