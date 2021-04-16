---
title: Ouverture de périphériques de sortie MIDI
description: Ouverture de périphériques de sortie MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- Appareil de sortie MIDI (Musical Instrument Digital Interface)
- MIDI (Musical Instrument Digital Interface), périphériques de sortie
- Jeux de fichiers MIDI, périphériques de sortie
- Périphériques de sortie MIDI
- Interface MIDI (Musical Instrument Digital Interface), ouverture des périphériques de sortie
- MIDI (Musical Instrument Digital Interface), ouverture des appareils de sortie
- exécution de fichiers MIDI, ouverture d’appareils de sortie
- ouverture de périphériques de sortie MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463067"
---
# <a name="opening-midi-output-devices"></a><span data-ttu-id="c8f7e-111">Ouverture de périphériques de sortie MIDI</span><span class="sxs-lookup"><span data-stu-id="c8f7e-111">Opening MIDI Output Devices</span></span>

<span data-ttu-id="c8f7e-112">Pour ouvrir un appareil de sortie MIDI pour la lecture, utilisez la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="c8f7e-112">To open a MIDI output device for playback, use the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="c8f7e-113">Cette fonction ouvre l’appareil associé à l’identificateur de périphérique spécifié et retourne un descripteur de l’appareil ouvert en écrivant le handle dans un emplacement de mémoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="c8f7e-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="c8f7e-114">L’un des paramètres de **midiOutOpen** est une valeur de mot double.</span><span class="sxs-lookup"><span data-stu-id="c8f7e-114">One of the parameters of **midiOutOpen** is a doubleword value.</span></span> <span data-ttu-id="c8f7e-115">Cette valeur spécifie une fenêtre ou un handle de thread, un handle d’événement ou l’adresse d’une fonction de rappel utilisée pour surveiller la progression de la lecture des données et des mémoires tampons de flux exclusives du système MIDI.</span><span class="sxs-lookup"><span data-stu-id="c8f7e-115">This value specifies a window or thread handle, an event handle, or the address of a callback function that is used to monitor the progress of the playback of MIDI system-exclusive data and stream buffers.</span></span> <span data-ttu-id="c8f7e-116">La surveillance permet à l’application de déterminer quand envoyer des blocs de données supplémentaires et quand libérer des blocs de données qui ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="c8f7e-116">Monitoring enables the application to determine when to send additional data blocks and when to free data blocks that have been sent.</span></span> <span data-ttu-id="c8f7e-117">Pour plus d’informations sur ces méthodes, consultez [gestion des blocs de données MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="c8f7e-117">For more information about these methods, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 