---
title: Gestion de l’enregistrement MIDI
description: Gestion de l’enregistrement MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- MIDI (Musical Instrument Digital Interface), enregistrement
- MIDI (Musical Instrument Digital Interface), enregistrement
- enregistrement d’un fichier audio MIDI, gestion
- Enregistrement MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462974"
---
# <a name="managing-midi-recording"></a><span data-ttu-id="dab4d-107">Gestion de l’enregistrement MIDI</span><span class="sxs-lookup"><span data-stu-id="dab4d-107">Managing MIDI Recording</span></span>

<span data-ttu-id="dab4d-108">Après avoir ouvert un appareil MIDI, vous pouvez commencer à enregistrer des données MIDI.</span><span class="sxs-lookup"><span data-stu-id="dab4d-108">After you open a MIDI device, you can begin recording MIDI data.</span></span> <span data-ttu-id="dab4d-109">Windows fournit les fonctions suivantes pour la gestion de l’enregistrement MIDI.</span><span class="sxs-lookup"><span data-stu-id="dab4d-109">Windows provides the following functions for managing MIDI recording.</span></span>



| <span data-ttu-id="dab4d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="dab4d-110">Value</span></span>                                      | <span data-ttu-id="dab4d-111">Signification</span><span class="sxs-lookup"><span data-stu-id="dab4d-111">Meaning</span></span>                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dab4d-112">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="dab4d-112">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | <span data-ttu-id="dab4d-113">Envoie une mémoire tampon au pilote de périphérique afin qu’il puisse être rempli avec les données MIDI exclusives système enregistrées.</span><span class="sxs-lookup"><span data-stu-id="dab4d-113">Sends a buffer to the device driver so it can be filled with recorded system-exclusive MIDI data.</span></span> |
| [<span data-ttu-id="dab4d-114">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="dab4d-114">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | <span data-ttu-id="dab4d-115">Arrête l’enregistrement MIDI et marque toutes les mémoires tampons en attente comme terminées.</span><span class="sxs-lookup"><span data-stu-id="dab4d-115">Stops MIDI recording and marks all pending buffers as done.</span></span>                                       |
| [<span data-ttu-id="dab4d-116">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="dab4d-116">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | <span data-ttu-id="dab4d-117">Démarre l’enregistrement MIDI et réinitialise l’horodatage à zéro.</span><span class="sxs-lookup"><span data-stu-id="dab4d-117">Starts MIDI recording and resets the time stamp to zero.</span></span>                                          |
| [<span data-ttu-id="dab4d-118">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="dab4d-118">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | <span data-ttu-id="dab4d-119">Arrête l’enregistrement MIDI.</span><span class="sxs-lookup"><span data-stu-id="dab4d-119">Stops MIDI recording.</span></span>                                                                             |



 

<span data-ttu-id="dab4d-120">Pour envoyer des tampons au pilote de périphérique afin d’enregistrer des messages système exclusifs, utilisez [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span><span class="sxs-lookup"><span data-stu-id="dab4d-120">To send buffers to the device driver for recording system-exclusive messages, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span></span> <span data-ttu-id="dab4d-121">L’application est avertie lorsque les mémoires tampons sont remplies avec des données enregistrées exclusives du système.</span><span class="sxs-lookup"><span data-stu-id="dab4d-121">The application is notified as the buffers are filled with system-exclusive recorded data.</span></span> <span data-ttu-id="dab4d-122">Pour plus d’informations sur les techniques de notification, consultez [gestion des blocs de données MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="dab4d-122">For more information about the notification techniques, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

<span data-ttu-id="dab4d-123">La fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) commence le processus d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dab4d-123">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function begins the recording process.</span></span> <span data-ttu-id="dab4d-124">Lors de l’enregistrement de messages système exclusifs, envoyez au moins une mémoire tampon au pilote avant de commencer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dab4d-124">When recording system-exclusive messages, send at least one buffer to the driver before starting recording.</span></span> <span data-ttu-id="dab4d-125">Pour arrêter l’enregistrement, utilisez [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span><span class="sxs-lookup"><span data-stu-id="dab4d-125">To stop recording, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span></span> <span data-ttu-id="dab4d-126">Avant de fermer l’appareil à l’aide de la fonction [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) , marquez les blocs de données en attente comme étant effectués en appelant [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span><span class="sxs-lookup"><span data-stu-id="dab4d-126">Before closing the device by using the [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) function, mark any pending data blocks as being done by calling [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span></span>

<span data-ttu-id="dab4d-127">Les applications qui requièrent des données horodatées utilisent une fonction de rappel pour recevoir les données MIDI.</span><span class="sxs-lookup"><span data-stu-id="dab4d-127">Applications that require time-stamped data use a callback function to receive MIDI data.</span></span> <span data-ttu-id="dab4d-128">Si vos exigences de synchronisation ne sont pas strictes, vous pouvez utiliser une fenêtre ou un rappel de thread.</span><span class="sxs-lookup"><span data-stu-id="dab4d-128">If your timing requirements are not strict, you can use a window or thread callback.</span></span> <span data-ttu-id="dab4d-129">Toutefois, vous ne pouvez pas utiliser un rappel d’événement pour recevoir des données MIDI.</span><span class="sxs-lookup"><span data-stu-id="dab4d-129">However, you cannot use an event callback to receive MIDI data.</span></span>

<span data-ttu-id="dab4d-130">Pour enregistrer des messages système exclusifs avec des applications qui n’utilisent pas de mémoires tampons de flux, vous devez fournir le pilote de périphérique avec des tampons.</span><span class="sxs-lookup"><span data-stu-id="dab4d-130">To record system-exclusive messages with applications that do not use stream buffers, you must supply the device driver with buffers.</span></span> <span data-ttu-id="dab4d-131">Ces mémoires tampons sont spécifiées à l’aide d’une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="dab4d-131">These buffers are specified by using a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dab4d-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dab4d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dab4d-133">Enregistrement d’un fichier audio MIDI</span><span class="sxs-lookup"><span data-stu-id="dab4d-133">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 