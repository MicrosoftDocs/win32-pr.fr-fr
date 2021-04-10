---
title: Préchargement des correctifs avec des synthétiseurs MIDI internes
description: Préchargement des correctifs avec des synthétiseurs MIDI internes
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), synthétiseurs internes
- MIDI (Musical Instrument Digital Interface), synthétiseurs internes
- lire des fichiers MIDI, des synthétiseurs internes
- synthétiseurs MIDI internes
- Interface MIDI (Musical Instrument Digital Interface), préchargement des correctifs
- MIDI (Musical Instrument Digital Interface), préchargement des correctifs
- Jeux de fichiers MIDI, préchargement des correctifs
- préchargement des correctifs MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940901"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a><span data-ttu-id="cebcb-111">Préchargement des correctifs avec des synthétiseurs MIDI internes</span><span class="sxs-lookup"><span data-stu-id="cebcb-111">Preloading Patches with Internal MIDI Synthesizers</span></span>

<span data-ttu-id="cebcb-112">Certains appareils de synthétiseur MIDI internes ne peuvent pas conserver tous les correctifs chargés simultanément.</span><span class="sxs-lookup"><span data-stu-id="cebcb-112">Some internal MIDI synthesizer devices cannot keep all of their patches loaded simultaneously.</span></span> <span data-ttu-id="cebcb-113">Ces appareils doivent précharger leurs données de correctifs.</span><span class="sxs-lookup"><span data-stu-id="cebcb-113">These devices must preload their patch data.</span></span>

<span data-ttu-id="cebcb-114">Windows fournit les fonctions suivantes pour demander à un synthétiseur de précharger et de mettre en cache les correctifs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="cebcb-114">Windows provides the following functions to request that a synthesizer preload and cache specified patches.</span></span>



| <span data-ttu-id="cebcb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cebcb-115">Value</span></span>                                                      | <span data-ttu-id="cebcb-116">Signification</span><span class="sxs-lookup"><span data-stu-id="cebcb-116">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cebcb-117">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="cebcb-117">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | <span data-ttu-id="cebcb-118">Demande qu’un appareil de synthétiseur MIDI interne précharge et met en cache les correctifs Melodic spécifiés.</span><span class="sxs-lookup"><span data-stu-id="cebcb-118">Requests that an internal MIDI synthesizer device preload and cache specified melodic patches.</span></span>              |
| [<span data-ttu-id="cebcb-119">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="cebcb-119">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | <span data-ttu-id="cebcb-120">Demande qu’un appareil de synthétiseur MIDI interne précharge et met en cache les correctifs à percussion clé spécifiés.</span><span class="sxs-lookup"><span data-stu-id="cebcb-120">Requests that an internal MIDI synthesizer device preload and cache specified key-based percussion patches.</span></span> |



 

<span data-ttu-id="cebcb-121">Pour plus d’informations sur la façon de déterminer si un appareil particulier prend en charge le préchargement des correctifs, consultez [interrogation des périphériques de sortie MIDI](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="cebcb-121">For information on how to determine if a particular device supports preloading patches, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

 

 