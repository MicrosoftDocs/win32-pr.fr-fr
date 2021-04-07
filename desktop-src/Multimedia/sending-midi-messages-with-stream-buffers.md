---
title: Envoi de messages MIDI avec des mémoires tampons de flux
description: Envoi de messages MIDI avec des mémoires tampons de flux
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- lire des fichiers MIDI, mémoires tampons de flux
- mémoires tampons de flux, envoyer des messages MIDI
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- Jeux de fichiers MIDI, envoi de messages
- envoi de messages MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725357"
---
# <a name="sending-midi-messages-with-stream-buffers"></a><span data-ttu-id="db356-111">Envoi de messages MIDI avec des mémoires tampons de flux</span><span class="sxs-lookup"><span data-stu-id="db356-111">Sending MIDI Messages with Stream Buffers</span></span>

<span data-ttu-id="db356-112">Lorsque votre application fonctionne avec des tampons de flux, elle utilise la fonction [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) pour envoyer tous les messages MIDI (courts et longs) à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="db356-112">When your application works with stream buffers, it uses the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function to send all (short and long) MIDI messages to the device.</span></span> <span data-ttu-id="db356-113">Pour spécifier des blocs de données de flux, utilisez les structures [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) et [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="db356-113">To specify stream data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) and [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structures.</span></span> <span data-ttu-id="db356-114">La structure **MIDIHDR** contient l’adresse d’un bloc de données verrouillé, la longueur du bloc de données et certains indicateurs assortis.</span><span class="sxs-lookup"><span data-stu-id="db356-114">The **MIDIHDR** structure contains an address of a locked data block, the data-block length, and some assorted flags.</span></span> <span data-ttu-id="db356-115">Les données sont stockées sous la forme de structures **MIDIEVENT** .</span><span class="sxs-lookup"><span data-stu-id="db356-115">The data is stored in the form of **MIDIEVENT** structures.</span></span> <span data-ttu-id="db356-116">Le système impose une limite de taille de 64 Ko sur les mémoires tampons de flux.</span><span class="sxs-lookup"><span data-stu-id="db356-116">The system imposes a size limit of 64K on stream buffers.</span></span>

<span data-ttu-id="db356-117">Une fois que vous avez utilisé **midiStreamOut** pour envoyer une mémoire tampon de données de flux de données, vous devez attendre que le pilote de périphérique se termine avec le bloc de données avant de le libérer.</span><span class="sxs-lookup"><span data-stu-id="db356-117">After you use **midiStreamOut** to send a stream buffer of data, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="db356-118">Si vous envoyez plusieurs blocs de données, vous devez surveiller l’achèvement de chaque bloc de données afin de savoir quand envoyer des blocs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="db356-118">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="db356-119">Pour plus d’informations sur les différentes techniques d’analyse de la saisie semi-automatique des blocs de données, consultez [gestion des blocs de données MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="db356-119">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 