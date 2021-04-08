---
title: Ouverture de périphériques d’entrée MIDI
description: Ouverture de périphériques d’entrée MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Interface MIDI (Musical Instrument Digital Interface), appareils d’entrée
- MIDI (Musical Instrument Digital Interface), appareils d’entrée
- enregistrement de données audio MIDI, appareils d’entrée
- Périphériques d’entrée MIDI
- Interface MIDI (Musical Instrument Digital Interface), ouverture des périphériques d’entrée
- MIDI (Musical Instrument Digital Interface), ouverture des appareils d’entrée
- enregistrement de l’audio MIDI, ouverture des appareils d’entrée
- ouverture de périphériques d’entrée MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726317"
---
# <a name="opening-midi-input-devices"></a><span data-ttu-id="2491e-111">Ouverture de périphériques d’entrée MIDI</span><span class="sxs-lookup"><span data-stu-id="2491e-111">Opening MIDI Input Devices</span></span>

<span data-ttu-id="2491e-112">Pour ouvrir un appareil d’entrée MIDI pour l’enregistrement, utilisez la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="2491e-112">To open a MIDI input device for recording, use the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span> <span data-ttu-id="2491e-113">Cette fonction ouvre l’appareil associé à l’identificateur de périphérique spécifié et retourne un descripteur de l’appareil ouvert en écrivant le handle dans un emplacement de mémoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="2491e-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="2491e-114">Si vous utilisez l' \_ indicateur d’état d’e/s midi \_ avec **midiInOpen**, le système utilise le message [**MIM \_ MOREDATA**](mim-moredata.md) pour alerter la fonction de rappel de votre application lorsqu’il ne traite pas les données MIDI suffisamment rapidement pour suivre le pilote de périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2491e-114">If you use the MIDI\_IO\_STATUS flag with **midiInOpen**, the system uses the [**MIM\_MOREDATA**](mim-moredata.md) message to alert your application's callback function when it is not processing MIDI data fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="2491e-115">(Le message [**mm \_ MIM \_ MOREDATA**](mm-mim-moredata.md) effectue la même tâche avec les rappels de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2491e-115">(The [**MM\_MIM\_MOREDATA**](mm-mim-moredata.md) message does the same job with window callbacks.</span></span> <span data-ttu-id="2491e-116">Toutefois, pour des raisons de performances, la plupart des applications utilisent des fonctions de rappel au lieu de rappels de fenêtre.) Si votre application traite des données MIDI dans un thread séparé, l’augmentation de la priorité du thread peut avoir un impact significatif sur la capacité de l’application à suivre le processus de données.</span><span class="sxs-lookup"><span data-stu-id="2491e-116">However, for performance reasons, most applications will use callback functions instead of window callbacks.) If your application processes MIDI data in a separate thread, boosting the thread's priority can have a significant impact on the application's ability to keep up with the data flow.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2491e-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2491e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2491e-118">Enregistrement d’un fichier audio MIDI</span><span class="sxs-lookup"><span data-stu-id="2491e-118">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 