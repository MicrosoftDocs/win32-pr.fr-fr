---
title: Traitement des données MIDI à partir de deux sources MIDI
description: Traitement des données MIDI à partir de deux sources MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Multimédia Windows, traitement de données MIDI à partir de deux sources
- multimédia, traitement de données MIDI à partir de deux sources
- audio multimédia, traitement de données MIDI à partir de deux sources
- audio, traitement des données MIDI à partir de deux sources
- Interface MIDI (Musical Instrument Digital Interface), traitement des données à partir de deux sources
- MIDI (Musical Instrument Digital Interface), traitement des données à partir de deux sources
- traitement des données MIDI à partir de deux sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031174"
---
# <a name="processing-midi-data-from-two-midi-sources"></a><span data-ttu-id="53a26-110">Traitement des données MIDI à partir de deux sources MIDI</span><span class="sxs-lookup"><span data-stu-id="53a26-110">Processing MIDI Data from Two MIDI Sources</span></span>

<span data-ttu-id="53a26-111">Le sous-système MIDI peut acheminer des messages MIDI de deux sources de données vers un seul périphérique de sortie MIDI pour une lecture simultanée.</span><span class="sxs-lookup"><span data-stu-id="53a26-111">The MIDI subsystem can route MIDI messages from two data sources to a single MIDI output device for concurrent playback.</span></span> <span data-ttu-id="53a26-112">Par exemple, une source peut être une musique en arrière-plan ou une ligne de basses qui a été pré-enregistrée et stockée dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="53a26-112">For example, one source can be background music or a bass line that has been pre-recorded and stored in a file.</span></span> <span data-ttu-id="53a26-113">La deuxième source peut être des données en temps réel à partir d’un instrument MIDI, tel qu’un clavier ou une guitare.</span><span class="sxs-lookup"><span data-stu-id="53a26-113">The second source can be live data from a MIDI instrument, such as a keyboard or guitar.</span></span>

<span data-ttu-id="53a26-114">Les deux sources de données envoient des données MIDI à un seul appareil MIDI identifié avec un seul descripteur.</span><span class="sxs-lookup"><span data-stu-id="53a26-114">Both data sources send MIDI data to a single MIDI device that is identified with one handle.</span></span> <span data-ttu-id="53a26-115">Envoyer un flux de données à l’aide de la fonction [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) et d’une ou plusieurs mémoires tampons de flux.</span><span class="sxs-lookup"><span data-stu-id="53a26-115">Send one data stream by using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function and one or more stream buffers.</span></span> <span data-ttu-id="53a26-116">Ce flux de données contient généralement des données préenregistrées qui sont compressées dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="53a26-116">This data stream typically contains prerecorded data that is packed into the buffer.</span></span>

<span data-ttu-id="53a26-117">Envoyez le deuxième flux de données (généralement à partir d’un instrument MIDI) de façon asynchrone à l’aide de la fonction [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) .</span><span class="sxs-lookup"><span data-stu-id="53a26-117">Send the second data stream (typically from a MIDI instrument) asynchronously by using the [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) function.</span></span> <span data-ttu-id="53a26-118">L’état d’exécution d’une mémoire tampon de flux n’est pas affecté par les appels asynchrones effectués par le deuxième flux de données.</span><span class="sxs-lookup"><span data-stu-id="53a26-118">The running status of a stream buffer will not be adversely affected by the asynchronous calls made by the second data stream.</span></span>

<span data-ttu-id="53a26-119">Chaque message bref envoyé avec **midiOutShortMsg** doit être un message MIDI complet, avec un octet d’État et le nombre approprié d’octets de données.</span><span class="sxs-lookup"><span data-stu-id="53a26-119">Each short message sent with **midiOutShortMsg** must be a complete MIDI message, with a status byte and the appropriate number of data bytes.</span></span> <span data-ttu-id="53a26-120">Si l’octet d’État est omis, **midiOutShortMsg** retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="53a26-120">If the status byte is omitted, **midiOutShortMsg** returns an error.</span></span> <span data-ttu-id="53a26-121">(Toutefois, il n’y a pas d’État en cours d’exécution avec la sortie du flux.)</span><span class="sxs-lookup"><span data-stu-id="53a26-121">(However, there is no running status with stream output.)</span></span>

 

 