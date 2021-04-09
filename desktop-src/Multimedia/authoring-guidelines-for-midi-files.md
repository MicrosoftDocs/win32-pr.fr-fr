---
title: Instructions de création pour les fichiers MIDI
description: Instructions de création pour les fichiers MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Instructions de création de fichiers MIDI (Musical Instrument Digital Interface)
- MIDI (Musical Instrument Digital Interface), instructions de création de fichiers
- création de fichiers MIDI, instructions de création de fichiers
- attributions de correctifs MIDI standard
- attributions de clés MIDI standard
- Interface MIDI (Musical Instrument Digital Interface), attributions de correctifs standard
- MIDI (Musical Instrument Digital Interface), attributions de correctifs standard
- MIDI (Musical Instrument Digital Interface), attributions de touches standard
- MIDI (Musical Instrument Digital Interface), attributions de touches standard
- création de fichiers MIDI, attributions de correctifs standard
- création de fichiers MIDI, attributions de clés standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029767"
---
# <a name="authoring-guidelines-for-midi-files"></a><span data-ttu-id="6046d-114">Instructions de création pour les fichiers MIDI</span><span class="sxs-lookup"><span data-stu-id="6046d-114">Authoring Guidelines for MIDI Files</span></span>

<span data-ttu-id="6046d-115">Suivez ces instructions pour créer des fichiers MIDI indépendants de l’appareil pour Windows :</span><span class="sxs-lookup"><span data-stu-id="6046d-115">Follow these guidelines to author device-independent MIDI files for Windows:</span></span>

-   <span data-ttu-id="6046d-116">Utilisez les [affectations de correctifs MIDI standard](standard-midi-patch-assignments.md) et les [attributions de clés MIDI standard](standard-midi-key-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="6046d-116">Use the [Standard MIDI Patch Assignments](standard-midi-patch-assignments.md) and [Standard MIDI Key Assignments](standard-midi-key-assignments.md).</span></span>
-   <span data-ttu-id="6046d-117">Toujours envoyer un message de modification de programme à un canal pour sélectionner un correctif avant d’envoyer d’autres messages à ce canal.</span><span class="sxs-lookup"><span data-stu-id="6046d-117">Always send a program-change message to a channel to select a patch before sending other messages to that channel.</span></span> <span data-ttu-id="6046d-118">Pour les deux canaux à percussion (10 et 16), sélectionnez le numéro de programme 0.</span><span class="sxs-lookup"><span data-stu-id="6046d-118">For the two percussion channels (10 and 16), select program number 0.</span></span>
-   <span data-ttu-id="6046d-119">Suivez toujours un message MIDI de modification de programme avec un message de contrôleur de volume principal MIDI (numéro de contrôleur 7) pour définir le volume relatif du correctif.</span><span class="sxs-lookup"><span data-stu-id="6046d-119">Always follow a MIDI program-change message with a MIDI main-volume controller message (controller number 7) to set the relative volume of the patch.</span></span>
-   <span data-ttu-id="6046d-120">Utilisez la valeur 80 (0x50) pour le contrôleur de volume principal pour les niveaux d’écoute normale.</span><span class="sxs-lookup"><span data-stu-id="6046d-120">Use a value of 80 (0x50) for the main-volume controller for normal listening levels.</span></span> <span data-ttu-id="6046d-121">Pour des niveaux plus silencieux ou plus forts, vous pouvez utiliser des valeurs inférieures ou supérieures.</span><span class="sxs-lookup"><span data-stu-id="6046d-121">For quieter or louder levels, you can use lower or higher values.</span></span>
-   <span data-ttu-id="6046d-122">Utilisez uniquement les messages MIDI suivants : Remarque avec la vélocité, la note de désactivation, le changement de programme, la courbure du tangage, le volume principal (contrôleur 7) et la pédale d’amortisseur (contrôleur 64).</span><span class="sxs-lookup"><span data-stu-id="6046d-122">Use only the following MIDI messages: note-on with velocity, note-off, program change, pitch bend, main volume (controller 7), and damper pedal (controller 64).</span></span> <span data-ttu-id="6046d-123">Des synthétiseurs internes sont requis pour répondre à ces messages et la plupart des instruments de musique MIDI y répondent également.</span><span class="sxs-lookup"><span data-stu-id="6046d-123">Internal synthesizers are required to respond to these messages and most MIDI musical instruments respond to them as well.</span></span>

 

 




