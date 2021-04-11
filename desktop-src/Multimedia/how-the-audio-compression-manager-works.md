---
title: Fonctionnement du gestionnaire de compression audio
description: Fonctionnement du gestionnaire de compression audio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- audio multimédia, gestionnaire de compression audio (ACM)
- audio, gestionnaire de compression audio (ACM)
- Audio Compression Manager (ACM), à propos de
- ACM (gestionnaire de compression audio), à propos de
- Audio Compression Manager (ACM), pilotes de codec
- ACM (gestionnaire de compression audio), pilotes de codec
- Audio Compression Manager (ACM), pilotes de convertisseur de format
- ACM (gestionnaire de compression audio), pilotes de convertisseur de format
- Gestionnaire de compression audio (ACM), pilotes de filtre
- ACM (gestionnaire de compression audio), pilotes de filtre
- Gestionnaire de compression audio (ACM), pilotes de compresseur
- ACM (gestionnaire de compression audio), pilotes de compresseur
- le gestionnaire de compression audio (ACM), les pilotes de décompresseur
- ACM (gestionnaire de compression audio), pilotes de décompresseur
- pilotes de codec
- mettre en forme les pilotes de convertisseur
- filtrer les pilotes
- pilotes de compresseur
- pilotes de décompresseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310341"
---
# <a name="how-the-audio-compression-manager-works"></a><span data-ttu-id="8f5b2-122">Fonctionnement du gestionnaire de compression audio</span><span class="sxs-lookup"><span data-stu-id="8f5b2-122">How the Audio Compression Manager Works</span></span>

<span data-ttu-id="8f5b2-123">L’ACM utilise des hooks d’interface de pilote existants pour remplacer l’algorithme de mappage par défaut pour les périphériques audio Waveform.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-123">The ACM uses existing driver interface hooks to override the default mapping algorithm for waveform-audio devices.</span></span> <span data-ttu-id="8f5b2-124">Cela permet à l’ACM d’intercepter les appels d’appareils ouverts.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-124">This allows the ACM to intercept device-open calls.</span></span> <span data-ttu-id="8f5b2-125">Une fois qu’un appel a été intercepté, l’ACM peut effectuer diverses tâches pour traiter les données audio, telles que l’insertion d’un compresseur externe ou d’un décompresseur dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-125">After a call has been intercepted, the ACM can perform a variety of tasks to process the audio data, such as inserting an external compressor or decompressor into the sequence.</span></span>

<span data-ttu-id="8f5b2-126">L’ACM gère les types de pilotes suivants :</span><span class="sxs-lookup"><span data-stu-id="8f5b2-126">The ACM manages the following types of drivers:</span></span>

-   <span data-ttu-id="8f5b2-127">Pilotes de compresseur et décompresseur (codec)</span><span class="sxs-lookup"><span data-stu-id="8f5b2-127">Compressor and decompressor (codec) drivers</span></span>
-   <span data-ttu-id="8f5b2-128">Mettre en forme les pilotes de convertisseur</span><span class="sxs-lookup"><span data-stu-id="8f5b2-128">Format converter drivers</span></span>
-   <span data-ttu-id="8f5b2-129">Filtrer les pilotes</span><span class="sxs-lookup"><span data-stu-id="8f5b2-129">Filter drivers</span></span>

<span data-ttu-id="8f5b2-130">Les compresseurs et les décompresseurs modifient un type de format.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-130">Compressors and decompressors change one format type to another.</span></span> <span data-ttu-id="8f5b2-131">Par exemple, un compresseur ou un décompresseur peut modifier un fichier PCM (modulation d’impulsions de code) en un fichier ADPCM (adaptative différentielle Pulse Code Modulation).</span><span class="sxs-lookup"><span data-stu-id="8f5b2-131">For example, a compressor or decompressor can change a PCM (Pulse Code Modulation) file to an ADPCM (Adaptive Differential Pulse Code Modulation) file.</span></span> <span data-ttu-id="8f5b2-132">Les convertisseurs de format modifient le format, mais pas le type de données.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-132">Format converters change the format, but not the data type.</span></span> <span data-ttu-id="8f5b2-133">Par exemple, un convertisseur peut modifier les données 44-kHz, 16 bits en données de 44 kHz, 8 bits.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-133">For example, a converter can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span> <span data-ttu-id="8f5b2-134">Les filtres ne changent pas du tout le format des données, mais ils modifient les données Waveform-Audio d’une certaine manière.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-134">Filters do not change the data format at all, but they change the waveform-audio data in some manner.</span></span> <span data-ttu-id="8f5b2-135">Par exemple, un filtre peut combiner un flux de données et un écho de lui-même.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-135">For example, a filter could combine a data stream and an echo of itself.</span></span> <span data-ttu-id="8f5b2-136">Un pilote ACM unique, ou une balise de filtre ou de format dans un pilote, peut également prendre en charge des combinaisons des types précédents.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-136">A single ACM driver, or a filter tag or format tag within a driver, might also support combinations of the preceding types.</span></span>

<span data-ttu-id="8f5b2-137">Pour la sortie Waveform-Audio, l’ACM passe chaque mémoire tampon de données au convertisseur à mesure qu’elle arrive.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-137">For waveform-audio output, the ACM passes each buffer of data to the converter as it arrives.</span></span> <span data-ttu-id="8f5b2-138">Le convertisseur décompresse les données et retourne les données décompressées à l’ACM dans une mémoire tampon « Shadow ».</span><span class="sxs-lookup"><span data-stu-id="8f5b2-138">The converter decompresses the data and returns the decompressed data to the ACM in a "shadow" buffer.</span></span> <span data-ttu-id="8f5b2-139">L’ACM transmet ensuite le tampon d’ombre décompressé au pilote Wave-audio.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-139">The ACM then passes the decompressed shadow buffer to the waveform-audio driver.</span></span> <span data-ttu-id="8f5b2-140">L’ACM alloue les mémoires tampons d’ombre à chaque fois qu’il reçoit un message de préparation.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-140">The ACM allocates the shadow buffers whenever it receives a prepare message.</span></span>

<span data-ttu-id="8f5b2-141">Pour une entrée Waveform-Audio, l’ACM transmet des tampons d’ombre vides au pilote.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-141">For waveform-audio input, the ACM passes empty shadow buffers to the driver.</span></span> <span data-ttu-id="8f5b2-142">Elle utilise une tâche en arrière-plan pour recevoir une notification après que le pilote a rempli le tampon d’ombre.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-142">It uses a background task to receive a notification after the driver has filled the shadow buffer.</span></span> <span data-ttu-id="8f5b2-143">L’ACM transmet ensuite les tampons au pilote pour la compression.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-143">The ACM then passes the buffers to the driver for compression.</span></span> <span data-ttu-id="8f5b2-144">Une fois la compression terminée, le pilote transmet les données à l’application.</span><span class="sxs-lookup"><span data-stu-id="8f5b2-144">After compression is finished, the driver passes the data to the application.</span></span>

 

 




