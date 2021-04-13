---
title: Réception de messages Time-Stamped MIDI
description: Réception de messages Time-Stamped MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- MIDI (Musical Instrument Digital Interface), messages horodatés
- MIDI (Musical Instrument Digital Interface), messages horodatés
- enregistrement d’un fichier audio MIDI, messages horodatés
- messages MIDI horodatés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314862"
---
# <a name="receiving-time-stamped-midi-messages"></a><span data-ttu-id="74c5a-107">Réception de messages Time-Stamped MIDI</span><span class="sxs-lookup"><span data-stu-id="74c5a-107">Receiving Time-Stamped MIDI Messages</span></span>

<span data-ttu-id="74c5a-108">En raison du délai entre le moment où le pilote de périphérique reçoit un message MIDI et le moment où l’application reçoit le message, l’horodatage des pilotes de périphériques d’entrée MIDI est le message MIDI avec l’heure à laquelle le message a été reçu.</span><span class="sxs-lookup"><span data-stu-id="74c5a-108">Because of the delay between when the device driver receives a MIDI message and the time the application receives the message, MIDI input device drivers time stamp the MIDI message with the time that the message was received.</span></span> <span data-ttu-id="74c5a-109">Les horodatages MIDI, qui sont définis au moment de la réception du premier octet du message, sont spécifiés en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="74c5a-109">MIDI time stamps, which are defined as the time the first byte of the message was received, are specified in milliseconds.</span></span> <span data-ttu-id="74c5a-110">La fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) réinitialise les horodatages pour un appareil à zéro.</span><span class="sxs-lookup"><span data-stu-id="74c5a-110">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function resets the time stamps for a device to zero.</span></span>

<span data-ttu-id="74c5a-111">Comme indiqué précédemment, pour recevoir des horodatages avec entrée MIDI, vous devez utiliser une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="74c5a-111">As stated previously, to receive time stamps with MIDI input, you must use a callback function.</span></span> <span data-ttu-id="74c5a-112">Le paramètre *dwParam2* de la fonction de rappel spécifie l’horodatage des données associées aux messages [**MIM \_**](mim-data.md) et [**\_ LONGDATA MIM**](mim-longdata.md) .</span><span class="sxs-lookup"><span data-stu-id="74c5a-112">The *dwParam2* parameter of the callback function specifies the time stamp for data associated with the [**MIM\_DATA**](mim-data.md) and [**MIM\_LONGDATA**](mim-longdata.md) messages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74c5a-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74c5a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74c5a-114">Enregistrement d’un fichier audio MIDI</span><span class="sxs-lookup"><span data-stu-id="74c5a-114">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 