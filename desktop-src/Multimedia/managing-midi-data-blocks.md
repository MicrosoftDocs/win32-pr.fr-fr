---
title: Gestion des blocs de données MIDI
description: Gestion des blocs de données MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- Interface MIDI (Musical Instrument Digital Interface), gestion des blocs de données
- MIDI (Musical Instrument Digital Interface), gestion des blocs de données
- Services MIDI, gestion des blocs de données
- gestion des blocs de données MIDI
- MIDI (Musical Instrument Digital Interface), traitement des messages de pilote
- MIDI (Musical Instrument Digital Interface), traitement des messages de pilote
- Services MIDI, traitement des messages de pilote
- traitement des messages du pilote
- MIDI (Musical Instrument Digital Interface), blocs de données
- MIDI (Musical Instrument Digital Interface), blocs de données
- Services MIDI, blocs de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940884"
---
# <a name="managing-midi-data-blocks"></a><span data-ttu-id="e7f33-114">Gestion des blocs de données MIDI</span><span class="sxs-lookup"><span data-stu-id="e7f33-114">Managing MIDI Data Blocks</span></span>

<span data-ttu-id="e7f33-115">Les applications qui utilisent des blocs de données pour transmettre des messages système exclusifs (à l’aide des fonctions [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) et [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) et des mémoires tampons de flux (à l’aide de la fonction [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ) doivent continuellement fournir au pilote de périphérique des blocs de données jusqu’à la fin de la lecture ou de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e7f33-115">Applications that use data blocks for passing system-exclusive messages (using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) and [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) functions) and stream buffers (using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function) must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="e7f33-116">Même si un bloc de données unique est utilisé, une application doit être en mesure de déterminer à quel moment un pilote de périphérique est terminé avec le bloc de données afin de libérer la mémoire associée au bloc de données et à la structure d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e7f33-116">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so it can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="e7f33-117">Trois méthodes peuvent être utilisées pour déterminer quand un pilote de périphérique est terminé avec un bloc de données :</span><span class="sxs-lookup"><span data-stu-id="e7f33-117">Three methods can be used to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="e7f33-118">Spécifiez une fonction de rappel pour recevoir un message envoyé par le pilote lorsqu’il a terminé avec un bloc de données.</span><span class="sxs-lookup"><span data-stu-id="e7f33-118">Specify a callback function to receive a message sent by the driver when it is finished with a data block.</span></span> <span data-ttu-id="e7f33-119">Pour obtenir des données d’entrée MIDI horodatées, vous devez utiliser une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="e7f33-119">To get time-stamped MIDI input data, you must use a callback function.</span></span>
-   <span data-ttu-id="e7f33-120">Utilisez un rappel d’événement (pour la sortie uniquement).</span><span class="sxs-lookup"><span data-stu-id="e7f33-120">Use an event callback (for output only).</span></span>
-   <span data-ttu-id="e7f33-121">Utilisez un rappel de fenêtre ou de thread pour recevoir un message envoyé par le pilote lorsqu’il a terminé avec un bloc de données.</span><span class="sxs-lookup"><span data-stu-id="e7f33-121">Use a window or thread callback to receive a message sent by the driver when it is finished with a data block.</span></span>

<span data-ttu-id="e7f33-122">Si une application n’obtient pas de bloc de données au pilote de périphérique quand cela est nécessaire, un décalage audible de lecture ou une perte d’informations d’enregistrement entrantes peut se produire.</span><span class="sxs-lookup"><span data-stu-id="e7f33-122">If an application does not get a data block to the device driver when it is needed, an audible gap in playback or a loss of incoming recorded information can occur.</span></span> <span data-ttu-id="e7f33-123">Au minimum, une application doit utiliser un schéma de double mise en mémoire tampon pour conserver au moins un bloc de données avant le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="e7f33-123">At a minimum, an application should use a double-buffering scheme to stay at least one data block ahead of the device driver.</span></span>

## <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="e7f33-124">Utilisation d’une fonction de rappel pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="e7f33-124">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="e7f33-125">Vous pouvez écrire votre propre fonction de rappel pour traiter les messages envoyés par le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="e7f33-125">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="e7f33-126">Pour utiliser une fonction de rappel, spécifiez l’indicateur de fonction de rappel \_ dans le paramètre *dwFlags* et l’adresse de la fonction de rappel dans le paramètre *DwCallback* de la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) ou [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="e7f33-126">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *dwFlags* parameter and the address of the callback function in the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="e7f33-127">Les messages envoyés à une fonction de rappel sont similaires aux messages envoyés à une fenêtre, sauf qu’ils ont deux paramètres de mot double au lieu d’un paramètre entier non signé et d’un paramètre de type double.</span><span class="sxs-lookup"><span data-stu-id="e7f33-127">Messages sent to a callback function are similar to messages sent to a window, except they have two doubleword parameters instead of an unsigned integer parameter and a doubleword parameter.</span></span> <span data-ttu-id="e7f33-128">Pour plus d’informations sur ces messages, consultez [envoi de messages System-Exclusive](sending-system-exclusive-messages.md) et [gestion de l’enregistrement midi](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="e7f33-128">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

<span data-ttu-id="e7f33-129">Utilisez l’une des techniques suivantes pour passer des données d’instance d’une application à une fonction de rappel :</span><span class="sxs-lookup"><span data-stu-id="e7f33-129">Use one of the following techniques to pass instance data from an application to a callback function:</span></span>

-   <span data-ttu-id="e7f33-130">Utilisez le paramètre *dwCallbackInstance* de la fonction qui ouvre le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="e7f33-130">Use the *dwCallbackInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="e7f33-131">Utilisez le membre **dwUser** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) qui identifie un bloc de données envoyé à un pilote de périphérique MIDI.</span><span class="sxs-lookup"><span data-stu-id="e7f33-131">Use the **dwUser** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies a data block being sent to a MIDI device driver.</span></span>

<span data-ttu-id="e7f33-132">Si vous avez besoin de plus de 32 bits de données d’instance, transmettez l’adresse d’une structure contenant les informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e7f33-132">If you need more than 32 bits of instance data, pass an address of a structure containing the additional information.</span></span>

## <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="e7f33-133">Utilisation d’un rappel d’événement pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="e7f33-133">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="e7f33-134">Pour utiliser un rappel d’événement, utilisez la fonction [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) pour récupérer le handle d’un événement et spécifiez l’événement de rappel \_ dans l’appel à la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="e7f33-134">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event and specify CALLBACK\_EVENT in the call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="e7f33-135">Un rappel d’événement est défini par tout ce qui peut provoquer un rappel de fonction.</span><span class="sxs-lookup"><span data-stu-id="e7f33-135">An event callback is set by anything that might cause a function callback.</span></span> <span data-ttu-id="e7f33-136">Contrairement aux fonctions de rappel et aux rappels de fenêtre ou de thread, les rappels d’événements ne reçoivent pas de notifications de fermeture, de fin ou d’ouverture spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e7f33-136">Unlike callback functions and window or thread callbacks, event callbacks do not receive specific close, done, or open notifications.</span></span> <span data-ttu-id="e7f33-137">Par conséquent, une application peut être amenée à vérifier l’état du processus en attente lorsque l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="e7f33-137">Therefore, an application may have to check the status of the process it is waiting for after the event occurs.</span></span>

<span data-ttu-id="e7f33-138">Pour plus d’informations sur les rappels d’événements, consultez [utilisation d’un rappel d’événement pour gérer la lecture mise en mémoire tampon](using-an-callback-to-manage-buffered-playback.md).</span><span class="sxs-lookup"><span data-stu-id="e7f33-138">For more information about event callbacks, see [Using an Event Callback to Manage Buffered Playback](using-an-callback-to-manage-buffered-playback.md).</span></span>

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a><span data-ttu-id="e7f33-139">Utilisation d’une fenêtre ou d’un rappel de thread pour traiter des messages de pilote</span><span class="sxs-lookup"><span data-stu-id="e7f33-139">Using a Window or Thread Callback to Process Driver Messages</span></span>

<span data-ttu-id="e7f33-140">Pour utiliser un rappel de fenêtre, spécifiez l' \_ indicateur de fenêtre de rappel dans le paramètre *dwFlags* et un handle de fenêtre dans le mot de poids faible du paramètre *DwCallback* de la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) ou [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="e7f33-140">To use a window callback, specify the CALLBACK\_WINDOW flag in the *dwFlags* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="e7f33-141">Les messages de pilote seront envoyés à la fonction de procédure de fenêtre pour la fenêtre identifiée par le handle dans *dwCallback*.</span><span class="sxs-lookup"><span data-stu-id="e7f33-141">Driver messages will be sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="e7f33-142">De même, pour utiliser un rappel de thread, spécifiez l’indicateur de thread de rappel \_ et un identificateur de thread dans l’appel à **MidiInOpen** ou **midiOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="e7f33-142">Similarly, to use a thread callback, specify the CALLBACK\_THREAD flag and a thread identifier in the call to **midiInOpen** or **midiOutOpen**.</span></span> <span data-ttu-id="e7f33-143">Dans ce cas, les messages sont publiés dans le thread spécifié et non dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e7f33-143">In this case, messages will be posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="e7f33-144">Les messages envoyés à une fenêtre ou un rappel de thread sont spécifiques au périphérique MIDI utilisé.</span><span class="sxs-lookup"><span data-stu-id="e7f33-144">Messages sent to a window or thread callback are specific to the MIDI device used.</span></span> <span data-ttu-id="e7f33-145">Pour plus d’informations sur ces messages, consultez [envoi de messages System-Exclusive](sending-system-exclusive-messages.md) et [gestion de l’enregistrement midi](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="e7f33-145">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7f33-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7f33-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7f33-147">Services MIDI</span><span class="sxs-lookup"><span data-stu-id="e7f33-147">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 