---
title: Mappage des appareils Waveform-Audio
description: Mappage des appareils Waveform-Audio
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- audio multimédia, mappage d’appareils Wave Audio
- audio, mappage d’une forme d’onde-périphériques audio
- Audio Compression Manager (ACM), mappage d’appareils Wave Audio
- ACM (gestionnaire de compression audio), mappage d’appareils Wave-Audio
- mappage d’appareils Wave-Audio
- audio multimédia, Mappeur
- audio, Mappeur
- Audio Compression Manager (ACM), Mappeur
- ACM (gestionnaire de compression audio), Mappeur
- mappeur
- sons Waveform, périphériques de mappage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839746"
---
# <a name="mapping-waveform-audio-devices"></a><span data-ttu-id="87e87-114">Mappage des appareils Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="87e87-114">Mapping Waveform-Audio Devices</span></span>

<span data-ttu-id="87e87-115">Windows fournit un ensemble de fonctions standard pour les périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="87e87-115">Windows provides a set of standard functions for audio devices.</span></span> <span data-ttu-id="87e87-116">Ces fonctions émettent des appels aux pilotes de périphériques qui gèrent les périphériques matériels.</span><span class="sxs-lookup"><span data-stu-id="87e87-116">These functions issue calls to device drivers that manage hardware devices.</span></span> <span data-ttu-id="87e87-117">Le système utilise un module appelé « mappeur » pour gérer les appareils installés.</span><span class="sxs-lookup"><span data-stu-id="87e87-117">The system uses a module called a "mapper" to manage installed devices.</span></span> <span data-ttu-id="87e87-118">Le Mappeur utilise des raccordements spéciaux dans l’interface de pilote pour intercepter les appels et agir comme intermédiaire entre le système et les pilotes installés dans le système.</span><span class="sxs-lookup"><span data-stu-id="87e87-118">The mapper uses special hooks in the driver interface to intercept calls and to act as an intermediary between the system and the drivers installed in the system.</span></span> <span data-ttu-id="87e87-119">Le Mappeur est responsable de la correspondance des demandes d’une application pour l’accès à un appareil avec les appareils disponibles et pour la recherche d’un appareil qui répond aux exigences audio de l’application actuelle.</span><span class="sxs-lookup"><span data-stu-id="87e87-119">The mapper is responsible for matching an application's requests for access to a device with the available devices and for finding a device that meets the current application's audio requirements.</span></span> <span data-ttu-id="87e87-120">Le système fournit des mappeurs pour les types de pilotes standard : Waveform-Audio, MIDI (Musical Instrument Digital Interface) et appareils auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="87e87-120">The system provides mappers for standard driver types: waveform-audio, MIDI (Musical Instrument Digital Interface), and auxiliary devices.</span></span>

<span data-ttu-id="87e87-121">L’ACM est une extension du système multimédia de base et est installé en tant que Mappeur.</span><span class="sxs-lookup"><span data-stu-id="87e87-121">The ACM is an extension of the basic multimedia system and is installed as a mapper.</span></span> <span data-ttu-id="87e87-122">Cela signifie que l’ACM utilise les crochets du mappeur de l’interface du pilote pour les périphériques audio Waveform.</span><span class="sxs-lookup"><span data-stu-id="87e87-122">This means the ACM uses the driver-interface mapper hooks for waveform-audio devices.</span></span> <span data-ttu-id="87e87-123">L’utilisation de ces hooks permet à l’ACM de décoder ou de coder des données Waveform Audio avant de les transmettre vers ou à partir d’un pilote de périphérique Wave-audio.</span><span class="sxs-lookup"><span data-stu-id="87e87-123">Using these hooks allows the ACM to decode or encode waveform-audio data before passing it to or from a waveform-audio device driver.</span></span> <span data-ttu-id="87e87-124">La différence entre l’ACM et le mappeur de système standard est que l’ACM peut rechercher un périphérique Wave-audio qui prend en charge un format spécifié ou une combinaison d’un périphérique audio Waveform et d’un compresseur ou décompresseur ACM qui prend en charge un format spécifié.</span><span class="sxs-lookup"><span data-stu-id="87e87-124">The difference between the ACM and the standard system mapper is that the ACM can search for a waveform-audio device that supports a specified format or find a combination of a waveform-audio device and an ACM compressor or decompressor that supports a specified format.</span></span>

<span data-ttu-id="87e87-125">Quand une application demande que le système ouvre un appareil Waveform Audio pour l’entrée ou la sortie, la demande spécifie le format et l’appareil.</span><span class="sxs-lookup"><span data-stu-id="87e87-125">When an application requests that the system open a waveform-audio device for input or output, the request specifies the format and device.</span></span> <span data-ttu-id="87e87-126">Lorsque l’appareil spécifié est le Mappeur, le Mappeur doit trouver un appareil qui prend en charge le format spécifié.</span><span class="sxs-lookup"><span data-stu-id="87e87-126">When the specified device is the mapper, the mapper must find a device that supports the specified format.</span></span> <span data-ttu-id="87e87-127">Le Mappeur implémenté dans l’ACM recherche un périphérique Wave-Audio installé qui prend en charge le format spécifié.</span><span class="sxs-lookup"><span data-stu-id="87e87-127">The mapper implemented in the ACM searches for an installed waveform-audio device that supports the specified format.</span></span> <span data-ttu-id="87e87-128">Si l’ACM ne trouve pas ce type d’appareil, il recherche un périphérique Wave-audio et un compresseur ou un décompresseur qui, ensemble, prennent en charge le format.</span><span class="sxs-lookup"><span data-stu-id="87e87-128">If the ACM cannot find such a device, it searches for a waveform-audio device and a compressor or decompressor that together support the format.</span></span> <span data-ttu-id="87e87-129">Plus précisément, l’ACM recherche un compresseur ou un décompresseur qui convertit le format spécifié dans un format pris en charge par un périphérique audio Wave installé.</span><span class="sxs-lookup"><span data-stu-id="87e87-129">Specifically, the ACM searches for a compressor or decompressor that converts the specified format into a format that is supported by an installed waveform-audio device.</span></span> <span data-ttu-id="87e87-130">Une fois que l’ACM a trouvé un appareil qui prend en charge le format converti, il peut honorer les demandes de lecture ou d’enregistrement du format demandé à l’origine, même si aucun périphérique Wave-Audio installé ne prend directement en charge ce format.</span><span class="sxs-lookup"><span data-stu-id="87e87-130">After the ACM finds a device that supports the converted format, it can honor requests to play or record the format originally requested, even though no installed waveform-audio device directly supports that format.</span></span>

<span data-ttu-id="87e87-131">Outre la conversion de format, l’ACM offre également des services pour prendre en charge la compression, la décompression, le filtrage, la sélection de format et la sélection de filtres.</span><span class="sxs-lookup"><span data-stu-id="87e87-131">In addition to format conversion, the ACM also offers services to support compression, decompression, filtering, format selection, and filter selection.</span></span> <span data-ttu-id="87e87-132">Il fournit une API standard qu’il prend en charge en appelant ses propres pilotes.</span><span class="sxs-lookup"><span data-stu-id="87e87-132">It provides a standard API that it supports by calling its own drivers.</span></span>

 

 




