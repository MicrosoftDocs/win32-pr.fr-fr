---
title: Résumé des cartes et des messages MIDI
description: Résumé des cartes et des messages MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, mappage de canal
- Mappeur MIDI, mappages de correctifs
- Mappeur MIDI, mappages de clés
- carte de canal
- mappages de correctifs
- cartes clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675069"
---
# <a name="summary-of-maps-and-midi-messages"></a><span data-ttu-id="e75f0-111">Résumé des cartes et des messages MIDI</span><span class="sxs-lookup"><span data-stu-id="e75f0-111">Summary of Maps and MIDI Messages</span></span>

<span data-ttu-id="e75f0-112">Voici les octets d’État pour les messages MIDI et les types de cartes qui affectent chaque message.</span><span class="sxs-lookup"><span data-stu-id="e75f0-112">Following are the status bytes for MIDI messages and the map types that affect each message.</span></span>



| <span data-ttu-id="e75f0-113">État MIDI</span><span class="sxs-lookup"><span data-stu-id="e75f0-113">MIDI status</span></span> | <span data-ttu-id="e75f0-114">Description</span><span class="sxs-lookup"><span data-stu-id="e75f0-114">Description</span></span>               | <span data-ttu-id="e75f0-115">Types de cartes</span><span class="sxs-lookup"><span data-stu-id="e75f0-115">Map types</span></span>                |
|-------------|---------------------------|--------------------------|
| <span data-ttu-id="e75f0-116">0x80-0x8F</span><span class="sxs-lookup"><span data-stu-id="e75f0-116">0x80-0x8F</span></span>   | <span data-ttu-id="e75f0-117">Note désactivée</span><span class="sxs-lookup"><span data-stu-id="e75f0-117">Note off</span></span>                  | <span data-ttu-id="e75f0-118">Cartes de canaux, cartes clés</span><span class="sxs-lookup"><span data-stu-id="e75f0-118">Channel maps, key maps</span></span>   |
| <span data-ttu-id="e75f0-119">0x90-0x9F</span><span class="sxs-lookup"><span data-stu-id="e75f0-119">0x90-0x9F</span></span>   | <span data-ttu-id="e75f0-120">Remarque sur </span><span class="sxs-lookup"><span data-stu-id="e75f0-120">Note on</span></span>                   | <span data-ttu-id="e75f0-121">Cartes de canaux, cartes clés</span><span class="sxs-lookup"><span data-stu-id="e75f0-121">Channel maps, key maps</span></span>   |
| <span data-ttu-id="e75f0-122">0xA0-0xAF</span><span class="sxs-lookup"><span data-stu-id="e75f0-122">0xA0-0xAF</span></span>   | <span data-ttu-id="e75f0-123">Polyphonic-clé aftertouch</span><span class="sxs-lookup"><span data-stu-id="e75f0-123">Polyphonic-key aftertouch</span></span> | <span data-ttu-id="e75f0-124">Cartes de canaux, cartes clés</span><span class="sxs-lookup"><span data-stu-id="e75f0-124">Channel maps, key maps</span></span>   |
| <span data-ttu-id="e75f0-125">0xB0-0xBF</span><span class="sxs-lookup"><span data-stu-id="e75f0-125">0xB0-0xBF</span></span>   | <span data-ttu-id="e75f0-126">Modification du contrôle</span><span class="sxs-lookup"><span data-stu-id="e75f0-126">Control change</span></span>            | <span data-ttu-id="e75f0-127">Cartes de canaux, mappages de correctifs</span><span class="sxs-lookup"><span data-stu-id="e75f0-127">Channel maps, patch maps</span></span> |
| <span data-ttu-id="e75f0-128">0xC0-0xCF</span><span class="sxs-lookup"><span data-stu-id="e75f0-128">0xC0-0xCF</span></span>   | <span data-ttu-id="e75f0-129">Changement de programme</span><span class="sxs-lookup"><span data-stu-id="e75f0-129">Program change</span></span>            | <span data-ttu-id="e75f0-130">Cartes de canaux, mappages de correctifs</span><span class="sxs-lookup"><span data-stu-id="e75f0-130">Channel maps, patch maps</span></span> |
| <span data-ttu-id="e75f0-131">0xD0-0xDF</span><span class="sxs-lookup"><span data-stu-id="e75f0-131">0xD0-0xDF</span></span>   | <span data-ttu-id="e75f0-132">Canal aftertouch</span><span class="sxs-lookup"><span data-stu-id="e75f0-132">Channel aftertouch</span></span>        | <span data-ttu-id="e75f0-133">Cartes de canal</span><span class="sxs-lookup"><span data-stu-id="e75f0-133">Channel maps</span></span>             |
| <span data-ttu-id="e75f0-134">0xE0-0xEF</span><span class="sxs-lookup"><span data-stu-id="e75f0-134">0xE0-0xEF</span></span>   | <span data-ttu-id="e75f0-135">Changement de courbure</span><span class="sxs-lookup"><span data-stu-id="e75f0-135">Pitch-bend change</span></span>         | <span data-ttu-id="e75f0-136">Cartes de canal</span><span class="sxs-lookup"><span data-stu-id="e75f0-136">Channel maps</span></span>             |
| <span data-ttu-id="e75f0-137">0xF0-0xFF</span><span class="sxs-lookup"><span data-stu-id="e75f0-137">0xF0-0xFF</span></span>   | <span data-ttu-id="e75f0-138">Système</span><span class="sxs-lookup"><span data-stu-id="e75f0-138">System</span></span>                    | <span data-ttu-id="e75f0-139">Non mappé</span><span class="sxs-lookup"><span data-stu-id="e75f0-139">Not mapped</span></span>               |



 

-   <span data-ttu-id="e75f0-140">Les quatre bits de poids fort représentent la valeur d’État.</span><span class="sxs-lookup"><span data-stu-id="e75f0-140">The high-order four bits represent the status value.</span></span> <span data-ttu-id="e75f0-141">Les quatre bits de poids faible représentent les informations de canal.</span><span class="sxs-lookup"><span data-stu-id="e75f0-141">The low-order four bits represent the channel information.</span></span>
-   <span data-ttu-id="e75f0-142">Les mappages de correctifs affectent uniquement le contrôleur 7 (volume principal).</span><span class="sxs-lookup"><span data-stu-id="e75f0-142">Patch maps affect only controller 7 (main volume).</span></span>
-   <span data-ttu-id="e75f0-143">Les messages système sont envoyés à tous les appareils répertoriés dans une carte de canal.</span><span class="sxs-lookup"><span data-stu-id="e75f0-143">System messages are sent to all devices listed in a channel map.</span></span>

 

 




