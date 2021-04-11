---
title: Architecture du mappeur MIDI
description: Architecture du mappeur MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, architecture
- Mappeur MIDI, plan d’installation
- Carte d’installation MIDI
- Mappeur MIDI, mappage de canal
- Mappeur MIDI, mappages de correctifs
- Mappeur MIDI, mappages de clés
- carte de canal
- mappages de correctifs
- cartes clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310825"
---
# <a name="the-midi-mapper-architecture"></a><span data-ttu-id="78700-114">Architecture du mappeur MIDI</span><span class="sxs-lookup"><span data-stu-id="78700-114">The MIDI Mapper Architecture</span></span>

<span data-ttu-id="78700-115">Le Mappeur MIDI utilise une carte d’installation MIDI pour déterminer comment traduire et rediriger les messages qu’il reçoit.</span><span class="sxs-lookup"><span data-stu-id="78700-115">The MIDI Mapper uses a MIDI setup map to determine how to translate and redirect the messages it receives.</span></span> <span data-ttu-id="78700-116">Une carte d’installation MIDI se compose des types de mappages suivants.</span><span class="sxs-lookup"><span data-stu-id="78700-116">A MIDI setup map consists of the following types of maps.</span></span>

-   [<span data-ttu-id="78700-117">Carte de canal</span><span class="sxs-lookup"><span data-stu-id="78700-117">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="78700-118">Mappages de correctifs</span><span class="sxs-lookup"><span data-stu-id="78700-118">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="78700-119">Cartes clés</span><span class="sxs-lookup"><span data-stu-id="78700-119">Key Maps</span></span>](key-maps.md)

<span data-ttu-id="78700-120">L’illustration suivante montre les rôles des cartes de canal, de correctif et de clé dans une carte d’installation MIDI.</span><span class="sxs-lookup"><span data-stu-id="78700-120">The following illustration shows the roles of channel, patch, and key maps in a MIDI setup map.</span></span>

![rôles de canaux, de correctifs et de clés dans une image de carte d’installation midi](images/mmap-a02.gif)

 

 




