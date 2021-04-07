---
title: Utilisation d’une fonction de rappel pour gérer la lecture mise en mémoire tampon
description: Utilisation d’une fonction de rappel pour gérer la lecture mise en mémoire tampon
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- Interface MIDI (Musical Instrument Digital Interface), lecture mise en mémoire tampon
- MIDI (Musical Instrument Digital Interface), lecture mise en mémoire tampon
- lecture de fichiers MIDI, lecture en mémoire tampon
- lecture mise en mémoire tampon
- Message MOM_CLOSE
- Message MOM_DONE
- Message MOM_OPEN
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- Jeux de fichiers MIDI, envoi de messages
- envoi de messages MIDI
- MIDI (Musical Instrument Digital Interface), fonctions de rappel
- MIDI (Musical Instrument Digital Interface), fonctions de rappel
- Jeux de fichiers MIDI, fonctions de rappel
- MidiOutProc fonction de rappel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726293"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a><span data-ttu-id="bd095-118">Utilisation d’une fonction de rappel pour gérer la lecture mise en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="bd095-118">Using a Callback Function to Manage Buffered Playback</span></span>

<span data-ttu-id="bd095-119">Vous pouvez définir votre propre fonction de rappel pour gérer la lecture en mémoire tampon des appareils de sortie MIDI.</span><span class="sxs-lookup"><span data-stu-id="bd095-119">You can define your own callback function to manage buffered playback of MIDI output devices.</span></span> <span data-ttu-id="bd095-120">La fonction de rappel est documentée en tant que [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bd095-120">The callback function is documented as [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span></span>

<span data-ttu-id="bd095-121">Les messages suivants peuvent être envoyés au paramètre *wMsg* de la fonction de rappel **MidiOutProc** .</span><span class="sxs-lookup"><span data-stu-id="bd095-121">The following messages can be sent to the *wMsg* parameter of the **MidiOutProc** callback function.</span></span>



| <span data-ttu-id="bd095-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd095-122">Value</span></span>                           | <span data-ttu-id="bd095-123">Signification</span><span class="sxs-lookup"><span data-stu-id="bd095-123">Meaning</span></span>                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd095-124">**\_fermeture MOM**</span><span class="sxs-lookup"><span data-stu-id="bd095-124">**MOM\_CLOSE**</span></span>](mom-close.md) | <span data-ttu-id="bd095-125">Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="bd095-125">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="bd095-126">**MOM \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="bd095-126">**MOM\_DONE**</span></span>](mom-done.md)   | <span data-ttu-id="bd095-127">Envoyé lorsque le pilote de périphérique est terminé avec un bloc de données envoyé à l’aide de la fonction [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) ou [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="bd095-127">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="bd095-128">**MOM \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="bd095-128">**MOM\_OPEN**</span></span>](mom-open.md)   | <span data-ttu-id="bd095-129">Envoyé lorsque l’appareil est ouvert à l’aide de la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="bd095-129">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="bd095-130">Ces messages sont similaires à ceux envoyés aux fonctions de procédure de fenêtre, mais les paramètres sont différents.</span><span class="sxs-lookup"><span data-stu-id="bd095-130">These messages are similar to those sent to window procedure functions, but the parameters are different.</span></span> <span data-ttu-id="bd095-131">Un handle de l’appareil MIDI ouvert est passé en tant que paramètre à la fonction de rappel, avec le mot double des données d’instance passées à l’aide de **midiOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="bd095-131">A handle of the open MIDI device is passed as a parameter to the callback function, along with the doubleword of instance data passed by using **midiOutOpen**.</span></span>

<span data-ttu-id="bd095-132">Une fois le pilote terminé avec un bloc de données, vous pouvez nettoyer et libérer le bloc de données.</span><span class="sxs-lookup"><span data-stu-id="bd095-132">After the driver is finished with a data block, you can clean up and free the data block.</span></span> <span data-ttu-id="bd095-133">En raison des restrictions suggérées sur les fonctions de rappel, il est préférable de ne pas le faire à partir de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="bd095-133">Because of the suggested restrictions on callback functions, it is better not to do this from within the callback function.</span></span>

 

 